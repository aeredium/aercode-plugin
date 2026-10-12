# aercode: the AEREDIUM code policy doorway for Claude Code

This plugin is the fitting of the doorway on your machine: a hook that asks the doorway before every tool call Claude Code makes, under your organisation's policy, and stops the call when the doorway says so. Every verdict carries a signed receipt. The plugin carries no policy, no rule and no key: the policy is your organisation's, held at the doorway; your credential lands on your machine when you sign in, and never in this plugin. It declares no server to Claude Code: the model does not hold the judge's tools; the hook is the fitting.

What is in it: the hook (`bin/aercode-hook`), the person's command (`bin/aercode`), the doorway's address (`doorway`, the one setting, fixed when the plugin was built), and the hooks it registers (`hooks/hooks.json`: every tool call, 960 seconds, block on failure; the verifier at the start of a session, on startup and on resume; the close at its end).

After installing, sign in once on each machine: in a terminal, run `aercode login`; your browser opens the doorway's sign-in page; paste the invitation code from the email your organisation sent you, or your owner key; allow the one scope. You hold one credential per machine. Then start Claude Code inside a clone of a project your organisation assigned you. `aercode verify` says in one sentence where you stand; `aercode uninstall` removes the plugin and your credential and says the machine is no longer governed.

The full guide is docs/plugin.md of github.com/aeredium/code-policy-engine.
