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

4. In SignalFx, go to your user profile and generate an API Token.
5. Use this value to fill in the API Token Constant in xMatters.

## xMatters Setup
1. Download the [SignalFxSteps.zip](SignalFxSteps.zip) file onto your local computer
2. Navigate to the Developer tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Update the Get Events step with the Status and Priority of the events you would like to look for.
5. Fill in the API Token for SignalFx in the Constants.
6. Fill in the recipients for the xMatters Alert in the xMatters Create Event step.


## Usage

### Outputs

| Name | Description |
| ---- | ----------  |
| shortDescription | URL of the repository |
| metricKeys | URL of the repository |
| metricValue | URL of the repository |
| data | URL of the repository |
| priority | URL of the repository |
| recipients | URL of the repository |
| incidentId | URL of the repository |
| status | URL of the repository |
| metricInputs | URL of the repository |
| rule | URL of the repository |
| runbookUrl | URL of the repository |
| triggeredWhileMuted | URL of the repository |
| imageUrl | URL of the repository |
| detectorUrl | URL of the repository |
| timestamp | URL of the repository |
| tip | URL of the repository |
| detector | URL of the repository |
| description | URL of the repository |
| detectOnCondition | URL of the repository |
| eventType | URL of the repository |



## Example
This is an image of the example flow provided. On an alert from SignalFx, it will look for xMatters events matching the SignalFx incidentId. It will then create an xMatters alert. On a response to the alert, the response is relayed back to SignalFx.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

