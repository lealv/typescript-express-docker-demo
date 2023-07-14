# typescript-express-docker-demo

## Packages needed
```npm install express```  
```npm install @types/express --save-dev```  
```npm install typescript --save-dev```

## Create tsconfig.json
```npx tsc --init```

## tsconfig.json setup
```"rootDir": "./src",```
```"outDir": "./dist",```

# Dev mode
## Auto rebuild
```npm install ts-node-dev --save-dev```  
Setup package.json to use
```
"scripts": {
  "dev": "ts-node-dev src/index.ts"
},
```

## Run
```npm run dev```

## Run as docker container
```docker compose -f docker-compose.dev.yml up```

# Prod mode
```
"scripts": {
  "dev": "ts-node-dev src/index.ts",
  "build": "tsc",
  "start": "npm run build && node dist/index.js"
},
```  
```npm run start```
## Run as docker container
```docker compose up```