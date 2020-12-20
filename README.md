### Use docker container instead of VMs

- Build image inside `ubuntu/` folder

`cd ubuntu/ && docker build -t ubuntu-sshd .`

- Run `docker run -p 2222:22 ubuntu-sshd`

- Root password `root`

- You can mount volume to `/root/.ssh` inside container with `authorized_keys` file. Give
`root:root` for mounted file.