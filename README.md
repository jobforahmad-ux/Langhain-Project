# Langhain-Project

This repository references the original course as a Git submodule at langchain-course/.

## Getting started

- Clone with submodules:
  `ash
  git clone --recurse-submodules https://github.com/jobforahmad-ux/Langhain-Project.git
  `

- If already cloned without submodules:
  `ash
  git submodule update --init --recursive
  `

## Updating the course content

- Pull latest from upstream inside the submodule and record the update in this repo:
  `ash
  cd langchain-course
  git checkout main
  git pull origin main
  cd ..
  git add langchain-course
  git commit -m "Update submodule to latest"
  git push
  `

## Pinning a specific version

- Optionally checkout a specific commit or tag inside langchain-course/:
  `ash
  cd langchain-course
  git checkout <tag-or-commit-sha>
  cd ..
  git add langchain-course
  git commit -m "Pin submodule to <tag-or-commit-sha>"
  git push
  `

## Notes

- The submodule points to: https://github.com/harishneel1/langchain-course.git
- This setup preserves attribution and avoids redistributing the source code directly in this repository.

## Auto-update script

Use the PowerShell script to update the submodule to the latest on a branch and push the change:

```powershell
# From repo root
powershell -ExecutionPolicy Bypass -File .\scripts\update-submodule.ps1 -SubmodulePath "langchain-course" -SubmoduleBranch "main" -Remote "origin"
```

- Parameters:
  - `-SubmodulePath`: Path of the submodule folder (default: `langchain-course`)
  - `-SubmoduleBranch`: Branch to track in the submodule (default: `main`)
  - `-Remote`: Superproject remote to push to (default: `origin`)

If you see an execution policy error, use `-ExecutionPolicy Bypass` as shown above or temporarily run:
```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```
