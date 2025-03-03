---
id: 'index'
title: '@jersmart/automapper-core'
slug: '/api/core/'
sidebar_label: 'README'
sidebar_position: 0
custom_edit_url: null
---

# @jersmart/automapper-core

This is the core package that will handle mapping configurations and mapping operations.

## Installation

```sh
npm i @jersmart/automapper-core
```

or with `yarn`

```sh
yarn add @jersmart/automapper-core
```

## Usage

`@jersmart/automapper-core` exposes `createMapper()` method to create a `Mapper` object with a accompany `MappingStrategy` (read more
about [Strategies](#Strategies))

`createMapper` accepts a `CreateMapperOptions` object with the following shape:

```ts
export interface CreateMapperOptions {
    strategyInitializer: MappingStrategyInitializer<MetadataIdentifier>;
    errorHandler?: ErrorHandler;
    namingConventions?: NamingConventionInput;
}
```

Read more about usage on [documentation site](https://automapperts.netlify.app/docs/api/create-mapper)

## Strategies

A given Mapper is accompanied by a Strategy by providing `strategyInitializer` when using `createMapper()`.

A Strategy will be responsible for:

-   Discover metadata (eg: `classes` uses `@AutoMap()` decorator to discover the metadata of the properties on the Classes)
-   Retrieve metadata: how the metadata should be retrieved from the discovery phase (eg: `classes` discovers and stores the metadata to `Reflect`, retrieve metadata simply gets them from `Reflect`)
-   Apply metadata: how the metadata is applied to the Model

`@automapper` provides the following official strategies:

-   `@jersmart/automapper-classes`: Work with TS/ES6 classes.
-   `@jersmart/automapper-pojos`: Work with Interfaces/Types along with POJOs. In projects that do not make use of Class, `pojos`
    can be used instead.
-   `@jersmart/automapper-mikro`: Work together with TS/ES6 classes along with [MikroORM](https://github.com/mikro-orm/mikro-orm)
-   `@jersmart/automapper-sequelize`: Work together with TS/ES6 classes along with [Sequelize](https://github.com/sequelize/sequelize)
