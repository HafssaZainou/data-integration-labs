# Lab 4
## Task 1: Setup

| Question | Answer |
| --- | --- |
| Which tool, which version? Which model answered? | Visual Studio Code, chat view in agent mode, version 1.147.0. Model: KI:connect Mistral Small 4 (`mistralai-mistral-small-4-119b-2603`), added in VS Code as a Custom Endpoint with my KI:connect.nrw key. |
| In which permission mode did the tool start, and how did you switch? | Agent mode "Interactive". No permission level was selected at the start. Then I chose `Manual Permissions` in the menu at the bottom of the chat. The menu offers `Manual Permissions`, `Assisted Permissions` and `Allow all` as well as three different agent modes: `Interactive`, `Plan` and `Autopilot`. |
| What did it do without asking: read files, edit files, run commands? | Read files (tool `Read` on the folder). Created `hello.txt` without asking, with the default settings. Ran `git log` without asking, also in Manual mode. |
| How do you see what it changed, and how do you undo it? | The editor shows the changes as a comparison (green = added lines, red = removed lines), and the chat lists "1 file changed +1 -0". I undid the change with *Restore Checkpoint* in the chat. The chat also offers **Keep** and **Undo** buttons, but I did not use them. |
| How do you start a fresh session? Where do you see how full the context window is, and how much of your quota this task used? | New session with the **+** in the chat. The context window is limited to 144K tokens (max context, which I set myself: 128000 input + 16000 output). Clicking the number next to the model name shows only this limit, no fill level, also not in a chat with messages. Quota: I found no usage meter in VS Code or on chat.kiconnect.nrw. The THKI notes say that all requests are attributed to TH Köln, not to individual persons, and the privacy statement mentions a cost element per conversation. According to the tutorial, API calls share the group, token and cost limits of the web interface. |
| Which instruction files does it read? | `AGENTS.md`. Test: I put the line "Always start every answer with the words WINTER IS COMING." into `AGENTS.md`. The answer began with it, also when the file was closed and not attached to the chat. |
| May your prompts and code be used to train models? Which setting controls it, and how did you set it? | I found no statement about model training in the privacy statement (version 2.0, 2025-06-30), the terms of use or the THKI notes (version 4.0, 01.07.2026), and no setting that controls it. The THKI notes say that open models run on servers in Germany/NRW and that, when used through this infrastructure, no data is transferred to the original developers (in my case: Mistral). For the commercial OpenAI models, processing happens "via Microsoft in the EU and globally". There is nothing to set, so I did not change anything. |

### Making it ask before writing

With the default settings, the agent created `hello.txt` without asking: the default of `chat.tools.edits.autoApprove` is `"**/*": true`. I set `"**/*": false` in my **user** `settings.json`. The same line in the workspace `.vscode/settings.json` had no effect (the setting did not appear in the Workspace tab of the settings). After a window reload, the agent asked "Create file?" with the options Allow Once, Allow Edits to hello.txt in this Session, Allow Edits in agent-test in this Session, Always Allow Edits to hello.txt, Always Allow Edits in agent-test and Skip. I chose Skip.

### Plan mode

In plan mode, creating a script failed ("Create File failed"): the agent could only write a plan. It saved it as `plan.md` outside my repository, in a `.copilot` session folder. The plan was larger than my request: three scripts (PowerShell, Python, Bash) and a README. I rejected it.

### Why this tool?

Access and cost: I use Mistral Small 4 through KI:connect.nrw with my TH Köln login, so I need no extra plan.  
Data protection: According to the model overview it is processed exclusively in Germany, and the THKI notes say that no data is transferred to the original developer. I can check this in the documents, which I could not do as clearly for the other tools I considered, including my Claude Pro plan.  
Openness and integration: It is an open model that runs in the Visual Studio Code chat I already use, and the Custom Endpoint lets me switch models if one works badly.  
Team: My partner uses Copilot Fusion, so we use different tools. The lab allows this, and our shared rules will be in `AGENTS.md`.  
Usage limits: The quota is shared and I cannot see my own usage, so I will start a fresh session for each step.