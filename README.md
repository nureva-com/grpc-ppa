# grpc-ppa
PPA repository for gRPC

## Usage

To use this PPA:

```bash
curl -s --compressed "https://nureva-com.github.io/grpc-ppa/KEY.gpg" | gpg --dearmor | sudo tee /usr/share/keyrings/nureva-grpc-archive-keyring.gpg
sudo curl -s --compressed -o /etc/apt/sources.list.d/nureva-grpc.list "https://nureva-com.github.io/grpc-ppa/nureva-grpc.list"
sudo apt update
sudo apt-get install -y <package from this repository>
```

## Updating/adding new Packages to the PPA

Put your new .deb files inside the git repo and run `./bin/generate.sh` to
update the files. Then commit and push to repo.
