# SignalFx Steps

These steps allow you to communicate between xMatters and SignalFx.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [SignalFxSteps.zip](SignalFxSteps.zip) - Workflow zip file with the step and example flow
* [signalfx.png](/signalfx.png) - SignalFx logo

# How it works
This step can be triggered through either an xMatters integration in SignalFx, or by using an HTTP trigger in SignalFx.


# Installation

## SignalFx Setup
1. Go to Integrations > xMatters. (It should be under the "Notification Services" section)
2. Create a new integration, filling in the name to identify the notification, and for the URL use the one given in the `Inbound - SignalFx` step in your xMatters Flow.
3. Add the xMatters integration to an alert as a recipient.

4. In SignalFx, go to your user profile and select `Access Tokens` from the tabs on the left. Create a new an Access Token from that menu.
5. Use this value to fill in the API Token Constant in xMatters.

## xMatters Setup
1. Download the [SignalFxSteps.zip](SignalFxSteps.zip) file onto your local computer
2. Navigate to the Developer tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Update the Get Events step with the Status and Priority of the events you would like to look for.
5. Fill in the API Token for SignalFx in the Constants.
6. Fill in the recipients for the xMatters Alert in the xMatters Create Event step.
7. Update the `SignalFx API` and `SignalFx Ingest` Endpoints with the correct values. `https://api.{REALM}.signalfx.com` and `https://ingest.{REALM}.signalfx.com` respectively.


## Usage

### Outputs

| Name |
| ---- |
| shortDescription |
| metricKeys |
| metricValue |
| data |
| priority |
| recipients |
| incidentId |
| status |
| metricInputs |
| rule |
| runbookUrl |
| triggeredWhileMuted |
| imageUrl |
| detectorUrl |
| timestamp |
| tip |
| detector |
| description |
| detectOnCondition |
| eventType |



## Example
This is an image of the example flow provided. On an alert from SignalFx, it will look for xMatters events matching the SignalFx incidentId. It will then create an xMatters alert. On a response to the alert, the response is relayed back to SignalFx.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

