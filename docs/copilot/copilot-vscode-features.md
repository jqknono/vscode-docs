---
Order: 2
Area: copilot
TOCTitle: Copilot Cheat Sheet
ContentId: de6f9f68-7dd5-4de3-a210-3db57882384b
PageTitle: GitHub Copilot in VS Code cheat sheet
DateApproved: 03/05/2025
MetaDescription: Get a quick overview of the GitHub Copilot features in Visual Studio Code. GitHub Copilot provides AI-powered features to help you write code faster and with less effort.
MetaSocialImage: images/shared/github-copilot-social.png
---
# GitHub Copilot in VS Code cheat sheet

GitHub Copilot in Visual Studio Code provides AI-powered features to help you write code faster and with less effort. This cheat sheet provides a quick overview of the features for GitHub Copilot in Visual Studio Code.

You can access GitHub Copilot in VS Code through the Chat view, directly in the editor, from the integrated terminal, and via AI-powered enhancements in the VS Code user interface.

> [!TIP]
> If you don't yet have a Copilot subscription, you can use Copilot for free by signing up for the [Copilot Free plan](https://github.com/github-copilot/signup) and get a monthly limit of completions and chat interactions.

The team is continuously working on improving Copilot in VS Code and adding new features. Some features are still experimental. Try them out and share your feedback in [our issues](https://github.com/microsoft/vscode-copilot-release/issues).

## Chat with GitHub Copilot

Use natural language to chat with GitHub Copilot and get help with coding tasks. For example, ask Copilot to explain a block of code or a programming concept. Get more information about using [Copilot Chat](/docs/copilot/copilot-chat.md).

| Action | Description |
|--------|-------------|
| `kb(workbench.action.chat.open)` | Open the **Chat view** and start a chat conversation with Copilot by using natural language. |
| `kb(workbench.action.chat.openEditSession)` | Open the **Copilot Edits view** and start a code editing session across multiple files. |
| `kb(workbench.action.quickchat.toggle)` | Open **Quick Chat** and ask a quick question to Copilot. |
| `kb(inlinechat.start)` | Start **Inline Chat** to send a chat request to Copilot directly from the editor. Use natural language or use `/` commands to give instructions to Copilot. |
| <i class="codicon codicon-mention"></i> | Type `@` in chat or select <i class="codicon codicon-mention"></i> to view the list of *chat participants*, which are domain experts that can help you in a specific area. Extensions can also contribute additional participants.<br/>Example: `@workspace how is auth implemented?`  |
| Participant detection _(Experimental)_ | Copilot Chat can also automatically route your question to the appropriate participant. [Get more info](https://code.visualstudio.com/updates/v1_93#_automatic-chat-participant-detection-in-chat-view-experimental). |
| `/` | Invoke a *slash command* to prompt for commonly used actions, such as explaining a block of code, generating tests or documentation. |
| `/explain` | Ask Copilot to explain a block of code or a programming concept. |
| <i class="codicon codicon-history"></i> | Select this icon in the Chat view to access your history of chat sessions. |
| <i class="codicon codicon-mic"></i> | Enter a chat prompt by using speech (voice chat). The chat response is read out aloud. |

> **Tips**
>
> - Use `/` commands and `@` participants to get more precise and relevant answers.
> - Be specific, keep it simple, and ask follow-up questions to get the best results.
> - Provide context by attaching files, symbols, or selections to your chat prompt.

## Code editing session

Use Copilot Edits to start a code editing session where you can iterate quickly on AI-generated code edits that are applied directly across multiple files in your workspace.

| Action | Description |
|--------|-------------|
| `kb(workbench.action.chat.openEditSession)` | Open the **Copilot Edits view** and start a code editing session across multiple files. |
| <i class="codicon codicon-plus"></i> | Start a new edit session. |
| Edit/Agent mode | Switch between edit mode and [agent mode (preview)](/docs/copilot/copilot-edits.md#use-agent-mode-preview) for Copilot Edits. |
| `Add Files...` | Attach files as context for editing. |
| `Accept` | Accept all current edits. |
| `Discard` | Discard all current edits. |
| <i class="codicon codicon-diff-multiple"></i> | View all edits in a multi-file diff editor. |
| <i class="codicon codicon-discard"></i> | Undo the last edit. |
| <i class="codicon codicon-redo"></i> | Redo the last edit. |
| <i class="codicon codicon-eye"></i> | Enable/disable attaching the active editors as context. |

> **Tips**
>
> - Add all files for which you want to get edits to your prompt.
> - Be specific and precise about the changes you want Copilot Edits to make.
> - If you have a larger task, decompose it in smaller tasks and iterate often.

## Generate code from chat

Copilot can generate code blocks in response to your chat prompts. Quickly apply the generated code in your project or insert it in a new file. For example, ask Copilot to optimize an algorithm in your code.

| Action | Description |
|--------|-------------|
| <i class="codicon codicon-git-pull-request-go-to-changes"></i> | Smart-apply the generated code block in the active editor. |
| <i class="codicon codicon-insert"></i> | Insert the generated code block at the cursor. |
| <i class="codicon codicon-copy"></i> | Copy the generated code block to the clipboard. |
| <i class="codicon codicon-terminal"></i> | Insert the generated code block in the terminal as a shell command. |
| `Insert into New File` | Insert the generated code block in a new file. |

> **Tips**
>
> - Provide details about the framework or libraries to use.
> - Consider creating [custom code-generation instructions](#customize-ai-code-generation).

## Attach context to your prompt

When you send a chat prompt to Copilot, you can attach context to help Copilot understand your question better. For example, add the current editor selection, a file, or a symbol to your chat prompt. Get more information about [best practices for using Copilot](/docs/copilot/prompt-crafting.md).

| Action | Description |
|--------|-------------|
| Attach <i class="codicon codicon-attach"></i> (`kb(workbench.action.chat.attachContext)`) | Open a Quick Pick to select relevant context for your chat prompt. Choose from different context types, such as workspace files, symbols, current editor selection, terminal selection, and more. |
| <i class="codicon codicon-eye"></i> | Enable/disable attaching the active editors as context. |
| `Prompts...` _(Experimental)_ | Add reusable prompt instructions to your request. Get more information about [prompt files](/docs/copilot/copilot-customization.md#reusable-prompt-files-experimental). |
| Drag & drop file | Drag & drop a file or editor tab onto the chat to attach the file as context. |
| Drag & drop folder | Drag & drop a folder onto the chat to attach the files within it as context. |
| Drag & drop problem | Drag & drop an item from the **Problems** panel to attach it as context. |
| Recent files _(Experimental)_ | Automatically include recently opened and edited files in your chat prompt. [Get more info](https://code.visualstudio.com/updates/v1_93#_use-recent-coding-files-as-inline-chat-context-experimental).  |

### Chat variables

Use chat variables in your chat prompt to reference context that is relevant to your question.

| Chat variable | Description |
|--------|-------------|
| `#changes` | The list of source control changes. |
| `#codebase` | Add relevant workspace content as context to your prompt. |
| `#editor` | Add the visible contents of the active editor as context for your prompt. |
| `#file` | Open a Quick Pick to select a file from your workspace and add it as context for your prompt. |
| `#<filename>` | Type `#`, followed by a filename, to get filename suggestions for workspace files and attach as context. |
| `#folder` | Type `#folder:`, followed by a folder name to select a folder from your workspace and add it as context for your prompt. Adding a folder adds all files within it as context. |
| `#problems` | Add workspace issues and problems from the **Problems** panel as context. Useful while fixing code or debugging. |
| `#selection` | Add the current editor selection as context to your prompt. |
| `#sym` | Open a Quick Pick to select a symbol from your workspace and add it as context for your prompt. |
| `#<symbol>` | Type `#`, followed by a symbol name, to get symbol suggestions for workspace files and attach as context. |
| `#terminalSelection` | Add the current terminal selection as context to your chat prompt. |
| `#terminalLastCommand` | Add the last run terminal command as context to your chat prompt. |
| `#testFailure` | Add test failure information as context. Useful when running and diagnosing [tests](/docs/debugtest/testing.md). |
| `#VSCodeAPI` | Add the VS Code API as context to your prompt to ask questions related to VS Code extension development. |

## Copilot in the editor

As you're coding in the editor, you can use Copilot to generate code completions as you're typing. Invoke Inline Chat to ask questions and get help from Copilot, while staying in the flow of coding. For example, ask Copilot to generate unit tests for a function or method. Get more information about [code completions](/docs/copilot/ai-powered-suggestions.md) and [Inline Chat](/docs/copilot/copilot-chat.md#inline-chat).

| Action | Description |
|--------|-------------|
| Code completions | Start typing in the editor and Copilot provides code suggestions that match your coding style and take your existing code into account. |
| Code comments | Provide a code completion prompt to Copilot by writing instructions in a code comment.<br/>Example: `# write a calculator class with methods for add, subtract, and multiply. Use static methods.` |
| Next Edit Suggestions _(Preview)_ | Predict your next code edit with Copilot Next Edit Suggestions. Enable Copilot NES with the `setting(github.copilot.nextEditSuggestions.enabled)` setting. Learn how to get started with [Copilot NES](/docs/copilot/ai-powered-suggestions.md#next-edit-suggestions-preview). |
| `kb(inlinechat.start)` | Start **Inline Chat** to send a chat request to Copilot directly from the editor. Use natural language or use `/` commands to give instructions to Copilot. |
| Prompt from the editor _(Experimental)_ | Start typing natural language directly in code and Copilot detects that you're not writing code but prompting, and will automatically start Inline Chat for your prompt. |
| `kb(editor.action.rename)` | Get AI-powered suggestions when renaming symbols in your code. |

> **Tips**
>
> - Use meaningful method or function names to get better code completions quicker.
> - Select a code block to scope your Inline Chat prompt or attach relevant context by attaching files or symbols.
> - Use the editor context menu options to access common Copilot actions directly from the editor.

## Customize AI code generation

Define [custom instructions](/docs/copilot/copilot-customization.md#custom-instructions) to help Copilot generate code or review code that matches the coding style, tools, and developer workflow of your team or project.

With reusable prompt files, you can specify common prompt instructions and relevant content in a Markdown file (`*.prompt.md`), that you can then reuse in your chat prompts.

| Action | Description |
|--------|-------------|
| File-based instructions | Define shared instructions for code generation in a `.github/copilot-instructions.md` file in your workspace. These common instructions supplement your own personal code-generation instructions.  |
| Code-review instructions _(Preview)_ | Define instructions for using Copilot to review an editor selection in settings or import from a file. You can define language-specific instructions. |
| Code-generation instructions _(Experimental)_ | Define instructions for code generation with GitHub Copilot in settings or import from a file. You can define language-specific instructions. |
| Test-generation instructions _(Experimental)_ | Define instructions for test generation with GitHub Copilot in settings or import from a file. You can define language-specific instructions. |
| Commit-message generation instructions _(Experimental)_ | Define instructions for commit message generation with GitHub Copilot in settings or import from a file. You can define language-specific instructions. |
| Pull request title and description generation instructions _(Experimental)_ | Define instructions for pull request title and description generation with GitHub Copilot in settings or import from a file. You can define language-specific instructions. |
| Reusable prompt files _(Preview)_ | Define reusable prompt instructions with additional context in Markdown files and use them for your chat prompts. Learn how to [create reusable prompt files](/docs/copilot/copilot-customization.md#reusable-prompt-files-preview).  |

> **Tips**
>
> - Define language-specific instructions to get more accurate generated code for each language.
> - Store your instructions in a file to easily share them with your team and across projects.

## Review code (experimental)

Copilot can do a quick review pass of a code block or perform a review of uncommitted changes in your workspace. Review feedback shows up as comments in the editor, where you can apply the suggestions.

| Action | Description |
|--------|-------------|
| **Review and Comment** _(Preview)_ | Select a block of code, and select **Copilot** > **Review and Comment** from the editor context menu for quick review pass.  |
| **Copilot Code Review** | Select the **Copilot Code Review** button in the Source Control view for a deeper review of all uncommitted changes. Join the [waitlist](https://gh.io/copilot-code-review-waitlist). |

## Generate tests

Copilot can generate tests for functions and methods in your codebase. Get more information about [slash commands in Chat](/docs/copilot/copilot-chat.md#slash-commands).

| Action | Description |
|--------|-------------|
| `/tests` | Generate tests for all or only the selected methods and functions in the editor. The generated tests are appended in an existing tests file or a new tests file is created.  |
| `/setupTests` | Get help setting up a testing framework for your code. Get recommendation for a relevant testing framework, steps to set up and configure it, and suggestions for VS Code testing extensions.   |
| `/fixTestFailure` | Ask Copilot for suggestions on how to fix failing tests. |
| Test coverage _(Experimental)_ | Generate tests for functions and methods that are not yet covered by tests. [Get more information](https://code.visualstudio.com/updates/v1_93#_generate-tests-based-on-test-coverage-experimental). |

> **Tips**
>
> - Provide details about the testing frameworks or libraries to use.

## Generate documentation

Generate code documentation for functions and methods in your codebase. Get more information about [slash commands in Chat](/docs/copilot/copilot-chat.md#slash-commands).

| Action | Description |
|--------|-------------|
| `/docs` | Generate documentation comments for all or only the selected methods and functions in the editor.  |

## Debug and fix problems

Use Copilot to help fix coding problems and to get help with configuring and starting debugging sessions in VS Code.

| Action | Description |
|--------|-------------|
| `/fix` | Ask Copilot for suggestions on how to fix a block of code or how to resolve any compiler or linting errors in your code. For example, to help fix unresolved Node.js package names. |
| `/fixTestFailure` | Ask Copilot for suggestions on how to fix failing tests. |
| `/startDebugging` _(Experimental)_ | Generate a `launch.json` debug configuration file and start a debugging session from the Chat view. [Get more information](https://code.visualstudio.com/updates/v1_93#_start-debugging-from-chat-experimental). |
| `copilot-debug` command | Terminal command to help you debug your programs. Prefix a run command to start a debugging session for it (for example, `copilot-debug python foo.py`). [Get more information](https://code.visualstudio.com/updates/v1_96#_debugging-with-copilot). |

> **Tips**
>
> - Provide additional information about the type of fix you need, such as optimizing the memory consumption or performance.
> - Watch for Copilot Code Actions in the editor that indicate suggestions for fixing problems in your code.

## Scaffold a new project

Copilot can help you create a new project by generating a scaffold of the project structure, or generate a notebook based on your requirements.

| Action | Description |
|--------|-------------|
| `/new` | Use the `/new` command in the Chat view to scaffold a new project or a new file. Use natural language to describe the type of project/file you need, and preview the scaffolded content before creating it.<br/>Example: `/new Express app using typescript and svelte` |
| `/newNotebook` | Use the `/newNotebook` command in the Chat view to generate a new Jupyter notebook based on your requirements. Use natural language to describe what the notebook should contain.<br/>Example: `/newNotebook get census data and preview key insights with Seaborn`. |

## Source control and issues

Copilot can analyze the changes in your commits and pull requests and provide suggestions for commit messages and pull request descriptions.

| Action | Description |
|--------|-------------|
| Commit | Generate a commit message for the current changes in a source control commit. |
| Pull request | Generate a pull request title and description that correspond with the changes in your pull request. |
| `@github` | Use the `@github` participant in chat to ask about issues, pull requests, and more across your repositories. Get more information about the [available GitHub skills](https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-your-ide#currently-available-skills).<br/>Example: `@github What are all of the open PRs assigned to me?`, `@github Show me the recent merged pr's from @dancing-mona`  |

## Search

Use Copilot to get more relevant search results in the Search view.

| Action | Description |
|--------|-------------|
| Semantic search | Include search results from Copilot in the Search view that are semantically relevant. |

## Terminal

Get help about shell commands and how to resolve errors when running commands in the terminal.

| Action | Description |
|--------|-------------|
| `kb(inlinechat.start)` | Start Inline Chat within the terminal to use natural language to quickly get and run a shell command.<br/>Example: `how many cores on this machine?` |
| <i class="codicon codicon-sparkle"></i> <br/>Fix using Copilot | Select the <i class="codicon codicon-sparkle"></i> icon on a failed shell command and get suggestions on how to resolve the error. |
| <i class="codicon codicon-sparkle"></i> <br/>Explain using Copilot | Select the <i class="codicon codicon-sparkle"></i> icon on a failed shell command and get an explanation about why the command failed. |
| `@terminal` | Use the `@terminal` participant in the Chat view to ask questions about the integrated terminal or shell commands.<br/>Example: `@terminal list the 5 largest files in this workspace` |
| `@terminal /explain` | Use the `/explain` command in the Chat view to explain something from the terminal.<br/>Example: `@terminal /explain top shell command` |

## Python and Notebook support

You can use Copilot Chat to help you with Python programming tasks in the Native Python REPL and in Jupyter notebooks.

| Action | Description |
|--------|-------------|
| <i class="codicon codicon-sparkle"></i> Generate<br/>`kb(inlinechat.start)` | Start Inline Chat in a notebook to generate a codeblock or Markdown block. |
| `#` | Attach variables from the Jupyter kernel in your chat prompt to get more relevant responses. |
| Native REPL + `kb(inlinechat.start)` | Start Inline Chat in the Native Python REPL and run the generated commands. |

## VS Code commands and APIs

You can use Copilot to get help about VS Code features, settings, and the VS Code extension APIs. Get more information about [chat participants](/docs/copilot/copilot-chat.md#chat-participants).

| Action | Description |
|--------|-------------|
| `@vscode` | Use the `@vscode` chat participant to ask questions about VS Code by using natural language.<br/>Example: `@vscode how to enable word wrapping?` |
| `@vscode /runCommand` | Use `/runCommand` with the `@vscode` chat participant to run a VS Code command.<br/>`@vscode /runCommand enable developer mode` |
| `@vscode /search` | Use `/search` with the `@vscode` chat participant to generate a VS Code search.<br/>Example: `@vscode /search python files without imports` |

> **Tips**
>
> - Use the `#vscodeAPI` chat variable if you're asking about the VS Code extension API.

## Next steps

- [Tutorial: Get started with GitHub Copilot in VS Code](/docs/copilot/getting-started.md)
