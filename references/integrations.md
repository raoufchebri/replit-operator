# Integrations

Use integrations to connect a Replit workspace with external tools and services, then attach an authorized integration to a project where Agent can apply it to one or more artifacts. Integration availability, authorization state, permissions, and project usage can change.

## Scope model

- A **workspace** contains projects, routines, conversations, settings, and shared resources. Enabling an integration in workspace Settings authorizes that external service for use from the workspace; it does not by itself modify a project or artifact.
- A **project** can contain multiple artifacts, such as a website, mobile app, design, slides, or another generated output. It also owns project-level services such as integrations, databases, domains, deployments, and secrets.
- To use a workspace-enabled connector in a project, attach it from the project composer or another live project integration entry point, then state the project outcome explicitly. Agent may modify the relevant artifact, but the connector is associated with the project rather than conceptually belonging only to that artifact.
- The observed composer path is **Add attachment (+) → Add an integration → select the connector**. The connector appears as a pill in the composer; include an explicit request such as adding OAuth with Clerk before sending.
- **Tools → Integrations** shows integrations used in the current project and links to the broader catalog. After Agent implements a connector-backed feature, verify whether the connector appears in this project list; do not assume project attachment succeeded from workspace `Active` status alone.
- Specialized project services may offer another valid entry path. For example, **Users & Auth** can start an authentication setup through Agent, while the composer path makes the chosen connector and requested implementation explicit.
- In the observed Clerk run, workspace Settings showed Clerk as `Active`, attaching it in the project composer successfully produced a working protected OAuth experience, but Clerk did not subsequently appear in **Integrations used in this app** and **Users & Auth** still showed the generic Replit setup entry. Treat those management panels as separate signals: verify connector-backed behavior in Preview and code/tests, and report any catalog or status mismatch instead of inferring failure or success from one panel alone.

## Discovery workflow

1. Confirm the intended workspace.
2. Open the workspace Settings surface and locate Integrations using live UI evidence.
3. Wait briefly for the settings dialog and catalog controls to render. Do not infer failure from an early home-screen snapshot.
4. Verify the Integrations heading, view selector, and search control are visible before continuing.
5. Choose either the full integration catalog or the list of already-added integrations.
6. Search or inspect without connecting, authorizing, or changing configuration.
7. Report the visible integration name, authorization state, and next action required.

## Existing integrations view

Use **Your integrations** to inspect the workspace's current integration state. Verify the selected view before reporting results.

- Classify each visible integration as active, disconnected, or ready to sign in.
- Record its displayed default permission and connected-app scope when present.
- Use **Manage integration** only after confirming the user wants to change that integration.
- The view can expose **Add MCP server**. Treat this as a configuration action, not discovery.

## Connection workflow

1. Identify the integration, destination account, data it may access, and actions it may perform.
2. Explain the external effect and obtain confirmation immediately before beginning authorization or connection.
3. For a custom MCP server, also identify its endpoint, authentication method, tools it exposes, and whether any tool can write or transmit data.
4. After user approval, complete the supported connection flow.
5. Verify the integration appears in the intended workspace and report the visible connection state.

## Custom MCP server workflow

1. Select **Add MCP server** only for approved discovery or setup work.
2. Verify the setup surface distinguishes a personal server from a workspace-wide server.
3. Inspect the required display name, MCP server URL, advanced settings, and **Test & Save** control.
4. Before entering a URL, secret, or authentication detail, explain what will be shared with the server and obtain explicit confirmation.
5. Test and save only after the user approves the exact server and scope.
6. Verify the server's displayed scope and connection state after saving.

## Guardrails

- Never assume the catalog size or a particular integration is available.
- Never connect, sign in, authorize OAuth, add credentials, or add a custom MCP server without explicit approval.
- Treat exact menus and labels as volatile; verify them from the live interface.
