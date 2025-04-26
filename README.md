# Discord Prediction Market Bot

A Discord bot that allows users to create and participate in prediction markets.
Users can create markets for future events, trade shares, and earn virtual
currency by making accurate predictions.

## Usage

The state of the bot is stored in a `state.json` file so it persists across bot restarts.

Users start with \$1000.
They can spend \$50 to create a market with the `/create_market` command.
They can bet in markets by buying and selling YES and NO shares
with `/buy` and `/sell`.
A YES share is a contract that pays out \$1 if the market resolves YES,
and a NO share pays out \$1 if the market resolves NO.

The creator of a market can resolve it with `/resolve_market`,
saying the outcome was YES or NO.
The market creator can also resolve a market UNDO,
which undoes all the balance changes from users betting in the market.
This is useful for cases where it's unclear how to resolve a market due to an under-specified description.
It's also useful for conditional markets of the form "If X, then Y?" that can resolve UNDO if X doesn't happen.

### Commands

```text
  /help             Get help on how to use this bot
  /balance          Get the balance of a user
  /balances         Get the balances of all users
  /portfolio        Get the portfolio of a user
  /create_market    Create a market (costs $50)
  /list_markets     Display a list of active markets
  /show_market      Show a market
  /resolve_market   Resolve one of your markets
  /buy              Buy shares
  /sell             Sell your shares
  /tip              Send a tip to another user
  /register         Register slash commands
  /input_time       Test time input
```
