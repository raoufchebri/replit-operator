# Project tools

Use this reference when operating inside a Replit project. Preserve the separation between drafting a plan, applying code changes, previewing a build, and releasing it.

## Build, Preview, and Plan

- Build view contains the project composer, Preview, and Tools. The composer is similar to the new-conversation composer and includes a Plan checkbox; the observed shortcut is Command-I. Verify the live shortcut and label.
- Plan mode is for a scoped implementation proposal. State the goal, constraints, expected checks, and that the plan should wait for approval before changing code.
- Verify the returned plan's outcome, out-of-scope items, files, and acceptance checks before execution. A plan can be viewed, revised, cancelled, built in the current session, or built in the background; labels are volatile.
- A background build becomes a separate task. It can return to a review/apply state before its changes reach the main project. After applying it, return to the default Build view with Agent chat on the left and Preview on the right. Use Preview to exercise the result in the main version, and consult the Agent chat for the implementation summary, reported checks, warnings, or follow-up needs before declaring the feature complete.
- After a task is applied, Replit can show suggested next tasks in the chat. Starting one launches a background task immediately; inspect its proposed purpose and record that it was started, but do not treat it as applied or complete until its review/apply flow finishes.
- In the expanded project entry in the main navigation, an active task appears as a child item beneath the project. The same entry exposes **New Task** for project-scoped work and **Open Board** for the task board. Creating a task can change project state; viewing the board is read-only.
- These project-only controls are not shown for ordinary conversations or routines. In the observed navigation, routine entries have a chat-and-clock treatment, conversations have a chat treatment, and projects use a distinct project icon. Treat iconography as a live visual cue, not a stable API.
- A project task can be opened without applying it; its Plan view exposes a reviewable proposal with View, Start Building, Revise, and Cancel. An active planning task marks the project as working in the navigation.
- The project board provides task navigation and a Kanban-style task board. Verify the live columns and task states before making workflow decisions; the taught state model is Draft, Active, Ready, and Done.
- While viewing a task, project publishing may be unavailable. Return to the main project before opening release controls.

## Project tools map

The observed Tools pane groups cloud services and setup services. Verify the current labels and availability rather than relying on this list.

| Service | Purpose | Change boundary |
| --- | --- | --- |
| Publishing | Release a version, access controls, scans, monitoring, analytics, feedback, advanced deployment settings | Approval before publishing, access, costs, or permanent geography choices |
| Domains | Add or manage custom domains | Approval before purchase, connection, or DNS changes |
| Monitoring | Traffic, request metrics, resource usage, analytics | Read-only before enabling paid or notification settings |
| Growth | SEO and growth opportunities | Approval before any changes to public metadata/content |
| Database | Development/production data configuration | Approval before provisioning, migrating, or exposing data |
| Users & Auth | Project authentication | Approval before provider setup or user-access changes |
| Security Center | Project-scoped vulnerability/privacy review | Scan is safe; approval before fixes/remediation |
| App Storage | Files and object storage | Approval before provisioning or uploads |
| Integrations | Replit-native and external connections | Approval before authorization, credentials, or connection |
| Git | Version-control connection | Approval before linking, pushing, or changing repository state |
| Secrets | Secure configuration values | Never reveal values; approval before adding, editing, or removing |
| Agent Skills | Project agent capabilities | Approval before enabling, importing, or changing instructions |

## Project tabs and preview chrome

- Prefer the ordinary project layout with the Agent chat beside **Preview**. Keep the persistent **Tools** and **Preview** tabs; close stale plans, boards, and temporary inspection tabs before starting unrelated work.
- Collapse the workspace sidebar when the subject is Agent chat, Preview, Tools, or publishing so the relevant project surfaces have enough room and remain legible in screenshots. Open or pin the sidebar only when its navigation or project controls are part of the instruction or evidence.
- The plus control beside Tools and Preview opens a searchable tool picker. The observed non-staff entries are Tools, Console, Developer, Logs, Shell, User Settings, Validation, VNC, Workflows, Files, and New file. Debug is staff-only. Open tools one at a time and close temporary tabs after inspection.
- **Developer** contains Networking, CPU/memory Resources, and SSH connection/key management. **Logs** exposes live deployment logs with search and display filters. **Shell** is a project terminal. **User Settings** affects personal editor and workspace behavior, not just the current project.
- **Validation** separates configured commands from past runs; adding a command changes project verification behavior. **VNC** requires a compatible running server and forwarded ports. **Workflows** lists run configurations and can create or stop workflows. **Files** searches project paths; **New file** enters file-creation mode. Do not create, stop, or reconfigure anything during read-only discovery.
- **Invite** exposes project-level collaboration. The observed dialog offered a private join link where anyone with the link would receive edit access; never copy or share that link, invite users, or change access without explicit approval.
- After release, Publish becomes **Republish**. The observed dialog summarized publisher, visibility, artifact count, domain, feedback state, and security review. Inspecting is safe; republishing, adding a domain, or changing visibility requires approval.
- **Inbox** surfaces project notifications and task activity. **Library** has Library and Files views, searches project outputs, and offers a New action. In the observed project it listed the Focus Sprint website artifact. Treat creation and file mutations as separate approval-gated actions.
- The artifact selector in Preview identifies the active artifact and type. The observed selector showed `Focus Sprint` as a Website plus **Create something new — Build with Agent**. Selecting an existing artifact is navigation; creating another artifact changes project scope.

### Preview toolbar

- The preview header includes the active artifact selector, Back, Forward, Refresh, the `.replit.dev` preview address/path, Webview logs, Screen size, an external-preview link, and Apply a design system. Verify availability against the live artifact.
- **Webview logs** opens a lower panel with Webview Logs and one or more Server Logs tabs when multiple servers are running. In the observed state the webview had no log entries. Opening and closing logs is read-only.
- **Screen size** provides Full size, 16:9, and named device presets. The observed mobile presets included current iPhone, Pixel, and Samsung Galaxy sizes. Use these for responsive verification, but treat the exact catalog as volatile.
- The external-preview control opens the preview in another tab when enabled. It was disabled in the observed session, so do not claim that a new tab was opened without verifying the live control.
- **Apply a design system** offered **Import from workspace** and **Extract design system**. Inspecting the menu is safe; importing or extracting can change project design assets or styling and requires approval.

## Verified post-publish views

- **Monitoring** separates application monitoring (uptime, requests, HTTP statuses, and duration) from infrastructure monitoring (CPU and memory) and has independent time ranges. It points visitor and user insights to Growth.
- **Growth** shows an SEO rating, an Agent-assisted scan, advanced analytics, and basic traffic metrics such as visitors, pages, referrers, countries, browsers, and devices. Metrics can initially be empty after release.
- **Database** lists project databases and their usage/compute information. Every development environment has a managed development database; ask Agent to persist the desired application data rather than asking it to provision that database or manually running schema migrations.
- For application-owned persistence, describe the records, ownership boundary, migration behavior, and checks in the prompt. Let Replit generate and apply the development schema through its managed task flow. Verify the resulting development tables and app behavior before publishing.
- On Publish or Republish, Replit detects development schema changes, generates and validates migrations, and offers a production database preview or **Approve and publish**. Do not add startup DDL or manually manipulate production. Obtain approval before applying the production migration, then wait through Provision, security checks, database setup, and Promote.
- After a successful release, select **Production Database** in Database and verify the expected tables and row counts independently of the development database. In the verified Focus Sprint run, production was provisioned automatically and the public application schema contained `focus_tasks` and `focus_sessions`, initially with zero rows; the development and production databases had separate capacity figures.
- A selected database has **Overview**, **My Data**, and **Settings**. Overview summarizes tables and row counts. My Data opens read-only by default; editing, SQL Console, Database Studio, schema selection, and schema refresh remain unavailable until editing is explicitly enabled. Do not enable editing for discovery.
- Settings exposes the masked connection variable, storage usage, connection details, recovery, backups, credential rotation, and deletion. Do not reveal or copy connection values. Treat credential regeneration and deletion as destructive. In the verified production state, point-in-time recovery covered the last seven days, while scheduled backups were off and had no backups yet; changing either policy requires approval.
- **Users & Auth** exposes a prebuilt login setup path and provider choices. Starting setup changes user access and requires approval.
- **Security Center** separates scans, active/dismissed findings, Agent-assisted fixes, and additional protection layers. Do not run fixes without approval.
- **App Storage** offers cloud buckets for uploads. Do not create a bucket or upload files without approval.
- **Git** is a project-level version-control surface. Do not link, push, or change repository state without approval.
- **Secrets** supports linking account-level secrets, creating secrets, and configurations. Values are masked; never expose them, and verify that access scope before changing any secret.

## Publishing workflow

For template-based projects, distinguish a Design mockup from a deployable artifact. The top-level **Publish** control is visible in Design, but a project containing only design mockups and reusable libraries has nothing to deploy; the Publishing pane directs the user to ask Agent to build an app from the selected design. After a Website artifact exists, publishing can be initiated from either Design or Build. Verify the artifact list instead of inferring deployability from the presence of the Publish button.

1. Confirm the intended project, preview, and tests. Run the offered security scan and record the result.
2. Verify the subdomain and access mode. Public publishing makes the app reachable by anyone with the URL; password or invite-only modes have different access implications.
3. Review suggested release add-ons individually. In the observed interface, analytics, uptime monitoring, blocking critical vulnerabilities, and a feedback widget are separate controls. Enabling feedback exposes a public submission surface; capture its placement and appearance after enabling.
4. Inspect Advanced settings without changing deployment type, resource allocation, secrets, production data, or geography. The observed geography setting warns that it becomes locked after publishing. Resource and database choices can have cost/data consequences.
5. Obtain explicit approval immediately before the final Publish action unless it has already been explicitly granted for this run. Wait for the publishing stages to complete; a successful pre-publish security check alone is not release completion.
6. Verify the live state, actual public access, the selected add-ons, and any deployment warnings. Keep referral badges off unless the user specifically asks to display them.

## Evidence to record

- When a screenshot teaches a specific control or action, frame it tightly enough that the relevant label, button, and resulting state are immediately legible. Preserve only the surrounding context needed to orient the user; use a wider default-layout capture for whole-workspace concepts.
- Before capturing, remove unrelated chrome: collapse the workspace sidebar unless it is the subject, close temporary project tabs, and keep only the panels needed to explain the step.
- For task creation, keep the project row and **New task** control visible beside the **Plan a new task** composer. For alternate entry paths, center the board popover and its actions. For review, center the Ready card with **Apply** and **Review** instead of relying on a wide board overview.
- Plan scope, verification criteria, and whether code was applied in foreground or background.
- Preview evidence for the requested feature after applying changes.
- Scan status, publishing progress, final release state, access mode, and enabled add-ons.
- Any service that remained unavailable before publication, and any setting deliberately left unchanged because it would affect cost, data, access, or external systems.
