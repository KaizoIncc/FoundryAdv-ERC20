# 🪙 FoundryAdv-ERC20

Este proyecto demuestra la implementación de un token ERC20 utilizando [Foundry](https://book.getfoundry.sh/), una herramienta rápida y modular para el desarrollo de aplicaciones en Ethereum. El contrato aprovecha las bibliotecas de [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts) para garantizar una implementación segura y estándar.

## 📦 Características

- Token ERC20 personalizado con nombre y símbolo definidos.
- Funcionalidades estándar: `transfer`, `approve`, `transferFrom`, `mint`, `burn`.
- Uso de contratos de OpenZeppelin para seguridad y fiabilidad.
- Scripts de despliegue y pruebas automatizadas con Foundry.

## 🗂️ Estructura del Proyecto

```
FoundryAdv-ERC20/
├── lib/                 # Dependencias externas (OpenZeppelin)
├── script/              # Scripts de despliegue
├── src/                 # Contratos fuente (ERC20)
├── test/                # Pruebas en Solidity
├── foundry.toml         # Configuración del proyecto Foundry
├── Makefile             # Tareas automatizadas
└── .gitignore           # Archivos y carpetas ignoradas por Git
```

## ⚙️ Requisitos Previos

- [Foundry](https://book.getfoundry.sh/getting-started/installation) instalado.
- [Node.js](https://nodejs.org/) (opcional, para herramientas adicionales).
- RPC URL (por ejemplo, de Alchemy o Infura).
- Clave privada con fondos en una testnet (por ejemplo, Sepolia).

## 🚀 Uso

### 🔨 Compilar

```bash
forge build
```

### ✅ Probar

```bash
forge test
```

### 🧪 Tomar una instantánea de gas

```bash
forge snapshot
```

### 🛠️ Desplegar

```bash
forge script script/DeployToken.s.sol:DeployToken --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify
```

> Asegúrate de tener configuradas tus variables de entorno:

```env
SEPOLIA_RPC_URL=https://sepolia.infura.io/v3/tu-api-key
PRIVATE_KEY=tu_clave_privada
ETHERSCAN_API_KEY=tu_api_key
```

## 🧪 Pruebas

Las pruebas están ubicadas en la carpeta `test/` y cubren:

- Transferencias de tokens.
- Aprobaciones y asignaciones.
- Funciones de `mint` y `burn`.

Ejecuta las pruebas con:

```bash
forge test -vv
```

## 📜 Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.

## 🙌 Agradecimientos

Inspirado en las prácticas recomendadas de desarrollo de contratos inteligentes y en la comunidad de Ethereum.
