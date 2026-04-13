# TimeTableStudio

Desktop app for course scheduling built with:

- React + TypeScript + Vite
- Electron
- Python schedule

## How to Run This Project

### 1. Portable Release
If you upload the portable build from `release/`, end users do **not** need to install:

- Python
- Node.js
- Electron

They only need to download the generated portable `.exe` and run it on Windows x64.

## Important Notes

- Portable release target currently focuses on Windows x64.
- The portable build bundles the Python scheduler, so end users do not need Python installed.
- Source mode still uses local Python from `PATH`.
- Desktop project data is stored in `Documents/TimeTableStudio/projects` for easier access by end users.
- Windows SmartScreen may still show a warning because the app is unsigned.
