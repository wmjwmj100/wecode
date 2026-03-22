# Uploading `wecode` Binary to GitHub

This document shows two common ways to publish the `wecode` executable.

## Option A (Recommended): GitHub Releases

Use this for distributing binaries to users.

1. Build binary (example):

```powershell
cd C:\work\wecode
# example build command (replace with your real build)
# cargo build --release
```

2. Create a tag and push:

```powershell
git add .
git commit -m "Initial wecode repository"
git tag v0.1.0
git remote add origin <YOUR_GITHUB_REPO_URL>
git branch -M main
git push -u origin main
git push origin v0.1.0
```

3. On GitHub, open the repository:
- Go to `Releases` -> `Draft a new release`
- Select tag `v0.1.0`
- Upload binary files (e.g. `wecode.exe`, `wecode-linux-x64`, checksums)
- Publish release

## Option B: Track Binary in Git (Only if needed)

If binary is larger than 100 MB, use Git LFS.

```powershell
cd C:\work\wecode
git lfs install
git lfs track "*.exe"
git add .gitattributes
```

Then add binary and push:

```powershell
git add path\to\wecode.exe
git commit -m "Add wecode binary"
git push
```

## Notes

- GitHub regular Git upload hard limit: 100 MB per file.
- For deliverables, Releases is cleaner than committing binaries into source history.
- Consider publishing checksums (`sha256`) alongside binaries.
