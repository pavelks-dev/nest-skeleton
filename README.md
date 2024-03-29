<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

<p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>

## Установка

```bash
$ npm install
```

## Запуск

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Тесты

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Миграции

С миграциями необходимо работать через typeorm cli. Поэтому его необходимо сначала установить npm i -g typeorm, либо запускать через npx typeorm <params> без установки.

### Создание миграций для существующей сущности (Entity)

```bash
# Generate a migration from existing table schema
typeorm migration:generate -n User
```

### Запуск миграций

Чтобы запустить миграции необходимо сначала скомпилировать ts файлы в js. И после этого запускать, поскольку команды migration:run и migration:revert работают только с файлами .js

```bash
# Compile migrations ts files
tsc

# Run migrations
typeorm migration:run
```

## Лицензия

Nest is [MIT licensed](LICENSE).
