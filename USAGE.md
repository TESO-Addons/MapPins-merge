### Installation

1. First of all you need to install `node` and `docker`
2. Run command `yarn bootstrap` - this is a required step!

### Developer commands
| Command | Description |
| --- | --- |
| `yarn dev` | Start package in dev mode |
| `yarn dev --scope=client` | Start client in dev mode |
| `yarn dev --scope=server` | Start server in dev mode |
| `yarn test` | Tests |
| `yarn lint` | Linter |
| `yarn format` | Prettier |
| `yarn build` | Production build |

### Vercel auto deploy
Register the account [vercel](https://vercel.com/)

Follow [instructions](https://vitejs.dev/guide/static-deploy.html#vercel-for-git)

As `root directory` define `packages/client`

### Production in docker

`docker compose up` - starts three services:
1. "client" with nginx, distributing client statics
2. "server"
3. "postgres"

If you need only one service then specify it command:

`docker compose up {sevice_name}`, example: `docker compose up server`

If you need to rebuild service use command:

`docker compose build {sevice_name}`
