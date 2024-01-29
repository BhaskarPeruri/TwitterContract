# Twitter Smart Contract


The contract includes access control checks, ensuring that only authorized users or operators can perform certain actions.

It provides functions to retrieve tweets and messages based on user and count criteria.


# **Functions of the contract**

**Internal Functions:**

1.'_tweet' Function:

    Internal function to create a new tweet.

    Checks if the caller has access or is an operator.

    Adds the tweet to the tweets mapping and updates related mappings.


2.'_sendMessage' Function:

    Internal function to send a message.
    
    Checks if the caller has access or is an operator.
    
    Adds the message to the conversations mapping.

**External Functions:**


1.'tweet' Function:

    Public function to create a tweet.
    
    Calls the internal _tweet function with the caller's address and tweet content.


2.'tweet' Function (Overloaded):

    Public function to create a tweet on behalf of another user.
    
    Calls the internal _tweet function with the specified user's address and tweet content.


3.'sendMessage' Function:

    Public function to send a message.
    
    Calls the internal _sendMessage function with the recipient's address and message content.


4.'sendMessage' Function (Overloaded):

    Public function to send a message on behalf of another user.
    
    Calls the internal _sendMessage function with the specified sender's and recipient's addresses, and message content.
    

5.'follow' Function:

    Public function to follow another user.
    
    Adds the followed user's address to the following mapping.


6.'allow' Function:

    Public function to grant operator privileges to another user.


7.'disallow' Function:

    Public function to revoke operator privileges from another user.


8.'getLatestTweets' Function:

    Public view function to get the latest tweets.
    
    Returns an array of Tweet structs based on the specified count.


9.'getLatestofUser' Function:
   
    Public view function to get the latest tweets of a specific user.
      
    Returns an array of Tweet structs based on the specified count for the given user.

