# website-regulation-a-plus-Crowdsale

The web front end for C4Coin's Regulation A+ Crowdsale, allowing investors to register, and providing a range of investor services.

* `develop` — [insert CircleCI badge]
* `master` — [insert CircleCI badge]

## Requirements

### Before and During the Crowdsale

* Describe `CO2KN` investment opportunity with appropriate Reg A+ disclaimers

  - Explain and advertise smart contract for equity token issuance
  - Links to whitepaper and public site
  - Possible integration to CMS, or just static content

* Account registration/login with ID verification and ETH address linking

  - Two factor Auth support
  - Name of the shareholder
  - Complete mailing address of the stock shareholder including contact number
  - Upload KYC Data

    - privacy statement / security of file uploads / file retention policy

  - Supply/update linked ETH address

* Password reset
* Display info about the Crowdsale (progress, duration, time remaining, shares sold/remaining etc.)

    - see SEC Terms and Conditions below.

### After the Crowdsale

  - View stockholder materials (e.g. matters submitted to stockholders for review/vote)

### SEC Requirements

1. Terms (As defined by the SEC):

    - Price per share (USD)
    - Nature of securities

        Awaiting feedback on what this means.

    - Closing date

        Will be pulled from the Crowdsale Contract itself.

    - Amount of securities offered

        Will be pulled from the Crowdsale Contract itself.

2. Implied Terms

    - Statement as to the number of days left in the campaign

        Calculated based on current date vs Crowdsale end date.

    - Offering goal in USD

3. Non-Terms

    - Minimum investment (in USD)
    - Date when minimum was reached
    - Number of investors

        Based on data from the Token contract.

    - Amount raised

        Based on data from the Token and Crowdsale contracts. The Token contract will know the number of tokens minted `totalSupply()` and the Crowdsale will know the USD to ETH conversion price at the time of minting. See also the Regulation A+ Crowdsale API project.

    - The words “Closing Soon”

        Awaiting feedback on the threshold for displaying this on the Crowdsale website.

## Development

The site will be built using `react-create-app` as a base and will conform to the general coding standards common to all of the C4Coin sites.

### Development Prerequisites

* [NodeJS](htps://nodejs.org), version 9.7.1 or better (I use [`nvm`](https://github.com/creationix/nvm) to manage Node versions — `brew install nvm`.)
* [Docker](https://www.docker.com) (Use [Docker for Mac](https://docs.docker.com/docker-for-mac/), not the homebrew version)
* [Access to the C4Coin Jira](https://c4coin.atlassian.net)
* [requirements google doc](https://docs.google.com/document/d/1s8kTfWc2VzSOXft3Zky7qowFLgNo9YIWEHuVV09LWXs)

### Initialisation

    npm install

### Testing

    npm test

or with code coverage

    npm run test:cov

### Linting

    npm run lint

## Deployment

The site will be deployed automatically to [netlify](https://netlify.com) once CircleCI has cleared a merge to either `develop` (staging server) or `master` (production).

## Contributing

Please see the [contributing notes](CONTRIBUTING.md).
