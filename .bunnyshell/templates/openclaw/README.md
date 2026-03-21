# OpenClaw - Bunnyshell Template

Bunnyshell environment template for [OpenClaw](https://github.com/openclaw/openclaw), a personal AI assistant with a web gateway UI.

## What's Included

- **OpenClaw** pre-installed globally via npm
- Web gateway UI exposed on port 18789
- Persistent `/root/.openclaw` config volume (5Gi)
- IP whitelisting via Bunnyshell security

## Access

- **Gateway UI**: `https://gateway-<env.base_domain>/`
- **Shell**: `bns exec <COMPONENT_ID> --tty --stdin`

## Environment Variables

| Variable | Description |
|----------|-------------|
| `OPENCLAW_TOKEN` | Your OpenClaw authentication token |

## Deploy

```bash
bns environments create \
  --from-path bunnyshell.yaml \
  --name "openclaw" \
  --project <PROJECT_ID> \
  --k8s <CLUSTER_ID>

bns environments deploy --id <ENV_ID>
```
