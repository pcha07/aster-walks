# aster-walks (public, walk runner only)

Holds one workflow, `.github/workflows/simulator-walk.yml` (copy of simulator-walk.yml next to this file). No app code, no secrets in git.
- Reads pcha07/vibe-dating with the repo secret `VIBE_READ` (fine-grained token, Contents: read-only, that one repo, 90 days).
- Builds the staging app (fake members only), runs the Maestro sim flows on an iPhone simulator (macos-15) and an Android emulator (ubuntu + KVM).
- Uploads only `walk-out/**` (screenshots, junit, video). GitHub masks the secret in logs automatically. Public artifacts: never walk a build that is not staging.
- Run: Actions > Aster simulator walk > Run workflow, ref = branch to walk.
