---
id: 'modules'
title: '@jersmart/automapper-classes'
sidebar_label: 'Exports'
sidebar_position: 0.5
custom_edit_url: null
---

## Interfaces

-   [AutoMapOptions](interfaces/AutoMapOptions.md)

## Variables

### AUTOMAPPER_METADATA_FACTORY_KEY

• `Const` **AUTOMAPPER_METADATA_FACTORY_KEY**: `"__AUTOMAPPER_METADATA_FACTORY__"`

#### Defined in

[lib/keys.ts:1](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/keys.ts#L1)

---

### AUTOMAP_PROPERTIES_METADATA_KEY

• `Const` **AUTOMAP_PROPERTIES_METADATA_KEY**: `"automap:properties"`

#### Defined in

[lib/keys.ts:3](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/keys.ts#L3)

---

### AUTOMAP_STANDALONE_METADATA_KEY

• `Const` **AUTOMAP_STANDALONE_METADATA_KEY**: `"automap:standalone"`

#### Defined in

[lib/keys.ts:4](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/keys.ts#L4)

## Functions

### AutoMap

▸ **AutoMap**(): `PropertyDecorator`

#### Returns

`PropertyDecorator`

#### Defined in

[lib/automap.ts:21](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/automap.ts#L21)

▸ **AutoMap**(`typeFn`): `PropertyDecorator`

#### Parameters

| Name     | Type                                                   |
| :------- | :----------------------------------------------------- |
| `typeFn` | () => `Constructor`<`any`\> \| [`Constructor`<`any`\>] |

#### Returns

`PropertyDecorator`

#### Defined in

[lib/automap.ts:22](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/automap.ts#L22)

▸ **AutoMap**(`options`): `PropertyDecorator`

#### Parameters

| Name      | Type                                             |
| :-------- | :----------------------------------------------- |
| `options` | [`AutoMapOptions`](interfaces/AutoMapOptions.md) |

#### Returns

`PropertyDecorator`

#### Defined in

[lib/automap.ts:25](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/automap.ts#L25)

---

### classes

▸ **classes**(`options?`): `MappingStrategyInitializer`<`Constructor`\>

#### Parameters

| Name      | Type                                |
| :-------- | :---------------------------------- |
| `options` | `MappingStrategyInitializerOptions` |

#### Returns

`MappingStrategyInitializer`<`Constructor`\>

#### Defined in

[lib/classes.ts:14](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/classes.ts#L14)

---

### getMetadataList

▸ **getMetadataList**(`model`): [metadataList: [string, Object][], nestedConstructor: Constructor[]]

#### Parameters

| Name    | Type                  |
| :------ | :-------------------- |
| `model` | `Constructor`<`any`\> |

#### Returns

[metadataList: [string, Object][], nestedConstructor: Constructor[]]

#### Defined in

[lib/get-metadata-list.ts:20](https://github.com/nartc/mapper/blob/efc4cb9d/packages/classes/src/lib/get-metadata-list.ts#L20)
