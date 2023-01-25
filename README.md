# Extrinsec AppDefender

## AppDefender Demo on Google Cloud Functions

This repo demonstrates running a sample GCF function with Extrinsec AppDefender enabled.  For more detailed information on the benefits of AppDefender or how it works, please visit the [main AppDefender repository](https://github.com/extrinsec/appdefender).

## Prerequisites

1. a Github account, to fork this repo so you can run your own Github actions workflows
1. a Google Cloud account with Billing enabled and configured for Github Actions deployment (see [this doc](GithubActionsToGCF.md) for reference)
1. an Extrinsec license key
1. (Optional) an Extrinsec policy group name
   - defaults to the observeAll.ability public group

## Deploy to GCP

1. save your Extrinsec license key as a Github Actions secret on your forked repo, as `ES_LICENSE_KEY`
2. if you haven't already, save `GCP_WORKLOAD_IDENTITY_PROVIDER_REF` and `GCP_SERVICE_ACCOUNT_EMAIL` as Github Actions secrets (see below section on enabling Github Actions deployment to GCP)
3. enable and run the Github Actions workflow
4. observe your GCF logs

Note:
- three functions with runtimes for NodeJS, Python and Ruby are shown here.  Feel free to remove any that you don't use, or change the runtime versions
- only outbound data capturing by AppDefender is shown in these samples.  Feel free to update the functions to see other use cases

