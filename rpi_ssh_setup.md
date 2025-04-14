## Raspberry Pi network & SSH at boot
- Connect to the network via Ethernet or WiFi using `raspi-config` or `nmcli`
- Enable SSH Server at boot `raspi-config`
## SSH Setup
- Setup SSH Client
    - Generate SSH key pair `ssh-keygen` (each user has its own SSH key pair)
    - Copy the public key manually to the `~/.ssh/authorized_keys` file or use `ssh-copy-id -i ~/.ssh/key.pub user@rpi_ip`
- Setup SSH Server `/etc/ssh/sshd_config`
    - Disable SSH password authentication
    - Disable root access via SSH, `PermitRootLogin no`
    - Restart service `sudo systemctl restart sshd`
- SSH Connection `ssh -i /root/.ssh/key user@rpi_ip`
## Specify SSH key by host
- Create SSH config file at `~/.ssh/config`
- Add text:
    ```
    Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/your_specific_key
    ```
