# Maintainer: Harry ten Berge <htenberge@gmail.com>

pkgname=ropieee
pkgver=20170917
pkgrel=1
arch=(any)
url="https://github.com/RoPieee/"
license=('MIT')
depends=('ropieee-version'
	 'fakeroot'
	 'usleep'
         'wput'
	 'git'
	 'ipcalc')
install=${pkgname}.install



package() {
echo "package"

   install -d "${pkgdir}/boot/RoPieee"
   install -d "${pkgdir}/opt/RoPieee/sbin"
   install -d "${pkgdir}/opt/RoPieee/conf"
   install -d "${pkgdir}/opt/RoPieee/lib"
   install -d "${pkgdir}/etc/systemd/system"
   install -d "${pkgdir}/etc/systemd/system/roonbridge.service.d"

   install -m0755 "../ropieee/bootstrap"                                "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/control_led"                              "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/check_ntp_offset"                         "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/run_rescue_scripts"                       "${pkgdir}/boot/RoPieee"

   install -m0644 "../ropieee/alsa-base.conf"                           "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/fstab"                                    "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/journald.conf"                            "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/ropieee.conf"                             "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/sshd_config"                              "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/resolved.conf"                            "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/pacman.conf"                              "${pkgdir}/opt/RoPieee/conf"

   install -m0755 "../ropieee/run-updates"                              "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/configure"                                "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/reboot"                                   "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/send-feedback"                            "${pkgdir}/opt/RoPieee/sbin"

   install -m0755 "../ropieee/lib/disable_usb_audio"                    "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/enable_usb_audio"                     "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/disable_wifi"                         "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/enable_wifi"                          "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/install_roonbridge"                   "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/install_touchscreen"                  "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/touchscreen_on"                       "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/touchscreen_off"                      "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/set_touchscreen_orient_default"       "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/set_touchscreen_orient_rotated"       "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/get_hardware_model"                   "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/check_for_updates"                    "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/set_update_timer"                     "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/get_country_code"                     "${pkgdir}/opt/RoPieee/lib"

   install -m0644 "../ropieee/systemd/ropieee1-bootstrap.service"       "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee-update.service"           "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee-update.timer"             "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-reboot.service"          "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-led.service"             "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee-feedback@.service"        "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee-roonbridge-override.conf" "${pkgdir}/etc/systemd/system/roonbridge.service.d"

   # overruling some default services
   install -m0644 "../ropieee/systemd/ntpd.service"                     "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ntpdate.service"                  "${pkgdir}/etc/systemd/system"
#   install -m0644 "../ropieee/rescue.service"                           "${pkgdir}/etc/systemd/system"
}

