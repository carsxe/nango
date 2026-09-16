# CarsXE → Nango public catalog

Staging copies of the **provider-only** CarsXE integration for Nango.

These files were drafted on Allen's workspace machine against a clone of [`NangoHQ/nango`](https://github.com/NangoHQ/nango) (`master` at `9c8e9e2`, release `0.71.8`). They were **not** originally in this repo — [`carsxe/nango`](https://github.com/carsxe/nango) was an empty stub (`README.md` + `.gitignore`) until this commit.

The contribution target is still a PR to **NangoHQ/nango**, not a CarsXE-side Nango client. Copy these paths into a fork of Nango when opening `feat(integrations): add CarsXE`.

## Scope (v1)

- CarsXE **REST** API at `https://api.carsxe.com`
- Auth: `API_KEY` injected as the `key` query parameter
- Connection verification: `GET /v1/auth/validate`
- Proxy only — no syncs, actions, or webhooks
- MCP (`https://mcp.carsxe.com/mcp`, `X-API-Key`) is out of scope

## Files

| Path | Role |
| --- | --- |
| [`packages/providers/carsxe.yaml`](packages/providers/carsxe.yaml) | Provider block to insert in Nango's `packages/providers/providers.yaml` (alphabetically between `canva-scim` and `cdw`) |
| [`docs/api-integrations/carsxe.mdx`](docs/api-integrations/carsxe.mdx) | Nango docs page |
| [`docs/api-integrations/carsxe/connect.mdx`](docs/api-integrations/carsxe/connect.mdx) | Connect UI guide |
| [`docs/snippets/generated/carsxe/PreBuiltUseCases.mdx`](docs/snippets/generated/carsxe/PreBuiltUseCases.mdx) | Empty pre-built syncs/actions |
| [`docs/snippets/generated/carsxe/PreBuiltTooling.mdx`](docs/snippets/generated/carsxe/PreBuiltTooling.mdx) | Tooling status table |
| [`packages/webapp/public/images/template-logos/carsxe.svg`](packages/webapp/public/images/template-logos/carsxe.svg) | 62×62 template logo |
| [`docs/catalog-inserts.md`](docs/catalog-inserts.md) | `docs.json` + `api-catalog.txt` insertion notes |

## Do not commit secrets

A live CarsXE key was used only for an in-memory `GET /v1/auth/validate` and `/specs` check. It is **not** in this repository. Rotate the key if it was pasted in chat.
