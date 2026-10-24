# UNO Q Hackout Submissions

Submit your Arduino UNO Q apps for your respective hackathon by opening a pull request that adds **only your `<github-username>.zip`** inside your track folder. Include all submission details in the `app.yaml` **inside the ZIP**. 

## Choose your track

### Northeastern Silicon Valley Hackathon

| Track   | Submission folder                                      |
| ------- | ------------------------------------------------------ |
| Arcade  | [`10-24-neu/arcade-track/`](10-24-neu/arcade-track/)   |
| Robocar | [`10-24-neu/robocar-track/`](10-24-neu/robocar-track/) |

Use this structure:

```text
10-24-neu/
├── arcade-track/
│   └── <github-username>.zip
└── robocar-track/
    └── <github-username>.zip
```

- Use the submitting attendee's GitHub username in lowercase. For a team, choose one member to submit on everyone's behalf.
- Name the ZIP **`<github-username>.zip`**, such as `alice-git.zip`, and place it directly in your track folder. GitHub usernames keep submissions distinct.
- Keep the same path when updating your submission. Replace your existing ZIP; do not add dated copies or filenames such as `alice-example-v2.zip`.

Example: `10-24-neu/arcade-track/alice-git.zip`.

## Prepare your app

Before exporting, update `name` and `description` in your app's `app.yaml`. Include the following information in `description` so reviewers can identify your team and run your app from the ZIP alone:

```yaml
name: Pixel Rally
description: |
  Event: NEU SV Hackout
  Track: arcade-track
  Members: Alice Example (@alice-git), Bob Example (@bob-example)
  Summary: A maze racing game controlled with the Modulino joystick.
  Run: Import into Arduino App Lab, select the UNO Q, and run the app.
  Controls: Joystick steers; button A starts or restarts a round.
  Setup and calibration: Describe required hardware settings, dependencies,
    calibration values, and any extra steps needed to reproduce your demo.
  Known limitations: List incomplete features or issues, or write "None".
  Credits: List reused code, assets, models, and their sources, or write "None".
```

Replace the example with your own details, including `robocar-track` if applicable. List every team member and their GitHub handle. Keep the `description: |` indentation shown above.

This is a metadata example, not a replacement for your whole file: **preserve your existing `ports`, `bricks`, `icon`, and any other app configuration**. Do not add separate top-level metadata fields for the submission.

Export your completed app from App Lab and rename the exported archive to `<github-username>.zip`. The ZIP must contain `app.yaml` at its root, together with the code, dependency declarations, assets, and calibration files your app needs. Do not wrap the app in another folder inside the ZIP. For the starter apps, the layout looks like this:

```text
<github-username>.zip
├── app.yaml
├── python/
└── sketch/
```

Check that the final ZIP imports and runs on your UNO Q. Remove credentials, tokens, and other secrets before exporting.

## Open your submission pull request

1. Fork this repository and clone your fork. Create a branch for your submission.
2. Place your `<github-username>.zip` directly inside **your track folder only**.
3. Commit and push that ZIP to your fork. Open a pull request targeting this repository's `main` branch.
4. Use a clear PR title, for example `Arcade Submission: Pixel Rally - @alice-git` or `Robocar Submission - @bob-example`.
5. Check the PR's **Files changed** tab: it must contain **only your submission's ZIP at the correct path**. Do not change the root README, track placeholders, another attendee's files, or files in the other track.

**Your submission is the pull request containing your `<github-username>.zip` in the correct track, with the submission information in its bundled `app.yaml`.** A PR description, issue, external download link, or loose `app.yaml` does not replace the ZIP.

Use one submission per GitHub username per track, and one submitter per team. For corrections while your PR is open, replace the ZIP at the same path and push to the same branch; the PR updates automatically. If it has already merged, open a new PR that replaces only your existing ZIP.
