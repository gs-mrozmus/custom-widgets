# Salesforce Cases Form Widget

This widget integrates with your Salesforce instance to enable case management directly from your community. Follow the setup steps below to get started.

---

## Prerequisites

- Access to your Salesforce instance with administrator privileges
- Access to your community administration panel

---

## Setup Instructions

### Step 1: Create External Client App in Salesforce

Navigate to your Salesforce instance:  
**Settings → Platform Tools → Apps → External Client Apps → External Client App Manager**

![External Client App Manager](README/01-external-client-app-manager.png)

### Step 2: Create New External Client App

Click to create a new External Client App.

![Create External Client App](README/02-create-external-client-app.png)

### Step 3: Enable Client Credentials Flow

Enable the Client Credentials Flow for your app.

![Enable Client Credentials Flow](README/03-enable-client-credentials-flow.png)

### Step 4: Retrieve Consumer Key and Secret

Copy your Consumer Key and Consumer Secret — you'll need these for the connector configuration.

![Consumer Key and Secret](README/04-consumer-key-and-secret.png)

### Step 5: Create Connectors from Templates

In your community admin panel, create new connectors from the available templates.

> **Required Connectors:**  
> You need to create all four of these connectors:
> - Salesforce Case Lookup by Contact Email
> - Salesforce Contact Lookup by Email
> - Salesforce Create Case for Contact
> - Salesforce Create Contact and Case

![Create Connectors from Templates](README/05-create-connectors-from-templates.png)

Provide the URL to your Salesforce instance along with the Consumer Key and Secret.

![Connector Configuration](README/06-connector-configuration.png)

### Step 6: Add Widget Source Repository

Add the current repository `https://raw.githubusercontent.com/gs-mrozmus/custom-widgets/refs/heads/main/widget_registry.json` to your Widget Sources by `Add New Endpoint` button.

![Add Widget Source](README/07-add-widget-source.png)

### Step 7: Add Widget to Your Community

Add the new Salesforce Cases widget to your community.

![Add Widget to Community](README/08-add-widget-to-community.png)

---

## Widget Preview

### Signed-in Users

For authenticated users, the widget displays their existing cases and allows creating new ones:

![Widget View for Signed Users](README/09-widget-signed-user-view.png)

### Anonymous Users

For visitors who are not signed in, the widget shows a disabled form:

![Widget View for Anonymous Users](README/10-widget-anonymous-user-view.png)
