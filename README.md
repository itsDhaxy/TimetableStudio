# TimeTableStudio

Desktop app for course scheduling built with:

- React + TypeScript + Vite
- Electron
- Python scheduler bridge

## Two Ways To Share This Project

### 1. Source Code
If you upload the source code only, users still need to install:

- Node.js
- npm
- Python 3

They also need to run the app from source.

### 2. Portable Release
If you upload the portable build from `release/`, end users do **not** need to install:

- Python
- Node.js
- Electron

They only need to download the generated portable `.exe` and run it on Windows x64.

## Development

Install dependencies:

```powershell
npm install
```

Run lint:

```powershell
npm run lint
```

Run Electron dev mode:

```powershell
npm run dev:electron
```

## Build Portable App

### Prerequisites for the developer machine

- Node.js
- npm
- Python 3
- PyInstaller

Install PyInstaller once:

```powershell
py -3 -m pip install pyinstaller
```

Install JavaScript dependencies:

```powershell
npm install
```

Create the recommended portable release asset:

```powershell
npm run dist:portable
```

Output:

- Portable zip asset: `release/TimeTableStudio-win-portable.zip`
- Bundled Python scheduler binaries: `build/python-dist/`

If you want to try a single-file portable `.exe`, use:

```powershell
npm run dist:portable:onefile
```

Note: the single-file portable build can take much longer to finish than the zip-based portable build.

## Important Notes

- Portable release target currently focuses on Windows x64.
- The portable build bundles the Python scheduler, so end users do not need Python installed.
- Source mode still uses local Python from `PATH`.
- Desktop project data is stored in `Documents/TimeTableStudio/projects` for easier access by end users.
- Windows SmartScreen may still show a warning because the app is unsigned.
