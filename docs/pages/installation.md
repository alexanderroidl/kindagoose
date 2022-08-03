# Installation

To install `kindagoose`, you need to execute one of these simple commands:

#### NPM

```shell
$ npm i kindagoose
```

#### Yarn

```shell
$ yarn add kindagoose
```

However, for the module to work you also need the following packages:

* `@nestjs/common`: `>=9.0.0`
* `@nestjs/core`: `>=9.0.0`
* `@typegoose/typegoose`: `>=9.11.0`
* `mongoose`: `>=6.5.0`
* `reflect-metadata`: `>=0.1.13`

In total, the install command should look like this (It is assumed you have already installed the packages `@nestjs/common`, `@nestjs/core` and `reflect-metadata` of the latest versions in your `NestJS` project):

#### NPM

```shell
$ npm i kindagoose @typegoose/typegoose mongoose
```

#### Yarn

```shell
$ yarn add kindagoose @typegoose/typegoose mongoose
```