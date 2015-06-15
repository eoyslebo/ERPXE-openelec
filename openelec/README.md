openelec
========

Plugin for https://github.com/ERPXE/tftpboot

```bash
export ISODIR=/tmp/iso
export ERPXEDIR=/tftpboot
mkdir -p $ISODIR
cd $ISODIR
wget http://releases.openelec.tv/OpenELEC-Generic.x86_64-5.0.8.tar
mkdir -p $ERPXEDIR/er/shares/openelec/storage
tar xf OpenELEC*tar -C /tmp
mv /tmp/OpenELEC-Generic.x86_64-5.0.8/splash.png $ERPXEDIR/er/plugins/openelec/openelec.png
mv /tmp/OpenELEC-Generic.x86_64-5.0.8/target/SYSTEM $ERPXEDIR/er/shares/openelec/
mv /tmp/OpenELEC-Generic.x86_64-5.0.8/target/KERNEL $ERPXEDIR/er/plugins/openelec/
$ERPXEDIR/bin/replace_nfsroot_ip.sh
bash
