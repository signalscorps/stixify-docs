# Microsoft Azure Sentinel

### Prerequisites

[An Stixify plan that supports use of our API.](https://www.stixify.com/pricing/)

### Setup

This integration uses the STIX/TAXII 2.x data Connector for Azure Sentinel which comes as standard in Azure Sentinel deployments.

![STIX/TAXII 2.x data Connector for Azure Sentinel](../.gitbook/assets/obstracts-azure-taxii-connector-setup.png)

You'll need to configure the following settings:

* **Friendly name (for server):** Will be shown against intelligence ingested, but can be anything you like
* **API root URL:** It’s easy to construct the Root URL. You just need your Stixify Group UUID, [obtained on the Group Management page in the Stixify web app.](https://app.stixify.com/user/manage\_group)
  * https://app.stixify.com/taxii/taxii2/YOUR-GROUP-UUID
* **Collection UUID:** The Collection UUID is a Collection UUID in Stixify and [can be obtained from the Collection List page in the Stixify web app.](https://app.stixify.com/collection/list/)
* **Username:** your Stixify username
* **Password:** your Stixify API key
* **Import indicators:** Select, "At most one month old" (or sooner). _Important: We do not allow download of older indicators._
* **Polling frequency:** Select, "1 hour".

Now click save, and you should see intelligence being ingested.&#x20;

![Azure Sentinel Threat Intelligence](../.gitbook/assets/obstracts-azure-taxii-threat-intel.png)

### Usage

Once data connector is enabled, the ingested threat intelligence will be used by active rules in Azure Sentinel that utilise threat intelligence.
