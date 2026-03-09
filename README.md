# COSMIC Public IP Applet

COSMIC applet that displays your machine's external (public) IP address in the panel popup.

## Run locally

```sh
cargo run --release
```

## Install and use in the COSMIC panel

1. Build in release mode:
   ```sh
   cargo build --release
   ```
2. Copy the files to system paths (adjust if you use a different prefix):
   ```sh
   sudo install -Dm0755 target/release/cosmic-applet-publicip /usr/bin/cosmic-applet-publicip
   sudo install -Dm0644 resources/app.desktop /usr/share/applications/com.github.derekkddj.cosmic-applet-publicip.desktop
   sudo install -Dm0644 resources/app.metainfo.xml /usr/share/appdata/com.github.derekkddj.cosmic-applet-publicip.metainfo.xml
   sudo install -Dm0644 resources/icon.svg /usr/share/icons/hicolor/scalable/apps/com.github.derekkddj.cosmic-applet-publicip.svg
   ```
3. Log out and back in to COSMIC (or restart the shell).
4. Open panel settings and add the **Public IP** applet.
5. Click the applet icon to see the current external IP.
