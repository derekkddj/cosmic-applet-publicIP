# COSMIC Public IP Applet

Applet de COSMIC que muestra la IP pública (externa) de tu equipo en el popup del panel.

## Ejecutar localmente

```sh
cargo run --release
```

## Instalar y usar en el panel COSMIC

1. Compila en release:
   ```sh
   cargo build --release
   ```
2. Copia los archivos a las rutas del sistema (ajusta si usas otro prefijo):
   ```sh
   sudo install -Dm0755 target/release/cosmic-applet-publicip /usr/bin/cosmic-applet-publicip
   sudo install -Dm0644 resources/app.desktop /usr/share/applications/com.github.derekkddj.cosmic-applet-publicip.desktop
   sudo install -Dm0644 resources/app.metainfo.xml /usr/share/appdata/com.github.derekkddj.cosmic-applet-publicip.metainfo.xml
   sudo install -Dm0644 resources/icon.svg /usr/share/icons/hicolor/scalable/apps/com.github.derekkddj.cosmic-applet-publicip.svg
   ```
3. Cierra sesión y vuelve a entrar en COSMIC (o reinicia el shell).
4. Abre la configuración del panel y agrega el applet **Public IP**.
5. Haz clic en el icono del applet para ver la IP externa actual.
