# Temporal Grafana Dashboards

This repository contains community-driven Grafana [dashboards](https://grafana.com/docs/grafana/latest/dashboards/) that can be used for monitoring 
Temporal Server and SDK metrics. 

We welcome contributions to existing as well as new dashboards that can help the community.

- ⚠️ Note that the intent for these dashboards is not to be used in production. They are here to provide out-of-the-box community dashboards you can learn from and use as a baseline for your monitoring efforts.
- Also note that we do not test these dashboards on all Grafana and Temporal Server versions. If you encounter any issues please report them by opening [an issue](https://github.com/temporalio/dashboards/issues/new) in this repository.

## Directory structure

* [`server/`](server): Dashboards for Temporal Server metrics
* [`sdk/`](sdk): Dashboards for Temporal SDK metrics. This includes two dashboards, one for Go/Java SDK and one Core based SDKs.
* [`misc/`](misc): Server metrics dashboards that have not been fully tested yet or need improvements

## Usage

Our [default helm chart](https://github.com/temporalio/helm-charts) installs Grafana and will provision the dashboards from this repo automatically. If you would like to try these dashboards on your own Grafana instance you can import them. Unfortunately Grafana does not allow importing by URL aside from those hosted on the Grafana website, so the JSON of the dashboard needs to be copy/pasted into your Grafana instance. To do this:

1. Copy the JSON for the dashboard you would like to import to your clipboard. For example if you wanted to import the Server Metrics dashboard, navigate to https://github.com/temporalio/dashboards/blob/master/server/server-general.json and then use the "Copy raw contents" button at the top right of the editor panel on Github (next to the "Delete this file" button).
1. In Grafana, navigate to the Dashboards -> Manage page.
1. Click the "Import" button on the far right of the page.
1. Paste the JSON from your clipboard into the "Or paste JSON" text area on the Import page.
1. Click the "Load" button.
1. Adjust the name and folder if you need to.
1. Click the "Import" button.
1. Grafana should save the dashboard and redirect browser to it.

## Learn more

For more information on Temporal, reference our [docs](https://docs.temporal.io/).
