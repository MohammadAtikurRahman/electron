# Your-App-Name

An Electron application built with React.

## Table of Contents

- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Building the Application for Production](#building-the-application-for-production)

## Installation

### 1. Install the necessary dependencies:

#### npm install

### 2. Install Electron and Electron Builder as development dependencies:

#### npm install --save-dev electron electron-builder

## Running the Application

### 1. Start the React development server:

#### npm start

### 2. In a separate terminal, start the Electron application:

#### npm run start-electron

## Building the Application for Production

### 1. Build the React application:

#### npm run build

### 2. Update the `scripts` section in your `package.json` file:

```json
"scripts": {
    "start": "cross-env BROWSER=none react-scripts start",
    "start-electron": "node start-electron.js",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "electron-start": "electron .",
    "electron-pack": "electron-builder --dir",
    "electron-build": "electron-builder"
}
"build": {
    "appId": "com.example.your-app-name",
    "files": [
        "build/**/*",
        "public/electron.js"
    ],
    "directories": {
        "buildResources": "assets"
    },
    "extraMetadata": {
        "main": "public/electron.js"
    }
}
