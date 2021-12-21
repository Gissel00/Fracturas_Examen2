# Heroku link
https://appfacturas00.herokuapp.com/

# gets con filtros
1)
https://appfacturas00.herokuapp.com/facturas?filter=%7B%0A%20%20%22include%22%3A%20%5B%0A%20%20%20%20%7B%0A%20%20%20%20%20%20%22relation%22%3A%20%22detalleFacturas%22%2C%0A%20%20%20%20%20%20%22scope%22%3A%20%7B%0A%20%20%20%20%20%20%20%20%22offset%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22limit%22%3A%202%2C%0A%20%20%20%20%20%20%20%20%22skip%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22order%22%3A%20%22precio%20ASC%22%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%5D%0A%7D%0A

2)
https://appfacturas00.herokuapp.com/productos?filter=%7B%0A%20%20%22offset%22%3A%200%2C%0A%20%20%22limit%22%3A%20100%2C%0A%20%20%22skip%22%3A%200%2C%0A%20%20%22order%22%3A%20%22nombre%20ASC%22%2C%0A%20%20%22include%22%3A%20%5B%0A%20%20%20%20%7B%0A%20%20%20%20%20%20%22relation%22%3A%20%22detalleFacturas%22%2C%0A%20%20%20%20%20%20%22scope%22%3A%20%7B%0A%20%20%20%20%20%20%20%20%22offset%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22limit%22%3A%202%2C%0A%20%20%20%20%20%20%20%20%22skip%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22order%22%3A%20%22precio%20DESC%22%2C%0A%20%20%20%22where%22%3A%20%7B%0A%20%20%20%20%20%20%20%20%20%20%22cantidad%22%3A%20%7B%22between%22%3A%5B5%2C80%5D%7D%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%5D%0A%7D%0A

3)
https://appfacturas00.herokuapp.com/detalle-facturas?filter=%7B%0A%20%20%22include%22%3A%20%5B%0A%20%20%20%20%7B%0A%20%20%20%20%20%20%22relation%22%3A%20%22producto%22%2C%0A%20%20%20%20%20%20%22scope%22%3A%20%7B%0A%20%20%20%20%20%20%20%20%22offset%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22limit%22%3A%205%2C%0A%20%20%20%20%20%20%20%20%22skip%22%3A%200%2C%0A%20%20%20%20%20%20%20%20%22order%22%3A%20%22cantidad%20ASC%22%0A%20%20%20%20%20%20%7D%0A%0A%20%20%20%20%7D%2C%0A%7B%0A%20%20%20%20%20%20%22relation%22%3A%20%22factura%22%2C%0A%20%20%20%20%20%20%20%22fields%22%3A%20%7B%22cliente%22%3Atrue%2C%22rtn%22%3Afalse%7D%0A%20%20%20%20%7D%0A%20%20%5D%0A%7D

# facturas

This application is generated using [LoopBack 4 CLI](https://loopback.io/doc/en/lb4/Command-line-interface.html) with the
[initial project layout](https://loopback.io/doc/en/lb4/Loopback-application-layout.html).

## Install dependencies

By default, dependencies were installed when this application was generated.
Whenever dependencies in `package.json` are changed, run the following command:

```sh
npm install
```

To only install resolved dependencies in `package-lock.json`:

```sh
npm ci
```

## Run the application

```sh
npm start
```

You can also run `node .` to skip the build step.

Open http://127.0.0.1:3000 in your browser.

## Rebuild the project

To incrementally build the project:

```sh
npm run build
```

To force a full build by cleaning up cached artifacts:

```sh
npm run rebuild
```

## Fix code style and formatting issues

```sh
npm run lint
```

To automatically fix such issues:

```sh
npm run lint:fix
```

## Other useful commands

- `npm run migrate`: Migrate database schemas for models
- `npm run openapi-spec`: Generate OpenAPI spec into a file
- `npm run docker:build`: Build a Docker image for this application
- `npm run docker:run`: Run this application inside a Docker container

## Tests

```sh
npm test
```

## What's next

Please check out [LoopBack 4 documentation](https://loopback.io/doc/en/lb4/) to
understand how you can continue to add features to this application.

[![LoopBack](https://github.com/loopbackio/loopback-next/raw/master/docs/site/imgs/branding/Powered-by-LoopBack-Badge-(blue)-@2x.png)](http://loopback.io/)
