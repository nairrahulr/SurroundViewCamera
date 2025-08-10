## Setup packages:

- ### Linux
  ```
  sudo apt update  -y
  sudo apt install  libpango1.0-dev \
                    libatk1.0-dev \
                    libgdk-pixbuf-2.0-dev \
                    libgtk-3-dev \
                    libsoup-3.0-dev \
                    libwebkit2gtk-4.1-dev -y
  ```
- ### Install [Node.js (current)](https://nodejs.org/en/download/current)
- ### Base dependencies (needs to be executed only once)

  ```
  npm i pnpm@latest -g

  # core dependencies
  pnpm i tauri vite deno -g

  # Select all options that'd show up, press "Enter"; press "y" to continue
  pnpm approve-builds -g

  # needs to be executed whenever there's a change in FE packages
  pnpm i
  ```

## Run app in DEV mode

```
# executes both backend (rust) and frontend (vite/svelte)
# first time run would install rust crates, which takes some time
pnpm tauri dev
```
