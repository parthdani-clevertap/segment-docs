---
title: 'Optimizely Feature Experimentation (Actions) Destination'
id: 641d5acea88fa531b9068608
hide-personas-partial: true
hide-boilerplate: false
hide-dossier: true
---

[Optimizely Feature Experimentation](https://www.optimizely.com/products/experiment/feature-experimentation/){:target="_blank"} is a feature flagging and experimentation platform for websites, mobile apps, chatbots, APIs, smart devices and anything else with a network connection.

With their SDK one can deploy code behind feature flags, experiment with A/B tests and use percentage deliveries to roll out or roll back flags immediately.

Segment’s Optimizely Feature Experimentation (Actions) destination support tracking of conversion events.
The only action (event) supported currently is trackEvent. [TrackEvent](https://docs.developers.optimizely.com/experimentation/v4.0.0-full-stack/docs/track-event-javascript-node){:target="_blank"} sends user conversion events for active experiments. Segment sends data using [Event API](https://docs.developers.optimizely.com/experimentation-data/reference/post_events){:target="_blank"}.


## Getting started

Before connecting to the Optimizely Feature Experimentation destination, you must have a [Optimizely Feature Experimentation](https://www.optimizely.com/products/experiment/feature-experimentation/){:target="_blank"} account, Account ID and Datafile URL.

To connect the Optimizely Feature Experimentation destination:

1. From the Segment web app, click **Catalog**, then click **Destinations**.
2. Search for **Optimizely Feature Experimentation** in the Destinations Catalog, and select the destination.
3. Click **Configure Optimizely Feature Experimentation (Actions)** in the top-right corner of the screen.
4. Select the source that will send data to Optimizely Feature Experimentation and follow the steps to name your destination.
5. On the **Settings** tab, authenticate the destination using datafile URL.
6. Once authenticated, input your account Id from your optimizely account. Toggle “Enable Destination” on and click  **Save Changes**
7. Navigate to the **Mappings** tab, click **New Mapping**, and select **Track Event**.
8. Under Select mappings, Select the event key from the dropdown or input the event manually as the  "event" and select the other mappings. Click **Save** and toggle to enable the mapping.
     * **Note:** The conversion event will only be sent if the event key configured should match exactly as the name of an active experiment metric set up in the Optimizely dashboard.
     * **Note:** The current user should activated in a running experiment with the associated metric. (Activation is expected to be done at the event source before sending track events to Segment).
{% include components/actions-fields.html settings="true"%}