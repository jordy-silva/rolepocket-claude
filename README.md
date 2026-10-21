# RolePocket for Claude

This is RolePocket's direct-distribution marketplace for Claude. It contains one plugin, **RolePocket**, with career-context, saved-job assessment and application-preparation workflows.

**Compatibility preview:** Claude compatibility is still being verified, including account connection and document delivery. This plugin is not listed in Anthropic's directory or endorsed by Anthropic.

## Before you start

- A paid Claude plan with plugin access is required for Claude chat or Cowork. Organization policies may require administrator approval.
- Connected job workflows require a RolePocket account with workspace access. RolePocket and Claude subscriptions are separate.
- Provide your career-context document or CV to the Claude conversation when needed. Installing the plugin does not give it access to your local files or previous chats.
- Application preparation requires a Claude environment that can create DOCX files, review their text, render every page and deliver the result. If those capabilities are unavailable, the workflow must remain a draft.

## Install from this marketplace

1. Open Claude, then **Customize > Plugins > Add > Add marketplace**. In Cowork, open Cowork first, then Customize.
2. Choose **Add from a repository** and paste `https://github.com/jordy-silva/RolePocket-claude`.
3. Find **RolePocket** in the added marketplace and select **Add** or **Install**, as shown by your client.
4. Open the plugin and confirm it contains three skills and a RolePocket connector. The connection target is `https://rolepocket.com/mcp`.
5. Open its **Connectors** tab, choose RolePocket and connect your account. Review the requested permissions before approving them.

Adding the marketplace and installing the plugin are separate steps. Installing the plugin also does not sign you in to RolePocket.

RolePocket supports OAuth automatic client registration. If Claude asks which OAuth client to use, choose **Register automatically**. Do not enter a personal API key or client secret. If authentication fails, stop and share the visible error through [support](https://rolepocket.com/support/), without including passwords, tokens or authorization codes.

## Verify the account and try a first task

Start a fresh conversation with RolePocket available and ask:

> Which RolePocket account is connected, and what can this connection do? Do not change anything.

Check that the response matches the account you intended to connect. A familiar display name alone may not distinguish two accounts. If uncertain, verify the account shown in RolePocket before continuing.

Attach your career-context file and ask:

> Use this career-context document to preview how my saved RolePocket jobs fit. Do not save recommendations or change any jobs.

If you need a career-context document first, provide your CV and ask:

> Help me build a reusable career-context document from this CV. Ask me about any missing facts.

Once you have reviewed the preview, you can explicitly ask Claude to save a recommendation for a selected job. For application preparation, select a specific job and ask for a DOCX CV. Claude must deliver and inspect the document before recording completed preparation in RolePocket. You submit applications yourself through the employer.

## Updates and disconnecting

New versions are published in this repository. Check the installed version against `plugins/rolepocket/.claude-plugin/plugin.json` and use Claude's marketplace controls to check for updates. Automatic updates have not yet been verified, so please check your installed version before relying on a new release.

To stop RolePocket account access, open **Connected assistants** in RolePocket and revoke the relevant Claude connection. Remove or disable the plugin in Claude if you also want to stop using its skills. Removing a plugin should not be treated as proof that the server-side authorization was revoked.

## If something is missing

- **No marketplace:** confirm that you pasted the repository URL above, and check whether your organization permits that repository.
- **No RolePocket plugin:** adding a marketplace does not install its plugins. Open the marketplace and add RolePocket.
- **Skills but no connector:** contact support with your Claude app version and plugin version so we can help complete your setup.
- **Connection works but no jobs appear:** check the RolePocket account, workspace access and requested queue. Do not switch to someone else's account.
- **No rendered DOCX:** keep the result as a draft. Complete preparation must not be recorded until delivery and inspection succeed.

Please keep CVs, career documents, account details and credentials out of public GitHub issues. Use the support page for account-specific help.

[Support](https://rolepocket.com/support/) | [Privacy](https://rolepocket.com/privacy/) | [Terms](https://rolepocket.com/terms/)

For more help with Claude itself, see [Claude plugin installation](https://support.claude.com/en/articles/13837440-use-plugins-in-claude) and [custom connector authentication](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).
