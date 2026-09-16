# Catalog inserts for NangoHQ/nango

Apply these in a fork of [`NangoHQ/nango`](https://github.com/NangoHQ/nango), not as standalone files.

## `docs/docs.json`

In the `900+ APIs & Integrations` group, insert alphabetically between `canvas-lms` and `cdw`:

```json
              "api-integrations/carsxe",
```

## `docs/api-catalog.txt`

Bump `Provider count` by 1, then insert this row after `canvas-lms`:

```
| `carsxe` | CarsXE | API_KEY | [docs](https://nango.dev/docs/api-integrations/carsxe.md) | [connect](https://nango.dev/docs/api-integrations/carsxe/connect.md) |  | other |
```

## `docs/llms.txt`

Bump the catalog slug count in the API catalog line by 1 (1008 to 1009 on `9c8e9e2`).
