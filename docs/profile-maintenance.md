# Profile maintenance

`README.md` is the public profile. `terminal.svg` is the terminal header; edit its text directly to update the introduction.

## Generated images

The **Update Profile Assets** workflow (`.github/workflows/snake.yml`) generates light and dark contribution snakes and a GitHub stats card. The card uses public statistics through the automatic `GITHUB_TOKEN`; no personal access token or external hosting is needed.

The workflow runs daily at 00:17 UTC (05:47 IST), on pushes to `main`, and manually from the Actions tab. Pull requests generate and validate images for review without publishing them. Download the `profile-assets` artifact from a successful run to preview all three SVGs.

Only successful runs on `main` publish to the existing `output` branch. Publishing uses a normal Git push and preserves branch history and other files. The README loads images from that branch, so a failed generation leaves the last successful images available. Keep the `output` branch in place.

To refresh manually, open **Actions → Update Profile Assets → Run workflow**, select `main`, and run it. Check both the `generate` and `publish` jobs. GitHub's image cache can take time to show a newly published image.

If publishing fails with HTTP 403, check that repository or organization policies allow the workflow's explicit `contents: write` permission and that branch rules allow the Actions bot to update `output`. The generation job only needs read access. The workflow does not force-push.

## Project links

Stockroom and Student Admin Dashboard are marked in progress until public repository URLs and accurate descriptions are available. Replace those lines when ready. Demo and live links are maintained by the project teams; LinkedIn can block automated link checks even when a link works in a browser.
