# Minting NFTs on Algorand Testnet
This repository provides a script to mint NFTs on the Algorand Testnet. You can use this script inside a GitHub Codespace and view the minted NFTs using the Pera Explorer.

## Features
Generate a new Algorand account or use an existing one.

Load metadata from a JSON file and create a hash for the NFT.

Mint NFTs on the Algorand Testnet.

View minted NFTs on the Pera Explorer. 
p.s Algorand Pera Wallet is available on IOS and Andriod check your app stores!

## Getting Started
### Clone the repository 
``` 
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name 
```

### Or create new Codespace (beginner friendly)
To enter the codespace just click the green code button on the repo page and click 'create new codespace'.

### Set up the environment
Run the provided setup script to install dependencies and set up the environment:

``` Bash
sh algorand_setup.sh
```
### Prepare metadata
Create a metadata.json file in the root of the repository. This file should contain the metadata for the NFT. You can use the following template provided within the repo:

``` JSON
{
    "name": "TBD",
    "description": "TBD",
    "image": "TBD",
    "decimals": 0,
    "unitName": "TBD",
    "image_integrity": "sha256-<your-image-hash>",
    "image_mimetype": "image/jpg",
    "properties": {
        "example_property_1": "value1",
        "example_property_2": "value2"
    }
}
```

### Run the script
Execute the script to mint the NFT:

```
python main.py
```

# Script Overview
Here's a brief overview of the main.py script:

### Generate New Account

The `generate_new_account()` function creates a new Algorand account and returns the address and mnemonic passphrase.

### Write Mnemonic to .env

The `write_mnemonic_to_env()` function saves the mnemonic passphrase to a .env file.

### Load Passphrase from .env

The `load_passphrase_from_env()` function retrieves the mnemonic passphrase from the .env file.

### Connect to Algorand Testnet

The `connect_to_algorand_testnet()` function establishes a connection to the Algorand Testnet.

### Load Metadata from File

The `load_metadata_from_file(file_path)` function loads metadata from a JSON file and returns it as a string.

### Create Metadata Hash

The `create_metadata_hash(metadata_str)` function creates a hash of the metadata using sha512_256.

### Create NFT Asset

The `create_nft_asset(algorand, account, metadata_hash)` function creates and sends a transaction to create the NFT asset on the Algorand Testnet.

### Viewing the NFT
You can view the minted NFT on the Pera Explorer by searching for the NFT asset ID.

If you have minted your NFT you can then search the asset ID on the Algorand Testnet with Pera Explorer here: https://testnet.explorer.perawallet.app/

# Enjoy experiementing with Algorand?
Come join the algodevs community with our active disord: https://discord.com/invite/algorand
Watch more algorand content in bytes or marathons with the Algodevs Youtube channel: https://www.youtube.com/@algodevs
