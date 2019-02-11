# NetworkSpec
Bloxberg Genesis file and Bootnodes

In order to connect to the bloxberg network, you will need to install the latest stable parity version (https://github.com/paritytech/parity-ethereum) on the server. You will also find the genesis file, an example config, and the initial bootnodes located here.

To join the bloxberg network:

1.	Change the account section in exampleNode.toml to your node address and password to unlock the account. Also change the engine_signer section with your validator address.
2.	Launch parity with ‘parity --tracing on –config exampleNode.toml’. This will throw an error because the account doesn’t exist but will generate the folder structure.
3.	Add your keystore (UTC file) to ./bloxbergData/exampleNode/keys/Bloxberg
4.	Upon parity launch, it will also generate an enode address to download the blockchain. Add this address to bootnodes.txt file
5.	Run parity again with ‘parity --tracing on –config exampleNode.toml’ and the blockchain should initialize and start downloading the current state of the chain from the bootnodes.
6.	We recommend daemonizing the process and adding as a startup process to the server so the node is stable.
