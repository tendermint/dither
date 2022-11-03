# Dither

Decentralized messaging for all Cosmos blockchains

## What is Dither?

Dither is a specification for CosmosSDK (and other Tendermint-based) chains to
implement Twitter-like functionality by simply utilizing the transaction's MEMO
field.

By leveraging the MEMO field of a transaction, any Cosmos zone can host a
censorship-proof conversation on the blockchain, in a censorship resistant way.

Dither is not a product, but a specification. Anyone can create a Dither
compliant blockchain, and anyone can create a Dither compliant message browser.

## How does it work?

### Dither spec 0.1

1. Use the transaction's MEMO field to record a Dither message. The MEMO must
   start with a "#" character. Any spaces immediately following the "#" must be
   discarded. Transactions with empty memo fields are ignored for the purpose
   of Dither.

2. Viewers such as blockchain explorers must display the first signer's bech32
   address. The message must be sanitized and escaped so as to prevent scripts
   from runnning. For safety, links should NOT be clickable, but remain as
   plaintext.

3. That's it.

The spec is intentionally kept simple, so as to allow convention to be formed
by the community. Name resolution and accountable recommendations and indexing
are left as an exercise for the community to be solved for later versions of
the Dither spec, to be submitted as pull requests.

_NOTE: This is perhaps too minimal, and not safe enough. Please submit a PR_

## Why do we need Dither?

The Facebook/Cambridge Analytica scandal has already proven that private
interests can work with private social media companies to even sway government
elections.

Presented with no further comment:

 * "You take a vaccine, and a year goes by, and everybody's fine. Then, you
   say, 'Okay, that's good. Now let's give it to five hundred people.' Then a
   year goes by and everybody's fine. So, well, then, let's give it to thousand
   of people, and then you find out that IT TAKES TWELVE YEARS for all hell to
   break loose!  And then, what have you done?" - Dr. Anthony Fauci (Feb. 1999)

 * "The world today has 6.8 billion people; that's headed up to about 9
   billion.  Now if we can do a really great job on new vaccines, healthcare,
   reproductive health services, we can lower that by perhaps 10 or 15
   percent." - Bill Gates, TED Talk 2010.

 * "The Bill and Melinda Gates Foundation announced a new $250 million
   commitment on Thursday, adding to the foundation’s total investment to $1.75
   billion into combating COVID-19 through vaccine development and
   distribution." - abcnews.go.com

 * "Gates Foundation now WHO’s biggest funder" - indiatimes.com

 * "YouTube doesn't allow content that spreads medical misinformation that
   contradicts local health authorities’ (LHA) or the World Health
   Organization’s (WHO) medical information about COVID-19." - google.com

 * "DHS plans to target inaccurate information on “the origins of the COVID-19
   pandemic and the efficacy of COVID-19 vaccines, racial justice, U.S.
   withdrawal from Afghanistan, and the nature of U.S. support to Ukraine.”" -
   https://theintercept.com/2022/10/31/social-media-disinformation-dhs/

Now with Turing-test passing AI readily available as open source platforms, the
singularity is already here, and centralized social media platforms can now
more than ever be manipulated by near-sentient AI bots with or without the
paid consent of the company.

