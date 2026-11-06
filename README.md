# 2026 Crack Lab

Modern binary analysis lab, bridging 1996-era reversing craft to 2026
tooling. Static analysis, sandboxed runs, tracing, diffing, and
local-LLM-assisted reading of disassembly. DOS-era targets delegate to
Debug Lab 2.0 (the 1996 heritage pipeline stays untouched).

## Install

```sh
cp 2026_crack ~/.local/bin/   # or anywhere on PATH
chmod +x ~/.local/bin/2026_crack
```

Requires: Python 3, objdump/binutils (PE via wine's binutils), strace,
optional local LLM endpoint for `explain`.

## Use

```
2026_crack tui                        interactive lab (default)
2026_crack identify FILE              magic, PE/ELF structure, hashes, entropy
2026_crack strings FILE [-u]          ascii + UTF-16LE strings
2026_crack disasm FILE [--lines N]    objdump slice (ELF + PE)
2026_crack run FILE [args...]         sandboxed run (wine prefix / timeout)
2026_crack trace FILE [args...]       strace for ELF, wine log for PE
2026_crack compare A B                version diff: sections, entropy, strings
2026_crack explain FILE [--lines N]   local LLM reads the disassembly
2026_crack dos                        hand a DOS target to Debug Lab 2.0
```
