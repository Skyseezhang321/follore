# Follore for Claude

[Follore](https://follore.com) is a place to publish columns that people subscribe to, and personal posts in your own space. This plugin connects Claude to your Follore account and adds a skill for writing the piece.

## What it adds

- **The `follore-editor` skill.** Turns a conversation with Claude, or your own notes, into an article, an edited Q&A or an edited dialogue, with a title, a summary and a Markdown body, plus a private editor's note on what was cut, removed and left unverified. It keeps who said what straight, removes keys and private details, and does not publish anything by itself.
- **The `follore` connection** to `https://follore.com/mcp`, with seven tools:
  - `identity` tells you what your connection may do and which columns you run.
  - `space` returns the address of your public space.
  - `column_brief` and `recent_items` read a column's brief and what it has already reported, so a new issue does not repeat the last one.
  - `submit_issue` files an issue of a column you run. It goes through that column's own review settings.
  - `create_post` saves an article to your space as a private draft.
  - `publish_post` makes a saved post public. It needs publishing permission on your connection, and publishing sends the title and summary to your subscribers.

## Signing in

Claude asks you to sign in to Follore when it first connects. You choose what the connection may do, and you can remove it at any time from Connected apps on the Agents & API page of your Follore workspace. The plugin has no API key to paste and stores no credential.

## What it sends, and where

- Claude calls `https://follore.com/mcp` only when you ask it to use Follore. What reaches Follore is what you asked it to save or file: a title, a summary and a body, or the name of a column to read.
- The editor's note stays in your conversation. It is never sent.
- The plugin contains no scripts, hooks or executables, runs nothing on your machine, and contacts no other address. It does not read credentials from your environment.
- The skill in this plugin does not fetch anything: it carries no instruction to read a web address or to replace itself, and it is updated only by installing a newer version of the plugin. (The copy of the skill that Follore serves on its own site does carry such an instruction, for assistants that keep a saved copy; this plugin leaves it out.)

## License

Released under the MIT License.

## Links

- [How to connect](https://follore.com/mcp-guide)
- [Support](https://follore.com/contact)
- [Privacy policy](https://follore.com/legal/privacy)
- [Terms of service](https://follore.com/legal/terms)
