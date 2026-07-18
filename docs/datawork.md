[简体中文](./datawork.zh-CN.md) · [← Back to README](../README.md)

# Use DeepSeek V4 with DataWork

DataWork is a local-first personal AI Agent system for Windows. It provides
general agents, a code agent, memory, todos, notes, Python automation, plugins,
and MCP tools within a single local workspace.

DeepSeek V4 models (`deepseek-v4-flash` and `deepseek-v4-pro`) are supported
through DataWork's built-in DeepSeek provider, with streaming, thinking mode,
reasoning effort control, and tool calling.

## 1. Install DataWork

- **Repository**: <https://github.com/jkjoker/datawork>
- **Download**: <https://publish.obsidian.md/xm/wiki/%E6%95%99%E7%A8%8B/datawork%EF%BC%9Aabout>

Download the latest installer (`datawork_setup.exe`), extract if needed,
and run it. DataWork runs on **Windows 10 and above**. No registration or
login required.

## 2. Get a DeepSeek API key

1. Open <https://platform.deepseek.com/api_keys>.
2. Sign in and create an API key.
3. Copy your key and keep it private.

## 3. Configure the model

1. Launch DataWork and open **设置 / Settings** → **模型管理 / Model Management**.
2. Fill in:

| Field | Value |
|---|---|
| Provider | `deepseek` |
| Model Name | `deepseek-v4-pro` or `deepseek-v4-flash` |
| Base URL | `https://api.deepseek.com/chat/completions` |
| API Key | Your DeepSeek API key |

When `deepseek` is selected, the Base URL is pre-filled automatically.
Click `添加模型 / Add` to save.

## 4. Create an Agent

1. Open **Settings** → **General Agent** → **Agent Management**.
2. Enter a name, select the DeepSeek model you just added, set permissions,
   and click **Add Agent**.

The Agent is now ready to use in the main AI tab (Expert / Code modes),
in the Coder editor, or via the built-in web server.

In **Expert** mode, select the Agent, choose reasoning depth (`High` / `Max`),
and send a message to start.

## Additional features

DeepSeek V4 integration in DataWork also supports:

- **Thinking mode**: enable via **Tips** → **Conversation Features** →
  **Thinking Mode**.
- **Reasoning effort**: the bottom bar shows `High` / `Max` when the
  model supports it.
- **1M context window**: both V4 models are registered with a 1M-token
  budget.
- **MCP tool calling**: the Agent can call configured tools over multiple
  rounds.
- **Code Agent**: switch to `Code` mode for coding tasks.

## Links

- DataWork: <https://github.com/jkjoker/datawork>
- DeepSeek API keys: <https://platform.deepseek.com/api_keys>
- DeepSeek API docs: <https://api-docs.deepseek.com/>
