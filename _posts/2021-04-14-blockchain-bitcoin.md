---
layout: default
title: "BlockChain deep"
date: 2021-04-14 10:09:00 -0400
categories: blockchain
permalink: /:categories/:title
---

LINK: [How Bitcoin Works Under the Hood](https://www.blogger.com/#)

## What is Bitcoin?

![ledgers](https://1.bp.blogspot.com/-aRwHJuD_qLE/YGoB4BSHVlI/AAAAAAAALQY/ntMCW9ty2PQiahVANZfFL8Sg9yHdQwXbACPcBGAYYCw/s16000/1.png "ledgers")

At its core, Bitcoin is just a digital file that lists accounts and money like a ledger. A copy of this file is maintained on every computer in the Bitcoin network. (update: you don't have to maintain a ledger just to use Bitcoin to send and receive money, this is for people who want to help maintain the system)  
These numbers don’t represent anything in the physical world, they only have value because people are willing to trade real goods and services for a higher number next to their account, and believe that others will do the same. The numbers only have value because we believe they have value, just like any other fiat currency

![ledgers](https://1.bp.blogspot.com/-Ct6E5wufFwM/YGoCT0NQgVI/AAAAAAAALQk/p8-Zjxl6qTkopN9NL_9v94eUJZ274kl5gCPcBGAYYCw/s16000/3.png)  
![ledgers](https://1.bp.blogspot.com/-Ct6E5wufFwM/YGoCT0NQgVI/AAAAAAAALQk/p8-Zjxl6qTkopN9NL_9v94eUJZ274kl5gCPcBGAYYCw/s16000/3.png)

To send money, you broadcast to the network that the amount on your account should go down, and the amount on a receiver’s account up. Nodes, or computers, in the Bitcoin network, apply that transaction to their copy of the ledger and then pass on the transaction to other nodes. This, with some math-based security, is really all there is--a system that lets a group of computers maintain a ledger.  
While this may sound similar to the way a bank maintains a ledger, the fact that the ledger is maintained by a group rather than a single entity introduces a number of important differences. For one, unlike at a bank where you only know about your own transactions, in Bitcoin, everyone knows about everyone else’s transactions.

## How Sending Money in Bitcoin Works

At a basic level, for Alice to send money to Bob, she simply broadcasts a message with the accounts and the amount:

    “Send 5.0 BTC from Alice to Bob.”

Every node that receives it will update its copy of the ledger, and then pass along the transaction message. But how can the nodes be sure that the request is authentic, that only the rightful owner has sent the message?  
Bitcoin rules require a kind of password to unlock and spend funds, and this password is what’s called a “Digital Signature.” Like a real handwritten signature, it proves the authenticity of a message, but it does so through a mathematical algorithm that prevents copying or forgery in the digital realm.  

## Digital signature  

![digital signature](https://1.bp.blogspot.com/-Xlz9U8g0BNM/YGoHhljq92I/AAAAAAAALQ0/vRznDhgbJus4neKs1N9Ekp8A9HmrRHQqwCPcBGAYYCw/s16000/4.png)  
![digital signature](https://1.bp.blogspot.com/-a8lkaQWPZFQ/YGoHhiYlpsI/AAAAAAAALQ4/83Yn39jaVl4sB6xef1gcRgOOlNjzKs7YACPcBGAYYCw/s16000/5.png)

Unlike a simple static password, a completely different Digital Signature is required for every transaction. Keep in mind that in Bitcoin, you’re dealing with complete strangers, so you never want to reveal a password that could be copied and reused by someone else.

![process](https://1.bp.blogspot.com/-VAxfRtcz7s0/YGoWKqQRqiI/AAAAAAAALcA/bGHWYd7qm6ghWCtbD0JeWJ9UTiHdRZlaACPcBGAYYCw/s16000/image010.png)

A Digital signature works by utilizing two different but connected keys, Private-Key to create a signature and a Public-Key that others can use to check it. The Public-Key is the wallet address.

![message](https://1.bp.blogspot.com/-KZv4en7_d4Y/YGoWK8tVtGI/AAAAAAAALbw/VRTLmSw3pekGqCEaXD7NTxfj6fadtKDBwCPcBGAYYCw/s16000/image012.png)

To spend money you have to prove that you are the owner of this wallet. You do that by generating a digital signature from a transaction message and your private key.

![message](https://1.bp.blogspot.com/-kjx3sweiBm0/YGoWLSuP7ZI/AAAAAAAALcI/9HFJSsqvL4AnYfxGzsZfluEjt2sQsTi9ACPcBGAYYCw/s16000/image014.png)

Other nodes in the network can use that signature in a different function to verify that it corresponds with your public key.  
Through the math behind the digital signature they're able to verify that the sender owned the private key without actually seeing the private key.

![message](https://1.bp.blogspot.com/-C_c85Bjbk2M/YGoWLnCafKI/AAAAAAAALcQ/Sawferl3Y8wwBHP_NsebT14ys2m9tAqrwCPcBGAYYCw/s16000/image016.png)

Because the signature depends on the message it will be different for every transaction and therefore can't be reused by someone for a different transaction.  
This dependence on the message also means that no one can modify the message as any changes to the message would invalidate the signature.
