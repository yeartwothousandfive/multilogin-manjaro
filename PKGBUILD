
pkgname=mlxapp
pkgver=12.17.0
pkgrel=1
pkgdesc="Multilogin Desktop Application"
arch=('x86_64')
url="https://multilogin.com/"
license=('custom')

depends=(
    'webkit2gtk-4.1'
    'gtk3'
    'libayatana-appindicator'
    'libx11'
    'glibc'
    'gcc-libs'
)

options=('!strip')

package() {
    # Application files
    install -dm755 "$pkgdir/opt/mlxapp"

    install -m755 \
        "$startdir/opt/mlxapp/desktop.bin" \
        "$pkgdir/opt/mlxapp/desktop.bin"

    install -m644 \
        "$startdir/opt/mlxapp/mlx.png" \
        "$pkgdir/opt/mlxapp/mlx.png"

    # Application launcher
    install -dm755 "$pkgdir/usr/bin"

    cat > "$pkgdir/usr/bin/mlxapp" <<'EOF'
#!/bin/sh
exec /opt/mlxapp/desktop.bin "$@"
EOF

    chmod 755 "$pkgdir/usr/bin/mlxapp"

    # Desktop shortcut
    install -Dm644 \
        "$startdir/usr/share/applications/mlxapp.desktop" \
        "$pkgdir/usr/share/applications/mlxapp.desktop"

    # Use the installed launcher
    sed -i \
        's|Exec=/opt/mlxapp/desktop.bin %u|Exec=/usr/bin/mlxapp %u|' \
        "$pkgdir/usr/share/applications/mlxapp.desktop"
}
