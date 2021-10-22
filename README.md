# Fedora Linux Live CD

See <https://fedoraproject.org/wiki/FedoraLiveCD>

And <https://github.com/livecd-tools/livecd-tools>

* <https://pagure.io/fedora-kickstarts>

* <https://pagure.io/fedora-comps>

```console
# # livecd-creator \
  --config=/usr/share/doc/livecd-tools/livecd-fedora-minimal.ks
```

```text
245M    livecd-fedora-minimal-***.iso
```

Kickstart

```text
lang en_US.UTF-8
keyboard us
timezone US/Eastern
authselect select sssd with-silent-lastlog --force
selinux --enforcing
firewall --disabled
part / --size 2048

repo --name=development --mirrorlist=http://mirrors.fedoraproject.org/mirrorlist?repo=rawhide&arch=$basearch


%packages
@standard

%end
```

Comp (DNF group)

```xml
  <group>
    <id>standard</id>
    <_name>Standard</_name>
    <_description>Common set of utilities that extend the minimal installation.</_description>
    <default>false</default>
    <uservisible>false</uservisible>
    <packagelist>
      <packagereq>abrt-cli</packagereq>
      <packagereq>acl</packagereq>
      <packagereq>at</packagereq>
      <packagereq>attr</packagereq>
      <packagereq>bash-completion</packagereq>
      <packagereq>bc</packagereq>
      <packagereq>bind-utils</packagereq>
      <packagereq>btrfs-progs</packagereq>
      <packagereq>bzip2</packagereq>
      <packagereq>cifs-utils</packagereq>
      <packagereq>compsize</packagereq>
      <packagereq>cpio</packagereq>
      <packagereq>crontabs</packagereq>
      <packagereq>cryptsetup</packagereq>
      <packagereq>cyrus-sasl-plain</packagereq>
      <packagereq>dbus</packagereq>
      <packagereq>default-editor</packagereq>
      <packagereq>deltarpm</packagereq>
      <packagereq>dos2unix</packagereq>
      <packagereq>dosfstools</packagereq>
      <packagereq>ed</packagereq>
      <packagereq>ethtool</packagereq>
      <packagereq>exfatprogs</packagereq>
      <packagereq>file</packagereq>
      <packagereq>fpaste</packagereq>
      <packagereq>fprintd-pam</packagereq>
      <packagereq>gnupg2</packagereq>
      <packagereq>hunspell</packagereq>
      <packagereq>iptstate</packagereq>
      <packagereq>irqbalance</packagereq>
      <packagereq>jwhois</packagereq>
      <packagereq>logrotate</packagereq>
      <packagereq>lsof</packagereq>
      <packagereq>mailcap</packagereq>
      <packagereq>man-pages</packagereq>
      <packagereq>mcelog</packagereq>
      <packagereq>mdadm</packagereq>
      <packagereq>microcode_ctl</packagereq>
      <packagereq>mlocate</packagereq>
      <packagereq>mtr</packagereq>
      <packagereq>net-tools</packagereq>
      <packagereq>nfs-utils</packagereq>
      <packagereq>nmap-ncat</packagereq>
      <packagereq>ntfs-3g</packagereq>
      <packagereq>ntfsprogs</packagereq>
      <packagereq>opensc</packagereq>
      <packagereq>passwdqc</packagereq>
      <packagereq>pciutils</packagereq>
      <packagereq>pinfo</packagereq>
      <packagereq>psacct</packagereq>
      <packagereq>quota</packagereq>
      <packagereq>realmd</packagereq>
      <packagereq>rsync</packagereq>
      <packagereq>rsyslog</packagereq>
      <packagereq>smartmontools</packagereq>
      <packagereq>sos</packagereq>
      <packagereq>sssd</packagereq>
      <packagereq>sudo</packagereq>
      <packagereq>symlinks</packagereq>
      <packagereq>systemd-udev</packagereq>
      <packagereq>tar</packagereq>
      <packagereq>tcpdump</packagereq>
      <packagereq>time</packagereq>
      <packagereq>traceroute</packagereq>
      <packagereq>tree</packagereq>
      <packagereq>unzip</packagereq>
      <packagereq>usbutils</packagereq>
      <packagereq>util-linux-user</packagereq>
      <packagereq>wget</packagereq>
      <packagereq>which</packagereq>
      <packagereq>words</packagereq>
      <packagereq>zip</packagereq>
      <packagereq type="conditional" requires="gnome-control-center">chrony</packagereq>
    </packagelist>
  </group>
```
