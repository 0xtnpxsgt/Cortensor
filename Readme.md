![image](https://github.com/user-attachments/assets/5980218d-ac4c-411b-8a34-048eed7c85c7)


# Cortensor Node Installation:

## Requirements :

Minimum : VPS Requirements : Contabo VPS2 - Region WEST/EAST

- ∞ CPU+ / ∞ GB RAM /  ∞ MBit/sec Download Speed

Recommended :

- ∞+ CPU ( Hızlı ) / ∞+ GB RAM / ∞+ MBit/sec Download Speed

To update and upgrade system packages, run the following command:

```bash
sudo apt update -y && sudo apt upgrade -y
```
## 2. Install the necessary packages:

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen unzip lz4 -y
```

## 3. Let's Pull the Files:

```bash
git clone https://github.com/cortensor/installer
```

## Let's go into the directory:

```bash
cd installer
```

## Docker - Ipfs - Install .sh : 

```bash
./install-docker-ubuntu.sh
```
```bash
./install-ipfs-linux.sh
```
```bash
./install-linux.sh
```
- Create a password for the Deploy user and remember it well.
## Deploy : 

```bash
cd
```

```bash
cp -Rf ./installer /home/deploy/installer
```

```bash
chown -R deploy.deploy /home/deploy/installer
```

## Deploy User:

```bash
sudo su deploy
```

## Exit to Main Directory:
```bash
cd ~/
```

## Creating Keys:

```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool gen_key
```
## Fund Your Wallet :
- Send 5 ETH ARB Sepolia to Miner Address
- Join Discord: https://discord.gg/cortensor

## Let's Register :
```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool register
```

## Stake :
1. Swap on uniswap at least 10$ worth of $COR Ethereum Mainnet, CA : 0x8e0EeF788350f40255D86DFE8D91ec0AD3a4547F
2. Stake $COR at Pool 3(84 Days) https://stake.cortensor.network/ (Stake 95% Balance)
- Fill Form: [Google Forms](https://docs.google.com/forms/d/e/1FAIpQLSfNEGWnWO10pnMPu5uX6yk4mZ9qf4fOxvTqcsFaO9V88OQFJw/viewform)
- Then tag and post to admin on this discord channel

- After your address whitelisted, run this command to register

## Let's Check: 

```bash
/usr/local/bin/cortensord ~/.cortensor/.env tool verify
```

## Let's start:

```bash
sudo systemctl start cortensor
```

- Monitor Node : https://dashboard-alpha.cortensor.network/

## After running node, post in this discord channel too :

- miner address : your_miner_address
- staking address : your_staking_wallet_address
- discord : your_discord_username
- telegram : your_telegram_usernam

## If you want to stop:

```bash
sudo systemctl stop cortensor
```


