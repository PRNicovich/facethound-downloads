# Facet Hound
### Advanced Precision Technologies, LLC

Gem-design viewer, cutting simulator and experimental faceting-machine dashboard.
**Prototype software — Windows and Android downloads are available below.**

## Download

| Device | Download |
| --- | --- |
| Android phone or tablet | [Download Android APK](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-Android.apk) |
| Windows 10/11, 64-bit | [Download Windows ZIP](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-Windows.zip) |
| Optional Android design library | [Download designs](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-Designs.zip) |
| Verify downloads | [SHA-256 checksums](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/SHA256SUMS.txt) |

[All releases and files](https://github.com/PRNicovich/facethound-downloads/releases). Download the APK or Windows ZIP, not GitHub's Source code archives.

## Android installation — same app for phones and tablets

1. Open the Android APK link on your phone/tablet. Download the APK.
2. Open **My Files → Downloads → FacetHound-Android.apk** and tap Install.
3. If prompted, allow My Files/browser to **Install unknown apps** for this installation. You can turn that permission off afterward.
4. If Samsung Auto Blocker prevents this install, temporarily disable it in **Settings → Security and privacy → Auto Blocker**, then restore it afterward. [Samsung's instructions](https://www.samsung.com/sg/support/mobile-devices/protect-your-galaxy-device-with-the-new-auto-blocker-feature/).
5. Open Facet Hound. For initial exploration, choose **Settings → Display → Viewer**, or turn on **Simulation**. No controller is needed.
6. For more designs, extract the optional design ZIP into Downloads. Use **Settings → Load gem** to grant access to the extracted Facet Hound folder.

To update, install the new APK over the existing app; **do not uninstall first** if you want to keep local settings and save states. No developer mode, USB debugging, PC or Java installation is required.

## Windows installation

1. Download the Windows ZIP and extract the **whole folder** to a writable location.
2. Open **Facet Hound/Facet Hound.exe**. Keep the `app` and `runtime` folders beside the EXE.
3. The Java runtime and USB serial library are included. No separate Java, Python, SDK or ADB is needed.
4. Use **Settings → Load gem**, Ctrl+O, or drag a supported design into the app.

This is an unsigned prototype; Windows may show an unknown-publisher warning. Only run the package you intended to download from this APT repository.

## Requirements: viewing and simulation

| Platform | Requirements |
| --- | --- |
| Android | Android 7.0/API 24 or newer. Previously tested on Galaxy S21 and Galaxy Tab Active2 (Android 9); newest layouts were checked off-device. Touch screen; no machine hardware required. |
| Windows | Windows 10/11 x64. Bundled Java runtime. Mouse/keyboard or touch. |
| iPhone/iPad | Native Viewer + Simulation prototype is being prepared. **No iOS download is available yet.** It needs Mac/Xcode build/signing and physical-device testing. No iOS machine control is planned for this first prototype. |

Supports GemCAD `.asc` / `.gem` and Gem Cut Studio `.gcs` designs on Android and Windows. Viewer mode omits mast telemetry; simulation uses generated values, not real measurements. RI/color previews are illustrative. PC optical preview is more demanding than the lightweight mobile display.

## Requirements: machine control / SKR communication

**Machine motion is not ready for unattended or live cutting.** Current SKR 3 H723 bring-up firmware confirms identity/nonce/heartbeat over USB, with motor and accessory outputs disabled. A verified handshake is not confirmation of motor, mast, lap or safety operation.

- Windows: suitable USB data cable and compatible SKR USB CDC firmware.
- Android: USB host/OTG support, app USB permission, a compatible data-capable hub/cable, and a verified charging/power arrangement.
- Real angle/index/Z/contact readings require the mast module, its wiring, calibration and telemetry firmware. RS485 lap control and accessory wiring/firmware still need integration.
- TMC2209 setup, motor wiring, power, homing/limits/interlocks and motion firmware must be validated before live control.
- External USB keyboard is optional. USB microscope support is currently external-app/split-view workflow.
- Android and PC are the initial control platforms. iOS prototype scope is Viewer + Simulation only.

No firmware flash is needed to try Viewer or Simulation. The public downloads do not include the private machine firmware source.

## Save and revisit work

**Settings → Save / load states** keeps multiple named checkpoints with the design, selected facet, completion/partial cuts, index edits, rough data and display/material setup. The automatic last-session file is separate. Saves are local to each device; loading pauses the demo/local dop animation.

## Share

[Printable QR image](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-QR-print.png) · [QR SVG](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-QR.svg) · [Square QR PNG](https://github.com/PRNicovich/facethound-downloads/releases/latest/download/FacetHound-QR.png)

The QR opens this download/instruction page. Keep using it when new releases appear.

## License and source

APT product binaries are proprietary. This public repository contains distribution files and documentation, **not the private application source**. Bundled third-party and upstream notices remain in the packages. Public availability does not grant rights to resell the product or remove notices. See the included license.
