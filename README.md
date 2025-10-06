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
