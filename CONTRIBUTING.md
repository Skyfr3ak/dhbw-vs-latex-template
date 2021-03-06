# Contributing guidelines

* run `npm install` to setup [commitizen](https://github.com/commitizen/cz-cli) and [commitlint](https://github.com/conventional-changelog/commitlint) in order to comply with the [conventional commits specification](https://www.conventionalcommits.org)!
* Update the [full example](./examples/full/full.tex) if you add a new feature.
* Rebuild all PDF examples if you change something that causes visual changes.
* Add documentation when you add a new feature.
* Update [patches.md](./docs/patches.md) if you introduce non-backwards-compatible changes.
* If you add an alternative template (`.def`) file:
  * Use the `\dhbwGet*` command to access data.
  * Wrap optional data points in `\ifdef{\dhbwGet*}{true code}{false code}`.
  * Test your template with weird user input (very long titles, missing subtitles etc.)
  * Add a `/.is choice`-type entry to the options of `udhbwvst.cls` to select the new template (e.g. `title-page-style` with choices `default` and `verycool`). The [pgfkeys manual](http://mirrors.ctan.org/graphics/pgf/base/doc/pgfmanual.pdf) may be helpful here.
  * For new title page templates: Make using a non-disclosure notice optional with `\ifbool{udhbwvst@if@print@ndn}{true code}{false code}`.
* Add a VSCode snippet if you add a new command.
* Write your code in english.

❤ Thank you!
