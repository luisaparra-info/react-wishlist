Práctica LMSGI
1. Dependencias 
    1. Instalar NodeJS (nvm)
    2. Instalar npm (nvm)
    3. Crear la carpet del proyecto
    4. Iniciar el proyecto (npm init)
    5. Instalar React en el proyecto
        (npm install --save react)
        (npm install --save react-dom)
2. Enpaquetado
    1. Instalar parcel (npm install --save-dev parcel-bundler)
    2. Crear un index.html simple
    3. Definir un script "start" en package.json
    4. Ejercutar start script npm start
    5. Primera prueba react con index.jsx
3. Estructura de carpetas
    * carpeta del proyecto/
        * src/ (Código fuente que nosotros escribimos)
            * (Folder by type)
            * (Folder by feature)
        * dist/ (Resultado de la compilación)
        * node_modules/ (Dependencias)
        * package.json
        * .archivos_configuuracion
4. Linting
Revisa en código en búsqueda de errores de código o estructura. Herramienta: eslint
    1. Instalar eslint: npm install -g --save-dev eslint
    2. eslint --init
    3. Añadir script:     "lint": "eslint --fix \"*.{js,jsx}\""
    4. Cambiar fichero .eslintrc.json 
        {
            "extends":  "airbnb",
            "env":{
                "browser":true
            },
            "rules":{
                "linebreak-style": "off"
            }
        }
        https://www.npmjs.com/package/eslint-config-airbnb (solucionar dependencias)
    5. Probar lint: npm run lint
    6. Instalar Husky: npm install --save-dev lint-staged husky
    7. Configurar packaje.json
    "husky": {
        "hooks":{
            "pre-commint": "lint-staged"
            }
    },
    "lint-staged":{
        "*.{js,jsx}": ["npm run lint"]
    }
5. Formato

    1. Instalar Prettier: npm install --save-dev prettier
    2. Añadir script "format" y reglas a package.json








