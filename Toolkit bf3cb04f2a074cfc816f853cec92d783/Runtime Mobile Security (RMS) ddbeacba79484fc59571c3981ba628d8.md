# Runtime Mobile Security (RMS)

CUI/GUI: GUI
Keywords: frida, hooking, runtime
OS: all

# Install

```bash
npm install -g rms-runtime-mobile-security
```

# Usage

Run: `RMS-Runtime-Mobile-Security` or `rms`. Open [`http://127.0.0.1:5000/`](http://127.0.0.1:5000/), or whatever URL is returned in Terminal.

`Spawn` function doesn't seem to be working for me, but `Attach` does (the target process should be running).

There are some predefined useful `frida` scripts (like in `objection`). To stop the program from crashing, use `System.exit() Bypass`. 

On the `Dump Tab` (if you have not already pressed `Run RMS` on the starting page) press `Load Classes` to see all classes and `Load methods`  to see the methods currently loaded. Chose the ones you're interested in (most of the time it's the package's name) and filter by pressing `Insert Filter`. The `Hook all methods` and see the console.

To hook some Cipher-related methods, use `frida` script `tracer_cipher.js`.