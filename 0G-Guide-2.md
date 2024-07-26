# Guide to Setting Up DA-Client, DA-Encoder, DA-Node, and DA-Retriever for 0G
## Part 2

### Setting Up DA-Node

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
Clone the 0G DA-Node Repository and Build the Binary:

```
git clone https://github.com/0gnetwork/0g-da-node.git
cd 0g-da-node
make install
```
Configure DA-Node:

Edit the configuration file:

```
nano ~/.0g-da-node/config.toml
```
Set parameters such as peers, validator, and network settings.

Start the DA-Node:

```
0g-da-node start
```
### Setting Up DA-Retriever
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
Clone the 0G DA-Retriever Repository and Build the Binary:

```
git clone https://github.com/0gnetwork/0g-da-retriever.git
cd 0g-da-retriever
make install
```
Configure DA-Retriever:

Edit the configuration file:

```
nano ~/.0g-da-retriever/config.toml
```
Set the necessary parameters, including source, destination, and retrieval settings.

Start the DA-Retriever:

```
0g-da-retriever start
```
