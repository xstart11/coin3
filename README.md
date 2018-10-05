CASAX Core integration/staging repository

[Web](https://casax.cc)

<a href="https://discord.gg/9rS5Rpu"><img src="https://discordapp.com/api/guilds/489548449704968193/embed.png" alt="Discord server" /></a>

[Explorer](http://explorer.casax.cc)

=====================================

### Coin Specs
<table>
<tr><td>Coin name</td><td>CaSaX</td></tr>
<tr><td>Symbol</td><td>CSX</td></tr>
<tr><td>Algo</td><td>Quark Zerocoin</td></tr>
<tr><td>Type</td><td>PoS/MN</td></tr>
<tr><td>Block Time</td><td>60 Seconds</td></tr>
<tr><td>Min Staking age</td><td>3 hours</td></tr>
<tr><td>Halving</td><td>~2 years (1,000,000 blocks)</td></tr>
<tr><td>Rewards</td><td>MN 75% / POS 25%</td></tr>
<tr><td>Maturity</td><td>120 blocks</td></tr>
<tr><td>Max Coin Supply</td><td>180,000,000</td></tr>
<tr><td>Premine</td><td>0.07% (126000)</td></tr>
<tr><td>Block maturity</td><td>120 blocks</td></tr>
<tr><td>Masternode collateral</td><td>2000 CSX</td></tr>
</table>

### PoS Rewards Breakdown

<table>
<th>Block</th><th>Reward</th><th></th>
<tr><td>2-10000</td><td>0.1</td><td></td></tr>
<tr><td>10001-20000</td><td>20</td><td>PoS - 5 CSX, MN - 15 CSX</td></tr>
<tr><td>20001-30000</td><td>25</td><td>PoS - 6.25 CSX, MN - 18.75 CSX</td></tr>
<tr><td>30001-40000</td><td>35</td><td>PoS - 8.75 CSX, MN - 26.25 CSX</td></tr>
<tr><td>40001-50000</td><td>50</td><td>PoS - 12.5 CSX, MN - 37.5 CSX</td></tr>
<tr><td>50001-60000</td><td>35</td><td>PoS - 8.75 CSX, MN - 26.25 CSX</td></tr>
<tr><td>60001-70000</td><td>25</td><td>PoS - 6.25 CSX, MN - 18.75 CSX</td></tr>
<tr><td>70001-80000</td><td>20</td><td>PoS - 5 CSX, MN - 15 CSX</td></tr>
<tr><td>80001-1000000</td><td>15</td><td>PoS - 3.75 CSX, MN - 11.25 CSX</td></tr>
</table>


***

It is recommended [use the shell script](https://github.com/CaSaX/mn-install) to install a CaSaX Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

Quick installation of the CaSaX daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/CaSaX/casax-core.git
    cd casax-core
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip Casaxd
    sudo strip Casax-cli
    sudo strip Casax-tx
    cd ..

Running the daemon:

    Casaxd 

Stopping the daemon:

    Casax-cli stop

Demon status:

    Casax-cli getinfo
    Casax-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/CaSaX/casax-core/releases

P2P port: 9116, RPC port: 9115
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
