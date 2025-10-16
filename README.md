# 🎮 Tic-Tac-Toe Game

Un juego clásico de Tres en Raya (Tic-Tac-Toe) desarrollado con React.js

## ✨ ¿Qué tiene este proyecto?

✅ **Tablero de 3x3 funcional** - Juega en un tablero interactivo  
✅ **Alternancia entre jugadores** - X y O se turnan automáticamente  
✅ **Detección de ganador** - El juego identifica al ganador instantáneamente  
✅ **Historial de movimientos** - Revisa todas las jugadas realizadas  
✅ **Viaje en el tiempo** - Vuelve a cualquier jugada anterior  
✅ **Interfaz moderna** - Diseño limpio y responsive con animaciones  

## 🚀 ¿Qué puedes agregar?

El juego base está completo, pero puedes mejorarlo con:

1. **Detección de empate** - Mostrar mensaje cuando se llena el tablero sin ganador
2. **Resaltar línea ganadora** - Marcar visualmente las 3 casillas ganadoras
3. **Botón de reinicio** - Para empezar una nueva partida rápidamente
4. **Animaciones avanzadas** - Transiciones suaves al hacer clic
5. **Contador de victorias** - Llevar registro de X vs O
6. **Modo oscuro** - Toggle para cambiar el tema
7. **Coordenadas en el historial** - Ver qué casilla se jugó en cada movimiento (ej: "X jugó en (1, 2)")

## 📋 Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- [Node.js](https://nodejs.org/) (versión LTS recomendada)
- npm (viene incluido con Node.js)
- Un editor de código como [Visual Studio Code](https://code.visualstudio.com/)

## 🛠️ Instalación

Sigue estos pasos para configurar el proyecto en tu máquina local:

### 1. Verificar Node.js y npm

```bash
node --version
npm --version
```

### 2. Crear el proyecto React

```bash
# Navega a la carpeta donde quieres crear el proyecto
cd Documents

# Crea el proyecto
npx create-react-app tic-tac-toe

# Entra a la carpeta del proyecto
cd tic-tac-toe
```

### 3. Configurar los archivos

#### `src/App.js`
Reemplaza el contenido con el código del juego (componentes Square, Board, Game y calculateWinner)

#### `src/App.css`
Agrega los estilos para el tablero, botones y diseño general

#### `src/index.js`
Simplifica el archivo para evitar errores:

```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import Game from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <Game />
  </React.StrictMode>
);
```

#### `src/index.css`
Agrega estilos globales y el fondo degradado

### 4. Ejecutar la aplicación

```bash
npm start
```

La aplicación se abrirá automáticamente en `http://localhost:3000`

## 📂 Estructura del proyecto

```
tic-tac-toe/
├── node_modules/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── App.js          # Lógica principal del juego
│   ├── App.css         # Estilos del tablero y componentes
│   ├── index.js        # Punto de entrada de React
│   └── index.css       # Estilos globales
├── package.json
└── README.md
```

## 🎯 Cómo jugar

1. El jugador **X** siempre comienza
2. Haz clic en cualquier casilla vacía para hacer tu jugada
3. Los jugadores se alternan entre **X** y **O**
4. El primero en conseguir 3 en línea (horizontal, vertical o diagonal) gana
5. Usa el historial en el panel derecho para volver a jugadas anteriores

## 🧩 Componentes principales

### `Square`
Representa cada casilla individual del tablero. Recibe el valor (X, O o null) y la función onClick.

### `Board`
Renderiza el tablero de 3x3 con 9 componentes Square. Maneja los clics y determina el estado del juego.

### `Game`
Componente principal que gestiona:
- Historial de movimientos
- Estado actual del juego
- Navegación temporal (volver a jugadas anteriores)

### `calculateWinner`
Función que verifica todas las combinaciones ganadoras posibles y retorna el ganador o null.

## 🔧 Solución de problemas

### Error: "Can't resolve './reportWebVitals'"
Simplifica el archivo `src/index.js` como se muestra en la sección de instalación.

### El servidor no inicia
```bash
# Detén el servidor con Ctrl + C y vuelve a iniciar
npm start
```

### Cambios no se reflejan
El servidor de desarrollo recarga automáticamente. Si no funciona, guarda los archivos de nuevo o reinicia el servidor.

## 🌟 Tecnologías utilizadas

- **React 18** - Librería de JavaScript para construir interfaces de usuario
- **React Hooks** - useState para manejar el estado
- **CSS3** - Estilos modernos con flexbox y transiciones
- **JSX** - Sintaxis que combina JavaScript y HTML

## 📝 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia MIT.

## 👨‍💻 Autor

Creado como proyecto de aprendizaje de React.js

---

¡Disfruta jugando! 🎉