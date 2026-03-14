```bash
# Download:
# https://github.com/openclaw/openclaw/blob/main/docker-compose.yml
# https://github.com/openclaw/openclaw/blob/main/docker-setup.sh

# Start setup:
OPENCLAW_IMAGE=ghcr.io/openclaw/openclaw:latest sh docker-setup.sh
# It will generate
# - ~/.openclaw
# - .env

# Input when setup:
# Model name for OpenRouter: openrouter/x-ai/grok-4-fast
# Choose Telegram channel, create bot by chatting with @BotFather

# After setup:
# 1. openclaw.json: change gateway.bind to "lan"
docker compose restart
# 2. Chat with bot by clicking in message of @BotFather
# Approve pairing
docker compose exec -it openclaw-gateway bash
openclaw pairing approve telegram <codeFromChat>
# 3. Dashboard: http://localhost:18789
# Must approve device otherwise it keeps display "pair required"
openclaw devices approve <requestId> # get request id from `devices/pending.json`
```