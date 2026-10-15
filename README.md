# Omabit for Omarchy — 0.1.0-rc.2

Generated installation repository. Authoritative source and issues:
<https://github.com/thelifeandtimes/omabit>. See `DISTRIBUTION.json` for provenance.
Make source changes there; do not hand-maintain this generated copy.

## Install

Run in your logged-in Omarchy desktop as your ordinary user:

```bash
omarchy plugin add https://github.com/thelifeandtimes/omarchy-omabit.git --enable
```

`omarchy plugin install` is an alias for `add`. Omarchy handles cloning, validation,
trust confirmation, bar placement and enabling. No sudo, local release directory,
Go compiler or shell install hook is required.

On first use, the plugin downloads the three prebuilt **0.1.0-rc.2** release tools
over HTTPS and verifies their exact sizes and SHA-256 hashes. This is approximately
38 MB. They are cached under `$XDG_CACHE_HOME/omabit/native-binaries/` (normally
`~/.cache/omabit/native-binaries/`), outside the git checkout and global PATH.
Later starts use that verified cache, including offline starts.

**Pause after installation to inspect the UI.** When ready, choose
**Setup → Set up this computer**. Host setup and its OS authorization are separate;
merely installing/enabling the plugin does not create a runner or start any ships.
Linux x86-64 and Python 3.11+ are required for these pinned tools.

If downloading fails, check network access and use Refresh, or run
`~/.config/omarchy/plugins/thelifeandtimes.omabit/bin/urbit-collector --help`
to see the diagnostic. A failed download does not publish a partial binary cache.

## Update

Finish active desktop submissions, then unload the plugin while Git replaces QML:

```bash
omarchy plugin disable thelifeandtimes.omabit
omarchy plugin update thelifeandtimes.omabit
omarchy plugin enable thelifeandtimes.omabit
```

New binary pins use a separate cache directory. Plugin update does not itself
upgrade a runner host or restart ships. Keep host updates explicit.

## Candidate scope

This is the 0.1.0-rc.2 development plugin with schema-15 runner support. Its Recommended
Apps pill is the documented frozen draft; use bare bootstrap for initial lifecycle
checks. Release notes: https://github.com/thelifeandtimes/omabit/releases/tag/v0.1.0-rc.2.
