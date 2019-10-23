# Configuração inicial

`create-react-app tdd-jest`
`yarn add react-app-rewired -D` || `npm i --save-dev react-app-rewired`

## Modificar os scripts

```
"scripts": {
"start": "react-app-rewired start",
"build": "react-app-rewired build",
"test": "react-app-rewired test",
}
```

## Remover linhas decódigos que não serão utilizadas

- public
- src

## Criar arquivos

config-overrides.js

```
config package.json:
"jest": {
"testMatch": [
"**/__tests__/**/*.test.js"
],
"setupFilesAfterEnv": [
"@testing-library/react/cleanup-after-each",
"@testing-library/jest-dom/extend-expect"
],
"moduleNameMapper": {
"^~/(.\*)": "<rootDir>/src/\$1"
}
},
```

## Criar Pasta

**tests**

## jsconfig.js

```
{
"compilerOptions": {
"baseUrl": "src",
"paths": {
"~/_": ["_"]
}
}
}
```

## Insira as dependências Dev

npm i --save-dev || yarn add -D

- @testing-library/react
- @testing-library/jest-dom
- @types/jest
- jest-localstorage-mock
- redux react-redux redux-saga
- immer
- axios
- axios-mock-adapter -D
