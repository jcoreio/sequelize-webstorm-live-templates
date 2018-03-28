# sequelize-webstorm-live-templates

WebStorm Live Templates for defining and flow typing Sequelize models

# Installation

1. Copy the text of [templates.xml](`templates.xml`)
2. Open the WebStorm Preferences
3. Go to **Live Templates**
4. Select the **JavaScript** section
5. Paste
6. Install `flow-typed` definitions for `sequelize`

# Templates

### `sequelize-model` (`Model` class file template)

Creates an `export default class $MODEL_NAME$ extends Model` declaration.

#### Variables

##### `$MODEL_NAME$`: the name of the model class
##### `$INIT_ATTRIBUTES$`: the flow types for attributes required at creation time
##### `$ATTRIBUTES$`: the flow types for all other attributes

## Associations

Make sure to `import {Association} from 'sequelize'` when using these.

### `sequelize-bt` (`BelongsTo` association field declaration)

Expand this template inside of a `Model` class definition.
Make sure use the `sequelize-imports-bt` template at top level to import the necessary flow types.

#### Variables

##### `$TARGET$`: the name of the association field
##### `$SOURCE_MODEL$`: the source model identifier
##### `$TARGET_MODEL$`: the target model identifier
##### `$PRIMARY_KEY$`: the flow type of the target model's primary key

### `sequelize-h1` (`HasOne` association field declaration)

Expand this template inside of a `Model` class definition.
Make sure use the `sequelize-imports-h1` template at top level to import the necessary flow types.

#### Variables

##### `$TARGET$`: the name of the association field
##### `$SOURCE_MODEL$`: the source model identifier
##### `$TARGET_MODEL$`: the target model identifier
##### `$PRIMARY_KEY$`: the flow type of the target model's primary key

### `sequelize-hm` (`HasMany` association field declaration)

Expand this template inside of a `Model` class definition.
Make sure use the `sequelize-imports-hm` template at top level to import the necessary flow types.

#### Variables

##### `$TARGET_SINGULAR$`: the singular name of the association field
##### `$TARGET_PLURAL$`: the plural name of the association field
##### `$SOURCE_MODEL$`: the source model identifier
##### `$TARGET_MODEL$`: the target model identifier
##### `$PRIMARY_KEY$`: the flow type of the target model's primary key

### `sequelize-btm` (`BelongsToMany` association field declaration)

Expand this template inside of a `Model` class definition.
Make sure use the `sequelize-imports-btm` template at top level to import the necessary flow types.

#### Variables

##### `$TARGET_SINGULAR$`: the singular name of the association field
##### `$TARGET_PLURAL$`: the plural name of the association field
##### `$SOURCE_MODEL$`: the source model identifier
##### `$TARGET_MODEL$`: the target model identifier
##### `$THROUGH_MODEL$`: the through model identifier
##### `$PRIMARY_KEY$`: the flow type of the target model's primary key

