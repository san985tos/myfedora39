# Export a VirtualBox VM to Vagrant box

## Commands

```
VBoxManage list runningvms
vagrant package --base satellite_vs614_satellite_614_1704257172801_3899 satellite_v6.14.box
vagrant box add package.box --name satellite_v6.14
vagrant box list

```

## Example

```
❯  VBoxManage list runningvms
"satellite_vs614_satellite_614_1704257172801_3899" {4ff11a60-457e-4a06-a003-7f7c4fcb1d20}

❯ vagrant package --base satellite_vs614_satellite_614_1704257172801_3899 satellite_v6.14.box
==> satellite_vs614_satellite_614_1704257172801_3899: Clearing any previously set forwarded ports...
==> satellite_vs614_satellite_614_1704257172801_3899: Exporting VM...
==> satellite_vs614_satellite_614_1704257172801_3899: Compressing package to: /home/lvazquez/vagrant-boxes-and-ISOs/package.box

❯ vagrant box add package.box --name satellite_v6.14
==> box: Box file was not detected as metadata. Adding it directly...
==> box: Adding box 'satellite_v6.14' (v0) for provider: 
    box: Unpacking necessary files from: file:///home/lvazquez/vagrant-boxes-and-ISOs/package.box
==> box: Successfully added box 'satellite_v6.14' (v0) for 'virtualbox'!

❯ vagrant box list
bento/fedora-36 (virtualbox, 202303.13.0)
bento/fedora-37 (virtualbox, 202309.08.0)
bento/fedora-38 (virtualbox, 202309.08.0)
fedora39        (virtualbox, 0)
generic/rhel8   (virtualbox, 4.3.10)
generic/rhel9   (virtualbox, 4.3.8)
satellite_v6.14 (virtualbox, 0)

```
