# Solar System Extension Specification

- **Title:** Solar System
- **Identifier:** <https://stac-extensions.github.io/solarsystem/v1.0.0/schema.json>
- **Field Name Prefix:** ssys
- **Scope:** Item, Catalog, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/README.md#extension-maturity):** Proposal
- **Owner**: @jlaura

This document explains the fields of the STAC Solar System (SSYS) Extension to a STAC Item, Catalog, or Collection. 
SSYS covers data sets that represents an individual image, mosaic, or derived raster of a planetary body. Examples 
of SSYS data include sensors with visible, short-wave and mid-wave IR bands (e.g., the THEMIS instrument on Mars 
Odyssey), visible images (e.g. Context Camera (CTX) aboard Mars Global Surveyor), or derived data sets like digital 
elevation models (DEM/DTM).

- Examples:
- [Catalog Example (Europa Galileo SSI Image)](examples/catalog.json)
- [Collection Example (Europa Galileo SSI Image)](examples/collection.json)
- [Item Example (Europa Galileo SSI Image)](examples/item.json)
- [SSYS JSON Schema](json-schema/schema.json)

## Item Properties

| Field Name      | Type        | Description |
| --------------- | ----------- | ----------- |
| ssys:targets    | \[string\]    | Array to hold list of target bodies (e.g. Mars, Moon, Earth) |
| ssys:local_time  | string      | Lexicographically sortable time string (e.g., 01:115:12.343) |

### Additional Field Information

#### ssys:targets

the field `ssys:targets` allows to have one or more targets listed within an array of strings. This can 
happen, for example, if several moons are in the same view. As an example, this scene has both of Ganymede
and Jupiter in the same image as taken by the NASA mission Cassini [PIA02862](https://photojournal.jpl.nasa.gov/catalog/PIA02862).

#### ssys:local_time

the field `ssys:local_time` allows for API searchable non-UTC time definitions. The time should be encoded in a 
string that is lexicographically sortable. For Mars, it is recommended that this time take the form `MarsYear:Sol:LocalTime`.

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.
