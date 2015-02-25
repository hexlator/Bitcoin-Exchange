# Bitcoin-Exchange

#installation 

Open application/config/config.php

edit the very bottom:

    define('DB_TYPE', 'mysql');
    define('DB_HOST', '127.0.0.1');
    define('DB_NAME', 'changeme');
    define('DB_USER', 'changme');
    define('DB_PASS', 'exchange1234');
    define('URL_PROTOCOL', 'https://'); //if you're not using https

in application/models/model ledit your rpc details
   
    public function btccoin()
    {
      //require APP . 'libs/easybitcoin.php';
       require APP . 'libs/jsonRPCClient.php';
       $bitcoin = new jsonRPCClient("");
    return $bitcoin;    
}

something like https://username:password@127.0.0.1:8332

Download notepad++ and put all files in a folder and ctrl + f, go to find in files, and replace Cryptxe with your exhcnage's name (I may use the $site->sirename; variable for this but until then do the notepad++ thng

Go to: public/js/voice.js and change all the domains to your own.

Import the sql file in to your database.


#translating

If adding new features, echo words like 

    _ex("my word here"); 

then you can download poedit and translate it to other languages.

#general
'
If you want to add staff memebers, to access mod cp or support tickers, in the row staff add 1
I may eventually add an install file, but for the time being I'll just leave it as manual install

Feel free to fork the resp to edit and create or update more features

#features

Includes lots of features
2factor authentication -- if this feature is set; to login the user needs to input the code from their phone.
Buy and sell coins
Built in messaging system, message the user when they add IP's etc
Whitelist IPs (if a user set an IP they will only be able to login with that IP on that account
Login history
Trade history
View open orders
View trades, which has an invoice that you can print
Public API
Graph chart to show prices for the day and volume On the dashboard the title has an updating price for the market you are viewing, so you can watch Youtube videos or browse the internet and view the market price without having to be on the website
Voice trading,trade using your voice.
