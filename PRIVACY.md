# Privacy

Infinity is a Mac app with no Infinity server. There is no account, no sign-up and no analytics. We (the people who make Infinity) never see your chats, files or keys.

## What stays on your Mac

- **Chats, projects, assistants, automations and settings** are saved in `~/Library/Application Support/Infinity`. Infinity keeps a daily backup of them in `Backups` there (the last 5 days).
- **API keys** are saved in your macOS Keychain. (A build you compile yourself in Xcode, signed only for your Mac, keeps them in a private file in the data folder instead, because the Keychain would ask for your password after every rebuild.)
- **The file search index** (Search your files) is saved in `Index` there. It holds short pieces of text from the folders you chose, so the app can find them by meaning.
- **Images you make** are saved in `Images` there.
- **Crash reports** from macOS are saved in `Crash Reports` there. They're never uploaded. If you want to send one, you attach it yourself.
- **The troubleshooting log** (Settings ▸ Developer) is off by default. When it's on, it records which Codex and Claude Code commands ran and how they ended, never message text, in a temporary file (`plan.log`, which Settings ▸ Developer ▸ Show log finds for you).

Settings ▸ Developer ▸ **Reset Infinity** removes your chats, settings and (if you choose) keys and starts the app from scratch. The old data folder goes to the Trash.

Settings ▸ General ▸ Your data ▸ **Export everything** puts your chats and settings in one zip you can keep or move to another Mac, where **Import an export** brings them back.

## What leaves your Mac, and where to

Only what a feature you use needs:

| When you… | What's sent | To |
|---|---|---|
| Chat with a cloud model | Your messages, attached files and the chat so far | The provider you picked (OpenAI, Anthropic, Google, OpenRouter, etc.), with your key |
| Use your ChatGPT plan | The same | OpenAI, through the Codex app on your Mac |
| Chat with Ollama, LM Studio or Apple Intelligence | Nothing | Stays on your Mac |
| Make an image with a cloud option | Your prompt | OpenAI, Google or ChatGPT (whichever you picked). Image Playground, FLUX.2 and Z-Image run on your Mac |
| Search your files with a cloud option | Pieces of the files you chose | OpenAI. EmbeddingGemma and Apple run on your Mac |
| Use voice with a cloud option | Your recording, or the text to read aloud | OpenAI. Apple voices run on your Mac |
| Download a model | A normal download request | Hugging Face, Ollama or LM Studio |
| Let an agent search the web | The search words | DuckDuckGo |
| Ask for the weather | The place name, then its coordinates | Open-Meteo (open-meteo.com) |
| Check for updates (once a day) | A request for a small file, with no information about you | Wherever the update feed is hosted |
| Install an update | A download of the new version, which Infinity checks is signed by the same developer before installing | The same place |
| Send feedback | Only what you write, the version and Mac details, and the newest crash report, in an email you send yourself | The feedback address |

Each provider's own privacy policy covers what they do with what you send them.

## Things to know while testing

- Infinity Code and assistants can change files and run commands in the folders you give them. At **Auto** they ask before risky commands; at **Full auto** they never ask. Keep a backup of anything important, and see the [terms](TERMS.md).
- Secrets you add to a Code project are saved on your Mac and given to your app as environment variables. They're never sent to a model.
- Deleting a chat moves it to the archive. Delete it from the archive to remove it for good.

Questions: support@ampdynamic.com, or Help ▸ Send Feedback in the app.
