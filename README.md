# Auto-MM-bot
Auto Middleman bot for Discord which handles LTC transactions

This is a bot I made in my free time originally for reputation, but I don't sell on Discord anymore so I'm just releasing it here for all you skids to say "WE HAVE VERY FIRST AUTO MM BOT ON THE MARKET" (I'm a skid).

# Cool stuff
- I use the Blockcypher API, API keys can be obtained here -> https://accounts.blockcypher.com/
- I also used coinGeckoAPI which you don't need to get an API key for.
- Each transaction has a new wallet created for them and saves the private key and address to a log file.
- Uses tickets for deals and Has a dispute system. Also has transcripts.
- Auto Payout to seller's wallet.
- Auto payment detection, along with a limit to not use up too many API uses.
- Buyers must confirm they got the valid product before a payout and if they don't a dispute starts.

# Example of how a deal would go
Seller: Opens ticket.
Bot: Asks for the user ID of the buyer.
Seller: gives the user ID.
Bot: Adds the User ID to the ticket.
Bot: Asks Seller how much money they will receive.
Seller: Answers with a number (let's say 1).
Bot: Asks seller for their LTC Wallet Address.
Seller: Gives them their LTC Wallet Address.
Bot: Tells Buyer to send $1 worth of LTC to the Bot's newly generated wallet address.
Buyer: Sends LTC, If not sent within 5 minutes the deal will be canceled (I suggest making a /recover command in case they sent it but it didn't get all confirmations on time, I may make it in the future).
Bot: Confirms they got the funds.
Bot: Confirms the funds have been confirmed.
Bot: Tells seller to send the product in the same channel, Optional but sending in channel makes it more secure for buyer & seller in case of a dispute and it needs to go into manual review.
Bot: Creates a prompt for ONLY the buyer to click to confirm the product's validity.
Buyer: Clicks the button.
Bot: If the button that is clicked is 'Confirmed' It will auto payout to the seller's wallet, if it's 'Dispute' it will not auto payout and tell the seller to create a dispute.
Bot: Saves Transcript.

# IMPORTANT
- The bot needs the SELLER to open the ticket.
- The bot doesn't use a Database it uses a list, I didn't want to add a DB so restarting the bot will reset the deals.
- Probably other stuff I forgot to mention.

# Commands
- /close - closes a ticket | admin only
- /get_private_key - gets a private key based on a deal id | admin only
- /get_wallet_balance - checks wallet balance
- /new_api_key - changes API key | admin only | not done
- /send_ltc - sends LTC to a wallet address through a bots address | admin only


# Will post files Later when im avaible
