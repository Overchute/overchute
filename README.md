<img height=320 src="https://github.com/ferMartz/overchute/blob/main/overchute.png" />

# Overchute

Intellectual Property Protocol

- Allow anyone to create a pseudonymous user account, using Internet Identity or other means.

- Allow users to deposit and withdraw some stable cryptocurrency (probably WTC or XTC).

- Allow users to create an offer:
- Generate a unique ID for the offer, with a unique URL for direct navigation to the offer. The offer status starts as 'draft'.
- Allow the creator to specify the offer price and the crowdsale duration.
- Allow the creator to trigger the start of the crowdsale, changing offer status to 'open'.
- Allow the creator to decrease the offer price at any time while the offer is open.
- Allow users to contribute to a specific open offer:
- Make a contribution of a desired amount. (For the MVP this can be a simple pledge, not a matching pledge.)
- Increase the contribution at any time while the offer is open.

- Note: Contributions must be held in such a way that they cannot be linked to a specific offer by inspecting the blockchain ledger (until the offer is fulfilled).
  Execute the rules of the mechanism:
  When the crowdsale duration is completed
  Calculate the total contribution and the overshoot.
  If overshoot is less than zero:
  Change the status of the offer to 'failed'.
  Transfer each contribution back to its contributor.
  If overshoot is greater than or equal to zero:
  Change the status of the offer to 'fulfilled'.
  Transfer the offer price to the creator.
  Calculate the platform fee and transfer it to the platform.
  Calculate the creator's share of the overshoot and transfer it to the creator.
  Calculate the contributors' share of the overshoot, and transfer a portion to each contributor in proportion to their contribution.
  Allow anyone to search for a specific offer, and inspect:
  the status of the offer (draft/open/failed/fulfilled) and the timestamped status changes
  for fulfilled offers: the offer price and the total contributed amount (since this can be inferred from ledger transactions anyway once transfers are made)
  Note: The dApp code must necessarily be open source. Because the offer price and contributions are not disclosed, users must be able to inspect the smart-contract implementing the Double-Blind Crowdsale Protocol to verify that it will function as claimed.
