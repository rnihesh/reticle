### Fixed

- **`@reticlehq/server` — `reticle open` on a machine with no browser launcher now points at a Reticle-owned browser.** In a container or on CI, `xdg-open` is missing, `open` failed with `spawn xdg-open ENOENT`, and the only advice was to open the url yourself or set a default browser, neither of which exists there. The recovery text now names `reticle_lease` for an agent and `npx @reticlehq/server drive <url>` for a shell, both of which open the app in the daemon's headless browser. Closes [#1271](https://github.com/reticlehq/reticle/issues/1271).
