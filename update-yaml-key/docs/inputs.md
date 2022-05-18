# StepInputs Schema

```txt
undefined
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                             |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------- |
| Can be instantiated | Yes        | Unknown status | No           | Forbidden         | Forbidden             | none                | [inputs.schema.json](../out/inputs.schema.json "open original schema") |

## StepInputs Type

`object` ([StepInputs](inputs.md))

# StepInputs Properties

| Property                                 | Type     | Required | Nullable       | Defined by                                                                                     |
| :--------------------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------- |
| [VALUES\_FILE](#values_file)             | `string` | Required | cannot be null | [StepInputs](inputs-properties-values_file.md "undefined#/properties/VALUES_FILE")             |
| [YAML\_KEY](#yaml_key)                   | `string` | Required | cannot be null | [StepInputs](inputs-properties-yaml_key.md "undefined#/properties/YAML_KEY")                   |
| [NEW\_VALUE](#new_value)                 | `string` | Required | cannot be null | [StepInputs](inputs-properties-new_value.md "undefined#/properties/NEW_VALUE")                 |
| [working\_directory](#working_directory) | `string` | Optional | cannot be null | [StepInputs](inputs-properties-working_directory.md "undefined#/properties/working_directory") |

## VALUES\_FILE

Target values file to update

`VALUES_FILE`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [StepInputs](inputs-properties-values_file.md "undefined#/properties/VALUES_FILE")

### VALUES\_FILE Type

`string`

## YAML\_KEY

The YAML Key to update

`YAML_KEY`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [StepInputs](inputs-properties-yaml_key.md "undefined#/properties/YAML_KEY")

### YAML\_KEY Type

`string`

## NEW\_VALUE

The new value of the YAML Key

`NEW_VALUE`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [StepInputs](inputs-properties-new_value.md "undefined#/properties/NEW_VALUE")

### NEW\_VALUE Type

`string`

## working\_directory

Working directory to run commands from

`working_directory`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [StepInputs](inputs-properties-working_directory.md "undefined#/properties/working_directory")

### working\_directory Type

`string`

### working\_directory Default Value

The default value is:

```json
"."
```

# StepInputs Definitions
