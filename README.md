# Soroban-Accelerated-Bootcamp-in-India-Final-Project



# Crowdfunding Dapp 
=================================





Getting Started
===============

Install Dependencies
--------------------
1. `rustc` >= 1.71.0 with the `wasm32-unknown-unknown` target installed. 
2. `soroban-cli`. , but instead of `cargo install soroban-cli`, run `cargo install_soroban`. 
3. If you want to run everything locally: `docker` (you can run both Standalone and Futurenet backends with it)
4. Node.js v18
5. [Freighter Wallet](https://www.freighter.app/) 



Run Backend
-----------


### Option 1: Deploy on Futurenet

0. Make sure you have soroban-cli installed, as explained above

1. Deploy the contracts and initialize them

       npm run setup

2. Select the Futurenet network in your Freighter browser extension

### Option 2: Run your own Futurenet node

1. Run the backend docker container with `./quickstart.sh futurenet`,

2. Load the contracts and initialize them

   Use your own local soroban-cli:

       ./initialize.sh futurenet http://localhost:8000

3. Add the Futurenet custom network in Freighter 

4. Add some Futurenet network lumens to your Freighter wallet.

   Visit https://laboratory.stellar.org/#create-account, and follow the instructions to create your freighter account on Futurenet.

### Option 3: Localnet/Standalone

0. If you didn't yet, build the `soroban-preview` docker image, as described above:

       make build-docker

1. In one terminal, run the backend docker containers and wait for them to start:

       ./quickstart.sh standalone


2. Keep that running, then deploy the contracts and initialize them:

   You can use your own local soroban-cli:

       NETWORK=standalone npm run setup

 
3. Add the Standalone custom network in Freighter


4. Add some Standalone network lumens to your Freighter wallet.

   1. Copy the address for your freighter wallet.
   2. Visit `http://localhost:8000/friendbot?addr=<your address>`


Frontend
--------

Now that you're running the backend, you can run the development server:

    npm run dev

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

