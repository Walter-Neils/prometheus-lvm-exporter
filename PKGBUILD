# Maintainer: Walter Irvin Neils <walter@walterneils.com>
pkgname=prometheus-lvm-exporter-bin
pkgver=1.0.0
pkgrel=1
pkgdesc="Prometheus exporter for LVM metrics (Manually built binary)"
arch=('x86_64')
url="https://github.com/project-url-here" # Update if applicable
license=('MIT') # Update based on the actual repo license
depends=('lvm2')
backup=('etc/prometheus-lvm-exporter.conf') # If you add a config later

# We assume the binary and service file are in the same folder as this PKGBUILD
source=("prometheus-lvm-exporter"
        "prometheus-lvm-exporter.service")

# Skip checksums since these are your local files
sha256sums=('SKIP'
            'SKIP')

package() {
    # 1. Install the binary
    install -Dm755 "${srcdir}/prometheus-lvm-exporter" "${pkgdir}/usr/bin/prometheus-lvm-exporter"

    # 2. Install the systemd service
    install -Dm644 "${srcdir}/prometheus-lvm-exporter.service" "${pkgdir}/usr/lib/systemd/system/prometheus-lvm-exporter.service"
}
