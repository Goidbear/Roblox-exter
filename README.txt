# roblox_external

External cheat for Roblox. ESP, aimbot, walkspeed. Separate process, no
injection, D3D11 overlay.

## ⚠️ before you run ⚠️

1. **Install the VC++ redistributable.** If you skip this, the exe will
   close instantly with no error message.
   → https://aka.ms/vs/17/release/vc_redist.x64.exe

2. **Start Roblox and join a game first**, then launch `roblox_external.exe`.

## features

- **ESP** — box, name, distance, health bar, tracer. full color/size tuning.

- **Aimbot** — hold a key to aim. configurable FOV, smoothing, target part
  (head / torso / legs). rebindable from the menu.

- **Walkspeed / Jump** — adjustable from the menu.

## controls

| key | action |
|---|---|
| INSERT | open / close menu |
| END | exit |
| RMB (default) | hold to aim |

## menu

Opened with INSERT. Save/load config buttons at the top, `config.ini` sits
next to the exe.

## known issues

- **Offsets go stale every Roblox update.** If ESP stops working after a
  patch, the offsets in `src/roblox/offsets.h` need refreshing.
- **Server-side walkspeed caps.** In games with strict anti-cheat, the
  server will reset your speed. Turn walkspeed off in those servers.

## building from source

Requires Visual Studio 2022 Build Tools, CMake 3.20+, and the imgui +
minhook submodules.

```bash
git clone https://github.com/ocornut/imgui vendor/imgui
git clone https://github.com/TsudaKageyu/minhook vendor/minhook
cmake -B build -G "Visual Studio 17 2022" -A x64
cmake --build build --config Release
```

## credits
Offsets from [theo's offsets](https://offsets.imtheo.lol).

## more stuff lol
10/69 in virus total damn.
Mostly broken but enjoy👍
