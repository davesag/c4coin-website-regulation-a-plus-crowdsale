# website-regulation-a-plus-crowdsale

The web front end for C4Coin's Regulation A+ Crowdsale

## Requirements

### Terms required by the SEC

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

        Based on data from the Token and Crowdsale contracts. The Token contract will know the number of tokens minted `totalSupply()` and the crowdsale will know the USD to ETH conversion price at the time of minting. See also the Regulation A+ Crowdsale API project.

    - The words “Closing Soon”

        Awaiting feedback on the threshold for displaying this on the crowdsale website.

## Development

The website will be a Single Page App built using Redux and React.

### Development Prerequisites

* [NodeJS](htps://nodejs.org), version 9.5+ (I use [`nvm`](https://github.com/creationix/nvm) to manage Node versions — `brew install nvm`.)
* [Docker](https://www.docker.com) (Use [Docker for Mac](https://docs.docker.com/docker-for-mac/), not the homebrew version)
* _add other details_

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
