# LiveryForge

**Custom iRacing liveries in a few clicks.** LiveryForge is a free Windows app that designs paint schemes for your iRacing car – racing stripes, gradients, geometric shards, camo, splatter – puts your own logos on it, shows it live on the car, and saves the finished livery straight into iRacing's paint folder.

This page is only for **downloads**. There is no source code here.

## What you need

- Windows 10 or Windows 11 (64-bit)
- iRacing, and your iRacing **customer ID** (a number – the app shows you where to find it)
- The **paint template** of your car from iRacing (a free download, see below)

## Supported cars

- Porsche 911 GT3 Cup (992.2)
- Aston Martin Vantage EVO GT3

More cars: download profiles other drivers made, or calibrate your own (see *More cars* below).

## Install

1. Go to **[Releases](../../releases/latest)** and download `LiveryForge-Setup-<version>.exe`.
2. Run it. No administrator rights are needed – LiveryForge installs just for your Windows user.
3. **Windows SmartScreen** will probably show *"Windows protected your PC"*. That happens because the app is not code-signed (signing certificates cost a lot of money every year). Click **More info** → **Run anyway**.
4. On the first start a short setup asks for your customer ID, finds your iRacing paint folder and lets you pick your car and its template.

*Optional – check the download:* every release also has a `.sha256` file. In PowerShell, `Get-FileHash .\LiveryForge-Setup-<version>.exe` must show the same number.

## Getting the iRacing paint template

On iracing.com open your car's page and download its **paint template**. It comes as a `.zip` – unzip it and choose the `.psd` file inside when LiveryForge asks for the template. LiveryForge only reads the template, it never changes it.

## Using it in iRacing

Press **Export** in LiveryForge. The car updates automatically in the iRacing UI's car view; in a sim session, press **Ctrl+R**. Your livery is saved as `car_<your ID>.tga` in `Documents\iRacing\paint\<car>\`.

Every export first backs up the livery that was there before – your original paint is always kept (see **Backups…** in the app).

## Logos

Put your team's or sponsors' logos on the car (**Logos** in the left panel):

- **Import** PNG, JPG or SVG logos into your logo library – they're reusable in every design.
- App icon with a background? **Remove background** clears the surround, **Remove colour** keys out a colour everywhere (e.g. the dark inside a shield, so the car colour shows through) – with smooth edges.
- **Text logos**: your name or team in a sporty font (Rajdhani, Orbitron, Exo 2, Saira, Russo One – free fonts), bold / italic, outline, letter spacing.
- Place them on the hood, roof, doors, rear quarters, bumpers or wing endplates. Logos on the sides go on **both sides, readable on both** (never mirror-reversed) – or on one side only.
- They are **never clipped**: a logo always stays on the visible part of the panel – away from panel edges, wheel arches, vents, grilles, lights and the number blocks. If one doesn't fit, it is moved or shrunk and the app tells you.
- A saved or shared design carries its logos, so a friend sees the same.

### Car views

Next to the flat template, the centre view shows the car from the **left, right, top, front and rear**. Drag a logo to move it, drag a corner to resize it, drag the round handle to turn it. While you drag, the parts that would be hidden show in red; when you let go it snaps onto the visible area. The sliders on the left are there for fine-tuning.

## Import a livery

Already have a livery (a 2048 TGA or PNG for the same car)? **Style → Import TGA…** uses it as the design – your logos and iRacing's branding still go on top. **Select pieces** and **Fill** (or **Fill with base colour**) paint over the parts you don't want.

## Updates

LiveryForge checks for a new version once a day when it starts (you can turn this off in Settings, or check by hand under Settings → About → *Check for updates*). When there is one, it shows what's new; **Update now** downloads it, checks it and installs it – your settings, designs and backups stay as they are.

## More cars

LiveryForge needs a *car profile* for each car: it tells the app how the car's flat template wraps around the real car. In the app, **Settings → Get car profiles…** lists the cars other drivers calibrated (they live in the [profiles](profiles) folder here) and installs them with one click – every download is checked before it is used.

Your car isn't there? **Settings → Calibrate new car (beta)…** walks you through it: export a colour-coded test livery, switch to the iRacing UI's car view (it updates by itself), press **Ctrl+Shift+L** from several angles, and LiveryForge works out the panels; you fix what it got wrong by clicking on the photos. Make the car as big as possible in the view before capturing. You can share the result as a `.lfcar` file (Settings → Car profiles → Export). Calibrating is new and still in beta – feedback is welcome.

Bumper stripes a little off the hood's? **Settings → Car profiles → Align bumpers from a photo (beta)…**: drop in a straight front (or rear) screenshot of the stripe test and LiveryForge lines the bumper up sideways and in width.

## Where your stuff lives

Settings, saved designs, your logo library, imported liveries and livery backups are in `%APPDATA%\LiveryForge`. Uninstalling LiveryForge (Windows Settings → Apps) removes the program but **keeps** this folder.

## Good to know

- Designs work on every supported car – share a design with a friend: *Designs → Export…*, they add it with *Import…*.
- *Capture iRacing* (screenshot thumbnails of your design) and **Ctrl+Shift+L** capture the window in front - the iRacing UI or the sim. The sim must run in **windowed or borderless** mode; fullscreen can't be captured.
