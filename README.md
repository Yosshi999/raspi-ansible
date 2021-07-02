raspy-ansible
====

My ansible playbook for Raspberry Pi 3 Model B.

## Requirements
- Ansible 2.9
- 2021-05-07-raspios-buster-armhf-lite.img

## Usage

1. Make sure the raspi is ssh-able. (Check if the file named `ssh` exists in the boot folder.)
2. Connect the host's ethernet to the raspi's ethernet.
3. Find the raspi's IP. (See the section Find IP)
4. Copy `hosts.sample` to `hosts` and modify it.
5. run `./run.sh`.
6. Now you can ssh using the port and the identity file which you configured.

## Find IP
Usually you can use `raspberrypi.local`.

Otherwise, you can find it by running

- `arp -a`
- (for WSL) `arp.exe -a`
- (for WSL) `powershell.exe "Resolve-DnsName raspberrypi.local"`

