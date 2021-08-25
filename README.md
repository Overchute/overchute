<img src="https://github.com/Overchute/overchute/blob/main/overchute_name.png" />

# Crowdsale Protocol - MVP user flows

- Creator produces a work of intellectual property (IP) and drafts an open licence for its release.
- Creator navigates to Overchute website and clicks the"Create new crowdsale" button.
- In input form, Creator enters:
  - Offer price (in cycles token XTC) (must be >=0)
  - End date (must be in the future)
  - XTC wallet address into which raised funds must be paid
  - Reads a description of the crowdsale rules and clicks "Confirm" button
- Overchute creates a crowdsale with the status "open', and generates a unique URL, displaying it for Creator to copy.
- Creator copies the crowdsale offer URL, and pastes it into a suspensive condition in the open licence, and publishes the open licence.
- Creator communicates the crowdsale to the community, pointing them to the IP product, the published open licence and the URL where they can contribute.
- Contributor navigates to crowdsale URL. The app displays:
  - Offer status (open/failed/fulfilled)
  - End date
  - Crowdsale rules
  - XTC wallet address for contributions, for Contributor to copy.
- Contributor sets up an XTC wallet and makes a payment to the copied crowdsale wallet address.
- On the crowdsale end date, Overchute calculates total contributions, and does the following:
  - If total contributions are less than the offer price:
    - Set crowdsale status to "failed".
    - Refund all contributions to the wallet addresses from which they came.
  - If total contributions are greater than or equal to the offer price:
    - Set crowdsale status to "fulfilled".
    - Pay offer price to the wallet address specified by the Creator.
    - Calculate the Platform's share of the overshoot, and pay it to the platform's wallet address.
    - Calculate the Creator's share of the overshoot and pay it to the wallet address specified by the Creator.
    - Calculate the total Contributors' share of the overshoot, and the portion due to each Contributor, and pay each to the wallet address from which the contribution came.
- IP User sees the open licence for the IP product and wants to know if the suspensive condition has been fulfilled.
- IP User navigates to the crowdsale URL in the open licence. The app displays the end date and crowdsale status (open/failed/fulfilled).

Notes for MVP design:

- User accounts or authentication are not required for any participants: Creator, Contributors or IP Users. (Future features will require the creation of a user account for each Creator.)
- When a Creator creates a crowdsale, it is open for contributions immediately, and cannot be modified.
- It must not be possible for a Contributor to see what other contributions have been made by looking at other payments to the same wallet address on the public transaction ledger.
