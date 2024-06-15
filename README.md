# Decentralized-Voting-System-Using-Ethereum-Blockchain

#### The Decentralized Voting System using Ethereum Blockchain is a secure and transparent solution for conducting elections. Leveraging Ethereum's blockchain technology, this system ensures tamper-proof voting records, enabling users to cast their votes remotely while maintaining anonymity and preventing fraud. Explore this innovative project for trustworthy and decentralized voting processes.


## Features
-  Implements JWT for secure voter authentication and authorization.
-  Utilizes Ethereum blockchain for tamper-proof and transparent voting records.
-  Removes the need for intermediaries, ensuring a trustless voting process.
-  Admin panel to manage candidates, set voting dates, and monitor results.
-  Intuitive UI for voters to cast votes and view candidate information.

## Requirements
- Node.js (version – 18.14.0)
- Metamask
- Python (version – 3.9)
- FastAPI
- MySQL Database (port – 3306)

## Screenshots

![Screenshot (1144)](https://github.com/ankursingh24/Dentcentralized-Voting-System-Using-Ethereum-Blockchain/assets/99939932/e5811e2e-f72a-4c12-9988-db5df416c769)


![Screenshot (1145)](https://github.com/ankursingh24/Dentcentralized-Voting-System-Using-Ethereum-Blockchain/assets/99939932/4b2a0c3b-97e0-42df-9d10-8c6ab7f3b0e8)

## Installation

1. Open a terminal.

2. Clone the repository by using the command

3. Download and install [Ganache](https://trufflesuite.com/ganache/).

4. Create a workspace named <b>developement</b>, in the truffle projects section add `truffle-config.js` by clicking `ADD PROJECT` button.

5. Download [Metamask](https://metamask.io/download/) extension for the browser.

6. Now create wallet (if you don't have one), then import accounts from ganache.

7. Add network to the metamask. ( Network name - Localhost 7575, RPC URl - http://localhost:7545, Chain ID - 1337, Currency symbol - ETH)

8. Open MySQL and create database named <b>voter_db</b>. (DON'T USE XAMPP)

9. In the database created, create new table named <b>voters</b> in the given format and add some values.

           CREATE TABLE voters (
           voter_id VARCHAR(36) PRIMARY KEY NOT NULL,
           role ENUM('admin', 'user') NOT NULL,
           password VARCHAR(255) NOT NULL
           );
   <br>

        +--------------------------------------+-------+-----------+
        | voter_id                             | role  | password  |
        +--------------------------------------+-------+-----------+
        |                                      |       |           |
        +--------------------------------------+-------+-----------+

12. Install truffle globally
    
        npm install -g truffle

 12. Install truffle  contracts globally
    
    npm i --save-dev @truffle/contract

    

14. Go to the root directory of repo and install node modules

        npm install

15. Install python dependencies

        pip install fastapi mysql-connector-python pydantic python-dotenv uvicorn uvicorn[standard] PyJWT

## Usage

#### Note: Update the database credentials in the `./Database_API/.env` file.

1. Open terminal at the project directory

2. Open Ganache and it's <b>development</b> workspace.

3. open terminal in project's root directory and run the command

        truffle console
   then compile the smart contracts with command

        compile
   exit the truffle console

5. Bundle app.js with browserify
    
        npm i browserify
   
       browserify ./src/js/app.js -o ./src/dist/app.bundle.js
   
2. Start the node server server
    
        node index.js

3. Navigate to `Database_API` folder in another terminal
    
        cd Database_API
    then start the database server by following command

        uvicorn main:app --reload --host 127.0.0.1

4. In a new terminal migrate the truffle contract to local blockchain
    
        truffle migrate

You're all set! The Voting app should be up and running now at http://localhost:8080/.<br>




## If you like this project, please give it a 🌟.
## Thank you 😊.
