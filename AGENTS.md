# AGENTS.md

- The whole app is `index.html`: inline CSS and JS, no build, no dependencies, no tests. Keep it that way.
- The parser (`parse()` in `index.html`) relies on the copied Proton Meet chat layout. A message header is three lines: initials, then name, then time. The meeting footer is found by the `H:MM:SS` call timer, and the line above the timer is the meeting title. "Joined/Left" notices are only matched against that title.
- Test changes by opening `index.html` in a browser and pasting a real chat export.
- `.github/workflows/publish.yml` deploys only `index.html` to GitHub Pages from a tag (run by hand). If a new file has to be served, add it to the workflow's `cp` step.
