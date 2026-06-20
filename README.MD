# recycling-se-icons

Custom icon set for Home Assistant based on the official recycling symbols from the EUpicto / Sveriges Sorterar system.

The purpose of this project is to make the official recycling symbols available for use in Home Assistant without modifying the symbols themselves.

## Features

- Official recycling symbols
- Home Assistant custom icon set
- Human-friendly aliases
- Lightweight JavaScript implementation
- Works with card-mod and standard Lovelace cards

## Installation

Copy:

```text
recycling-se.js
```

to:

```text
/config/www/
```

Add the resource:

```yaml
frontend:
  extra_module_url:
    - /local/recycling-se.js?v=1
```

Restart Home Assistant.

## Usage

Examples:

```yaml
icon: recycling-se:mat
icon: recycling-se:plast
icon: recycling-se:restavfall
icon: recycling-se:pappersforpackningar
```

### Available aliases

| Alias | Symbol |
|---------|---------|
| mat | matavfall |
| plast | plastforpackningar |
| rest | restavfall |
| pappersforpackningar | pappers_forpackningar |
| glas | ofargade_glasforpackningar |
| fargat_glas | fargade_glasforpackningar |
| metall | metallforpackningar |
| batteri | batterier |
| elektronik | smaelektronik |
| ljuskalla | ljuskallor |
| farligt | farligt_avfall |
| tradgard | tradgardsavfall |
| tidning | tidningar |

## Example

```yaml
type: entities
title: Sophämtning
entities:
  - entity: sensor.nasta_matavfall
    icon: recycling-se:mat

  - entity: sensor.nasta_plast
    icon: recycling-se:plast

  - entity: sensor.nasta_restavfall
    icon: recycling-se:rest

  - entity: sensor.nasta_papper
    icon: recycling-se:pappersforpackningar
```

## Symbol Source

The recycling symbols originate from the EUpicto recycling symbol system and are distributed in Sweden through Sveriges Sorterar.

The symbols are used for their intended purpose and are not modified regarding:

- shape
- proportions
- meaning
- naming

For information about the recycling symbol system:

- https://www.sverigesorterar.se
- https://www.eupicto.com

## Rights and Attribution

This repository contains a technical conversion of the official recycling symbols for Home Assistant.

The JavaScript code, build scripts and documentation are licensed under the MIT License.

The recycling symbols themselves remain the property of their respective rights holders.

Project documentation shall clearly state:

- the origin of the symbols
- the intended purpose of the symbols
- the rights holders of the symbols

## Acknowledgements

Special thanks to:

- EUpicto
- Avfall Sverige
- Cirkulær Danmark
- KIVO
- Samband

for maintaining and promoting a common recycling symbol system.

## Disclaimer

This project is not affiliated with, endorsed by, or maintained by EUpicto, Sveriges Sorterar or Avfall Sverige.

It is an independent community project intended to improve integration with Home Assistant.
