---
layout: default
title: Intro
nav_order: 
---
## Guia: Criando um Nó de Bitcoin em um Raspberry Pi
{: .no_toc }

## Índice
{: .no_toc .text-delta }

1. TOC
{:toc}


Sempre fui fascinado pelo assunto *Liberdade*! Em 2103 em meio a videos de opiniões políticas e socias sobre a promoção da liberdade me deparei com um vídeo de um velho conhecido, Daniel Fraga, apresentando uma tecnologia chamada Bitcoin. Fiquei desconfiado e ao mesmo tempo encantado com o novo *dinheiro digital, descentralizado e incensurável*. Comecei a estudar a tecnologia o tanto quanto podia e cheguei até a minerar. Minha primeira carteira de bitcoin foi o software original do Bitcoin (Bitcoin-qt), o mesmo que fazemos um *full-node* (Nó de Bitcoin). Sem saber, na época, já estava contribuindo ara a rede, além de ter meu próprio banco, livre e de código aberto. Aqui pretendo ensinar a fazer um nó completo de Bitcoin de baixíssimo custo.


![RaspiBolt Logo](images/raspibit_logo.png)

## Why am I excited about Bitcoin and Lightning?

**Bitcoin as new technology** is an incredibly interesting endeavor, especially because of its interdisciplinary nature. **Bitcoin as sound money** is going to have a major impact on economic principles and society as a whole. In my opinion, a solid, anti-fragile base layer for this future monetary network is the killer app for blockchains and will be more important than the most novel feature of competing altcoin projects.

At the moment, Bitcoin is more of a store of value and not really suited for small everyday transactions. Due to limitations of the blockchain and the growth of its usage, fees have risen and business models relying on cheap transactions are being priced out. This is fine. **Truly decentralized blockchains are a scarce resource** and cannot scale to accommodate all global transactions. The current scaling pains are a great motivator to build better technology to scale exponentially, as opposed to just making everything bigger for linear scaling.

This is where the **Lightning Network** comes in. As one of several new blockchain “extensions”, its promise is to accommodate nearly unlimited transactions, with instant payment confirmation, minimal fees and increased privacy. It sounds almost too good to be true, but in contrast to ubiquitous ICO with their own token, this technology is well researched, committed to the cypherpunk open-source ethos and leverages the solid underpinnings of Bitcoin.

Bitcoin's security model requires both full nodes and miners to be decentralized. While the full-node-using economy must be decentralized to stop fake bitcoins that do not abide to consensus from being accepted as payments, the miners must be  decentralized to stop censorship of transactions and to make  transactions irreversible. 

To preserve the decentralized nature of this monetary system, I think it is important that everybody can run their own trustless Bitcoin full node, preferably on cheap hardware like a Raspberry Pi. If Bitcoin is digital gold, then a full node wallet is your own personal goldsmith who checks for you that received payments are genuine. 

This is why I set out to build my **RaspiBolt** and think that I have now - through numerous iterations - quite a good configuration that I would like to share as my modest contribution to the community. I am not a systems specialist, so please feel free to point out improvements.

## About this guide
### Structure

1. Introduction (this page)
2. [Preparations](raspibolt_10_preparations.md): get all required parts and start downloading the mainnet Blockchain
3. [Raspberry Pi](raspibolt_20_pi.md): set up and configure the Pi as a secure Linux server
4. [Bitcoin](raspibolt_30_bitcoin.md): install and configure the Bitcoin Core software as a Full Node, on testnet
5. [Lightning](raspibolt_40_lnd.md): install and configure the Lightning Network Daemon (LND), on testnet
6. [Mainnet](raspibolt_50_mainnet.md): after you are comfortable with your setup, switch to Bitcoin mainnet
7. [FAQ](raspibolt_faq.md): frequently asked questions and further reading
8. [Updates](raspibolt_updates.md): keep track of changes

### Purpose

My aim is to set up a Bitcoin and Lightning node that
* is as fully validating Bitcoin Full Node and does not require any trust in a 3rd party,
* is reliably running 24/7, 
* is part of and supports the decentralization of the Lightning network by routing payments and 
* can be used to send and receive personal payments using the command line interface.

This server is set up without graphical user interface and is used remotely using the Secure Shell (SSH) command line. In the future, this server should function as my personal backend for desktop and mobile wallets, but I haven’t found a good solution to this yet. So, command line it is for the moment.

**The good old days**: this was the original goal of this guide, back in 2017, simply buying a Blockaccino.

[![](images/00_blockaccino_goal.png)](https://vimeo.com/258395303)

**Wishlist for further enhancements**

- [x] Bitcoin / Lightning desktop wallet support: Electrum / Zap Desktop  
- [x] Bitcoin mobile wallet support: Zap iOS / Shango  
- [x] Hardware wallet support: Electrum + HW wallet
- [ ] Full backup, incl. Lightning channel states

### Target audience

This guide strives to give simple and foolproof instructions. But the goal is also to do everything ourselves, no shortcuts that involve trust in a 3rd party allowed. This makes this guide quite technical and lengthy, but I try to make it as straightforward as possible and explain everything for you to gain a basic understanding of the how and why.

If you like to learn about Linux, Bitcoin and Lightning, this guide is for you.

### A word of caution
All components of the Lightning network are still under development and we are dealing with real money here. So this guide follows a conservative approach: first setup and test everything on Bitcoin testnet, then - once you are comfortable to put real money on the line - switch to Bitcoin mainnet with a few simple changes.

---
Get started: [Preparations >>](raspibolt_10_preparations.md)
