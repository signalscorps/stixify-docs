---
description: >-
  Ingest threat intelligence from Stixify into Microsoft Azure Sentinel for log
  matching.
---

# Microsoft Azure Sentinel

### Prerequisites

[An Stixify plan that supports use of our API.](https://www.stixify.com/pricing/)

### Setup

This integration uses the STIX/TAXII 2.x data Connector for Azure Sentinel which comes as standard in Azure Sentinel deployments.

![STIX/TAXII 2.x data Connector for Azure Sentinel](../.gitbook/assets/obstracts-azure-taxii-connector-setup.png)

1. Navigate to the Threat Intelligence - TAXII connector&#x20;
2. Select add new
3. Set the following field values:
   1. **Friendly name (for server):** Will be shown against intelligence ingested, but can be anything you like
   2. **API root URL:** It’s easy to construct the Root URL. You just need your Stixify Group UUID, [obtained on the Group Management page in the Stixify web app.](https://app.stixify.com/user/manage\_group)
      * https://app.stixify.com/taxii/taxii2/YOUR-GROUP-UUID
   3. **Collection UUID:** The Collection UUID is a Collection UUID in Stixify and [can be obtained from the Collection List page in the Stixify web app.](https://app.stixify.com/collection/list/)
   4. **Username:** your Stixify username
   5. **Password:** your Stixify API key
   6. **Import indicators:** Select, "At most one month old" (or sooner). _Important: We do not allow download of older indicators._
   7. **Polling frequency:** Select, "1 hour".

Now click save, and you should see intelligence being ingested.

### Usage

Once data connector is enabled, the ingested threat intelligence will be used by active rules in Azure Sentinel that utilise threat intelligence.
