# Guide to Setting Up DA-Client, DA-Encoder, DA-Node, and DA-Retriever for 0G
## Part 1

### Setting Up DA-Client
Update System Packages:

```
sudo apt update && sudo apt upgrade -y
```
Install Required Dependencies:

```
sudo apt install -y build-essential git curl jq
```
Install Go:

```
wget https://golang.org/dl/go1.19.1.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.19.1.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
source ~/.profile
```
Clone the 0G DA-Client Repository and Build the Binary:

```
git clone https://github.com/0gnetwork/0g-da-client.git
cd 0g-da-client
make install
```
Configure DA-Client:

Edit the configuration file:

```
nano ~/.0g-da-client/config.toml
```
Set the appropriate configuration parameters, including validator, node, and network settings.

Start the DA-Client:

```
0g-da-client start
```
### Setting Up DA-Encoder

Update System Packages:

```
sudo apt update && sudo apt upgrade -y
```

Install Required Dependencies:

```
sudo apt install -y build-essential git curl jq
```
Install Go:

```
wget https://golang.org/dl/go1.19.1.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.19.1.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
source ~/.profile
```
Clone the 0G DA-Encoder Repository and Build the Binary:

```
git clone https://github.com/0gnetwork/0g-da-encoder.git
cd 0g-da-encoder
make install
```
Configure DA-Encoder:

Edit the configuration file:

```
nano ~/.0g-da-encoder/config.toml
```
Set the configuration parameters such as input, output, and encoding settings.

Start the DA-Encoder:

```
0g-da-encoder start
```
