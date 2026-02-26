# CodexBar Android 🎚️

Android port of [CodexBar](https://github.com/steipete/CodexBar) — shows AI coding tool usage stats on your phone.

## Features

- 📊 **Usage meters** for Session, Weekly, and Monthly windows
- 🔄 **Auto-refresh** every 2 minutes
- 🌙 **Dark/light theme** following system preference
- 🔐 **Secure storage** for API keys via Android DataStore
- 🎨 **Material 3** design with animated meters

## Supported Providers

| Provider | Auth Method |
|----------|-------------|
| 🤖 Claude | Anthropic API Key |
| ⚡ OpenAI Codex | OpenAI API Key |
| ✦ Cursor | Session Token (cookie) |
| ♊ Gemini | Google API Key |
| 🐙 GitHub Copilot | Personal Access Token |
| 🔀 OpenRouter | API Key |
| 🪁 Kiro | API Key |
| 🔷 Vertex AI | OAuth Token + Project ID |

## Build Instructions

### Requirements
- Android Studio Hedgehog or newer
- Android SDK 34
- Java 17 / Kotlin 1.9

### Steps

1. Clone / extract this project
2. Open in Android Studio: `File → Open → CodexBarAndroid/`
3. Wait for Gradle sync
4. Click ▶ Run or `Build → Generate Signed APK`

### Command line

```bash
cd CodexBarAndroid
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

## Setup

1. Launch the app
2. Tap **Settings** (⚙️ top right)
3. Toggle each provider ON
4. Enter your API key / token
5. Go back → tap 🔄 Refresh

## Getting Credentials

### Claude
Visit [console.anthropic.com](https://console.anthropic.com) → API Keys

### OpenAI Codex  
Visit [platform.openai.com/api-keys](https://platform.openai.com/api-keys)

### Cursor
1. Log in to [cursor.com](https://cursor.com)
2. Open browser DevTools → Application → Cookies
3. Copy `WorkosCursorSessionToken` value

### Gemini
Visit [aistudio.google.com/apikey](https://aistudio.google.com/apikey)

### GitHub Copilot
1. Go to [github.com/settings/tokens](https://github.com/settings/tokens)
2. Create a token with `copilot` scope

### OpenRouter
Visit [openrouter.ai/settings/keys](https://openrouter.ai/settings/keys)

### Vertex AI
```bash
gcloud auth print-access-token
```
Note: expires every hour

## License

MIT — Based on CodexBar by [steipete](https://twitter.com/steipete)
