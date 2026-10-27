# Proton Meet Chat Cleaner

Turns a Proton Meet chat copied from the chat panel into a clean log. It strips avatar initials, buttons, the meeting footer, and "Joined"/"Left" notices.

Live: https://weeklydevchat.github.io/proton-meet-chat-cleaner/

## Usage

1. In Proton Meet, select all in the chat panel and copy.
2. Open the [live page](https://weeklydevchat.github.io/proton-meet-chat-cleaner/) (or `index.html` locally) and paste into the left pane.
3. Copy the clean log from the right pane.

Options:

- Remove joined/left notices
- Keep timestamps
- Keep names
- Merge back-to-back messages from the same person
- Output as plain text or Markdown

Everything runs in the browser. Nothing is sent anywhere. Your option choices are saved in `localStorage`.

## Development

The whole app is `index.html`: one file with no build step and no dependencies. Edit it and reload the page.

## Publishing

The site is deployed to GitHub Pages by hand from a tag:

1. Tag the release, e.g. `git tag v2026.2.0 && git push origin v2026.2.0`.
2. Run the **Publish to GitHub Pages** workflow (Actions tab) and give it the tag.

Only `index.html` is published.

Versions are `vYEAR.RELEASE.PATCH`: the year, the release number within that year (starting at 1 each year), and the patch number (e.g. `v2026.2.0`, `v2026.3.1`, `v2027.1.0`).

## License

MIT. See [LICENSE](LICENSE).
