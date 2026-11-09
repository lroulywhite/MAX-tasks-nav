# Explore the Tasks page: interactive walkthrough

A short, top-level walkthrough of the Tasks page in MomentusMAX. A screen sits on the left and short, large-print notes sit on the right, in the same layout as the Today's Focus, Opportunity page, and Calendar walkthroughs.

## What learners do

- Start on an overview and select a numbered area on the screen, or use Next and Back.
- On Task list, select Status, Urgency, or System generated to see where each one is.
- On Search and filters, select Search, Urgency, Status, or Source to see each menu.
- On Task details, select Details, Description and files, or Take action.

Steps: Overview, Task list, Search and filters, Task details, New task.

## Repo contents

| Path | Purpose |
| --- | --- |
| `index.html` | The walkthrough. Screens, scripts, and styles are inlined. The only external request is Google Fonts, which falls back to system fonts |
| `.nojekyll` | Tells GitHub Pages to serve the file as is |
| `.gitignore` | Standard ignores |

## Run locally

Open `index.html` in a browser.

## Publish with GitHub Pages

1. Push to `main`.
2. In the repo, go to Settings > Pages, choose Deploy from a branch, then `main` and `/ (root)`.
3. The page is served at `https://<user>.github.io/<repo>/`. Suggested repo name: `MAX-tasks-nav`.

## Embed in Genially or 360Learning

The page is responsive. Give it as much room as you can, ideally a full slide.

```html
<iframe src="https://<user>.github.io/<repo>/" title="Explore the Tasks Page Walkthrough" width="100%" height="100%" style="border:0;width:100%;height:100%;" allowfullscreen loading="lazy"></iframe>
```

Test in Genially's Preview or published view. Embeds can look blank in the editor.

## How it was built

The five screens are lossless renders of five saved snapshots of the Tasks page (task detail, New Task form, and the Urgency, Status, and Source menus). Only the screen as captured is shown. Nothing was redrawn.

Real-looking names in the snapshots were replaced with fictional ones before rendering: the meeting names in the task list, the assignee, and the Created By username in the New Task form. The replacement list is at the top of the build script and is easy to extend.

To change notes, edit the `STEPS` array in `index.html`. To change a screen, use a new approved capture. Do not edit the embedded images.

## Sources for the notes

| Step | Source |
| --- | --- |
| Task list | Labels on the captured screen. The sparkle meaning comes from its tooltip, "System generated" |
| Search and filters | The filter menus in the captures: Urgency (All, High, Medium, Low), Status (All, New, In Progress, Overdue, Done, Dismissed), Source (All, System, Manual) |
| Task details | Labels on the captured task detail |
| New task | Labels on the captured New Task form |

## Before you publish

- Product to confirm the inferred behavior: that selecting a status or urgency pill changes it, and that Manual tasks are the ones people create. The captures show the pills as interactive and the form shows Source: Manual, but neither is shown in use.
- Product or Security must confirm the demo data is mock, including opportunity names such as Conference and Dental Symposium.
- This file contains captures of the MomentusMAX interface and is Momentus internal training content. Keep the repo private unless Momentus approves public sharing. No license is granted. All rights reserved by Momentus Technologies.
