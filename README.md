# KryptoJobs2o

## Background
You work at a startup that’s building a new and disruptive application named KryptoJobs2Go (a fictitious application). Your customers can use KryptoJobs2Go to find fintech professionals from a list of candidates, hire them, and then pay them. As the lead developer, you’ve been tasked with integrating the Ethereum blockchain network into the application. The purpose is to enable the customers to instantly pay their hired fintech professionals with cryptocurrency.

## What You're Creating
The completed `fintech_finder.py` file, which contains the code that’s associated with the web interface of your application. (The included code is compatible with the Streamlit library.) You’ll write all your code for this Challenge in this file.

Note that by using `import` statements, you’ll integrate the `crypto_wallet.py` Python script into the code in this file.
A `README.md` file that includes screenshots to confirm that by assuming the role of a KryptoJobs2Go customer, you successfully created an Ethereum transaction, including the gas estimate, that pays a KryptoJobs2Go candidate for their work.


## Step 1: Import Ethereum Transaction Functions into the KryptoJobs2Go Application
In this section, you'll import several functions from the `crypto_wallet.py` file into the `fintech_finder.py` file. Note that the latter file contains the code for the customer interface of the KryptoJobs2Go application. And, you’ll import the functions to add wallet operations to this application. In this section, you’ll also assume the role of a KryptoJobs2Go customer (that is, you’ll provide your Ethereum wallet and account information to the application).

To do all this, complete the following steps:

 1) Review the code in the `crypto_wallet.py` file. Note that the Ethereum transaction functions that you’ve built throughout this module have been incorporated into Python functions that allow you to automate the process of accessing them. The Ethereum transaction functions include `wallet`, `wallet.derive_acount`, `get_balance`, `fromWei`, `estimateGas`, `sendRawTransaction`, and others.

2) Add your mnemonic seed phrase (which Ganache provided) to the `SAMPLE.env` file. Then rename the file to `.env`.

3) Open the `fintech_finder.py` file. Near the beginning of the file, after the provided import statements, import the following functions from the `crypto_wallet.py` file:

- generate_account

- get_balance

- send_transaction

4) In the Streamlit sidebar section of code, create a variable named `account`. Set this variable equal to a call to the `generate_account` function. Note that this function will create the hierarchical deterministic (HD) wallet and the Ethereum account of the KryptoJobs2Go customer (in this case, you).

5) In the same section of code, define a new `st.sidebar.write` function that displays the balance of the customer account. In this function, call the `get_balance` function, and pass it your Ethereum `account.address`.
