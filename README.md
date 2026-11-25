# OG Launcher

A fast, modern custom launcher for **Minecraft: Java Edition**, built with **Rust (Tauri 2)** and **React + TypeScript + Tailwind**.

> Personal, non-commercial hobby project. Not affiliated with Mojang or Microsoft.

## Features

- Launch any Minecraft version (release, snapshots, old versions) with **Vanilla, Fabric or Quilt**
- Separate **instances** per version, with shared libraries and assets cache
- Built-in **Modrinth** browser: mods, resource packs and shaders, with one-click install and required dependencies
- **My content** view: enable/disable/delete mods, icons and descriptions resolved from Modrinth by file hash
- Automatic **Java detection and download** (Eclipse Temurin) matching the version's requirements
- Live **game console** window with log search, copy and stop button
- 3D skin preview, multiple accounts, Polish and English UI

## Microsoft account sign-in

The launcher signs players in with the **official Microsoft device code flow**:

1. Microsoft account (OAuth 2.0 device code)
2. Xbox Live user token → XSTS token
3. Minecraft Services login (`/authentication/login_with_xbox`)
4. Ownership check (`/entitlements/mcstore`) and profile (`/minecraft/profile`)

Only the refresh token is stored locally on the user's machine. **Passwords are never seen or stored** by the launcher.

## Tech stack

| Part | Technology |
| --- | --- |
| Backend | Rust, Tauri 2, reqwest, tokio |
| Frontend | React 18, TypeScript, Tailwind CSS, Framer Motion |
| 3D skin | skinview3d |
| Mods | Modrinth API |

## Source code

The source code is not public. More details can be provided on request.

## License

All rights reserved. Minecraft is a trademark of Mojang Studios.
