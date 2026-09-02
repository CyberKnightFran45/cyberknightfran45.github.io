# PvZ2CHotUpdate

Same idea as `translations`, but now JSON files are delivered instead of
text: push a file, GitHub builds and hosts it, the game fetches it
live.

Content is split into variants -- a plain folder name under `raw/`, one per
cheat strength (`default`, `max_level`, ...). Each variant is a full,
self-contained bundle; which one a build points at is just which
`JsonUpdateServerConfig` URL its `SERVERCONFIG.rton` carries.

Each variant carries both platforms: `raw/<variant>/ad/<cv>/` (Android) and
`raw/<variant>/ios/<cv>/` (iOS). Android and iOS run on their own separate
version numbers, so their `<cv>` folders are usually different -- that's
expected, not a mismatch to fix.

**Original repo made by evilhack28**
