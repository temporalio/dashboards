# Temporal DataDog SDK Dashboards

The [Dashboard](temporal_sdk_dashboard.json) here works with [this openmetrics configuration](openmetrics.h_conf.yaml).

### Prerequisites

1. [DataDog Agent](https://docs.datadoghq.com/getting_started/agent/), installed.
2. Advanced `Percentile` configuration for Distribution metrics.
   1. Which metrics? Basically, any metrics [here](https://docs.temporal.io/references/sdk-metrics) that are a `Histogram` and for which you want to report percentiles (p95/p99).
   
### Put it all together
1. Visit [here](https://docs.datadoghq.com/integrations/openmetrics/) for OpenMetrics configuration with the DataDog agent for details about configuring your DD Agent.
2. Drop this [conf.yaml](openmetrics.h_conf.yaml) at your Agent `openmetrics.d` config path.
3. Import the [Dashboard](temporal_sdk_dashboard.json)
4. Be sure you enable the `Percentile` configuration for relevant metrics. 

> **Example for configuring `temporal_request_latency`**:
> * Visit https://app.datadoghq.com/metric/summary?metric=temporal_request_latency
> * Set `Advanced > Percentiles > Configure > ON`


