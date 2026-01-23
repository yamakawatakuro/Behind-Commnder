# Behind Commander
A MIDI controller application for Pangolin Beyond, designed with lighting console-style workflows for live performance environments.

## Features
- **Built-in Virtual MIDI Port** - No need for loopMIDI (requires teVirtualMIDI driver)
- GO button workflow similar to lighting consoles (grandMA-style)
- Cue list management (add/edit/reorder)
- Dual mode operation (Operation/Edit)
- Four fade patterns (instant/linear/smooth/slow)
- Crossfade and auto-follow support
- Built-in MIDI mapping with "Learn" function
- Japanese/English language support

## Download
[Latest Release](https://github.com/yamakawatakuro/Behind-Commnder/releases)

## System Requirements

### Required
- Windows 10/11 (64-bit)
- Pangolin Beyond (with MIDI/PangoScript support)

### For Virtual MIDI Port Feature
Behind Commander includes built-in virtual MIDI port functionality. To use this feature:

**Option 1: teVirtualMIDI Driver (Recommended)**
- Download: https://www.tobias-erichsen.de/software/virtualmidi.html
- Free for personal use
- Allows Behind Commander to create virtual MIDI ports automatically

**Option 2: loopMIDI**
- Alternative if you prefer not to install teVirtualMIDI
- Download: https://www.tobias-erichsen.de/software/loopmidi.html

> **Note**: Without either driver, you can still use Behind Commander with physical MIDI devices or by selecting an existing MIDI output port.

## Installation

1. Download `BehindCommander-Setup.exe` from the [latest release](https://github.com/yamakawatakuro/Behind-Commnder/releases)
2. Run the installer
3. **(Optional)** Install teVirtualMIDI driver if you want automatic virtual MIDI port creation
4. Launch Behind Commander
5. Import the included PangoScript file into Pangolin Beyond
6. Configure MIDI input in Beyond's settings:
   - If using virtual port: Select "Behind Commander"
   - If using loopMIDI: Select your loopMIDI port
7. Start controlling Beyond!

## Quick Start

### First Time Setup
1. Start Behind Commander
2. Go to Edit Mode (press Edit button or E key)
3. Click "Learn" to map your MIDI controller buttons
4. Add cues to your cue list
5. Switch to Operation Mode (press Oper button or O key)
6. Use GO button to trigger cues in Beyond

### Virtual MIDI Port
On first launch, Behind Commander will attempt to create a virtual MIDI port named "Behind Commander". 
- ✅ If successful, you'll see "Virtual MIDI port active" in the console
- ⚠️ If unsuccessful, install teVirtualMIDI driver or use loopMIDI

## Documentation
Comprehensive Japanese user manual is included with the installation.

## Feedback
Feature suggestions and bug reports are welcome!
- [Report Issues](https://github.com/yamakawatakuro/BehindCommander/issues)
- [Discussions](https://github.com/yamakawatakuro/BehindCommander/discussions)

## License
MIT License

---

## For Developers
### Building from Source
```bash
# Install dependencies
npm install

# Run in development mode
npm run dev

# Build installer
npm run build
```

### Tech Stack
- Electron
- Node.js
- Koffi (for native DLL integration)
- easymidi (for MIDI communication)
