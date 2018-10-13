<img src="https://demille.github.io/encrusted/src/img/name.svg" alt="encrusted" width="200px;"/>

---

#### A z-machine (interpreter) for Infocom-era text adventure games like Zork

Runs in a web interface or directly in a terminal.  
Built with Rust and WebAssembly (`wasm32-unknown-unknown`).

🎮 [Load the web version][web]

**Features**
- [x] Live mapping to keep track of where you are
- [x] Undo / Redo support
- [x] Narration / Dictation using the [web speech APIs][APIs]
- [x] Object tree inspector

[web]: https://sterlingdemille.com/encrusted
[APIs]: https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API

### Install
Terminal version:

```sh
cargo install encrusted
```

Run a file with `encrusted <FILE>`.  
Use `$undo` and `$redo` to step through your move history.  
Use `save` and `restore` to save your progress.

### Build
Terminal version:

```sh
cargo build --bin encrusted
```

WebAssembly/React web version:

```sh
# Runs webpack dev server on port 8000
npm run dev

# Builds web interface (.wasm module) and bundles JS into the ./build directory
npm run release
```

### Notes
- Currently only supports v3 zcode files (most of Infocom's library, really)
- Saves games in the Quetzal format
- Zork 1, 2 and 3 can be downloaded from http://www.infocom-if.org/downloads/downloads.html

### License
MIT
