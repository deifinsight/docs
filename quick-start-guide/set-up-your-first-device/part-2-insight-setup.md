---
description: >-
  This page focus on the setup of the FX30 and controller devices on the Insight
  portal.
---

# Part 2: Insight setup

## Set up the Equipment

Log into the portal at [`https://insight.deif.com`](https://insight.deif.com).

Follow **Settings =&gt; Equipment Management** from the navigation menu and then press the **Add Equipment** button.

![Equipment Management page](../../.gitbook/assets/equipment_add1.png)

### Enter Equipment details

![Creating a new Equipment](../../.gitbook/assets/equip_add1%20%281%29.png)

Fill all required fields as a minimum.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Control</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Status</td>
      <td style="text-align:left">Switch.
        <br />Activate/Deactivate the Equipment.</td>
      <td style="text-align:left">No</td>
    </tr>
    <tr>
      <td style="text-align:left">Equipment Type</td>
      <td style="text-align:left">Locked field.
        <br />Fixed as &quot;Diesel genset&quot;.</td>
      <td style="text-align:left">No</td>
    </tr>
    <tr>
      <td style="text-align:left">Equipment Name</td>
      <td style="text-align:left">Entry field.
        <br />The name by which the Equipment will be identified.</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">Equipment Model</td>
      <td style="text-align:left">
        <p>Entry field.</p>
        <p>Information about the model of the Equipment.</p>
      </td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">Connection Type</td>
      <td style="text-align:left">
        <p>Dropdown.</p>
        <p>See Note 1 below.</p>
      </td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">IP Address</td>
      <td style="text-align:left">
        <p>Entry field.</p>
        <p>The IP address of the device</p>
      </td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">Unit ID</td>
      <td style="text-align:left">
        <p>Dropdown.</p>
        <p>See Note 1 below.</p>
      </td>
      <td style="text-align:left">No</td>
    </tr>
    <tr>
      <td style="text-align:left">Port</td>
      <td style="text-align:left">
        <p>Entry field.</p>
        <p>Default at 502 - standard port for Modbus TCP.</p>
      </td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">Users</td>
      <td style="text-align:left">Multi-selection dropdown.
        <br />See Note 2 below.</td>
      <td style="text-align:left">No</td>
    </tr>
    <tr>
      <td style="text-align:left">Teams</td>
      <td style="text-align:left">Multi-selection dropdown.
        <br />See Note 2 below.</td>
      <td style="text-align:left">No</td>
    </tr>
  </tbody>
</table>

¹ If you require to set a Modbus ID \(for example: when using Modbus TCP to Serial converter\), choose `Modbus RTU to TCP Converter` from the **Connection Type** dropdown. When **Connection Type** is set to `TCP/IP`, the Modbus ID is set to 3.

² Selecting users and teams is not very relevant at this stage.

### Define Product Family and Tags

The first step is to define the Product Family, for which there are two choices available. See below table.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Product Family</th>
      <th style="text-align:left">Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Multi-line 2 (Default)</td>
      <td style="text-align:left">
        <p>Set of predefined tag configuration for the DEIF ML2 platform.</p>
        <p>No extra effort is required.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">None</td>
      <td style="text-align:left">
        <p>Set of predefined tag names for any Modbus platform.</p>
        <p>Selecting None will clear all configured tags.</p>
        <p>Data for non-configured tags will not be received from the device.</p>
      </td>
    </tr>
  </tbody>
</table>

![View of the default \(Multi-line 2\) Product Family. ](../../.gitbook/assets/equip_tags.png)

Setting up tags is not in the scope of this Quick Start Guide.  
For information on how to set up a tag, please follow the link below.

{% page-ref page="../../knowledge-base/modbus-tags.md" %}

### Saving your Equipment configuration

Once the tag configuration is finished, the configuration may be saved and ended.

![Save the Device configuration](../../.gitbook/assets/equip_tags2.png)

There is an optional step to Save and configure Notifications - **Save&Next** button.  
The configuration of Notifications is not part of the scope of this Quick Start Guide.

{% page-ref page="../../knowledge-base/notifications.md" %}

{% hint style="success" %}
The Equipment is now configured.  
Before data is received, the Equipment must be linked to a DAU.
{% endhint %}

## Set up the DAU

To conclude the process, you will need to register the DAU and link the Equipment that was created above.

### Add a DAU

Start by adding a DAU by navigating to **Settings =&gt; DAU Management** and pressing the **Add DAU** button.

![](../../.gitbook/assets/dau_add1.png)

### Register DAU details

Give the DAU a recognisable name.   
You can give it the same name as the Equipment or a variation of it, for example.

Introduce the **IMEI** and **Serial Number** of the DAU.  
These can be found in the DAU Configuration page, the DAU box and the label on the device.

{% hint style="info" %}
Quick Tip: If you kept DAU Configuration page open in your browser you can simply copy and paste the **IMEI** and **Serial Number** from one page to the other.
{% endhint %}

![The DAU has just a few settings.](../../.gitbook/assets/dau_add2.png)

{% hint style="warning" %}
Both the IMEI and Serial Number must be introduced correctly, or the DAU will not work correctly.

Please note that only the IMEI has a validation of the input provided.
{% endhint %}

### Geo-location options

When enabling the geo-location, a time interval for location reporting must be set.  
The interval is set in minutes by means of a dropdown.  
An interval of zero \(0\) defines that the location is only sent one time just after power-up of the DAU.

### Link the DAU to the Equipment

Press the **Next** button to move to the **Equipment Connection** tab.  
Finally, select a single Equipment from the list and press **Save**.

![Link the Equipment to the DAU](../../.gitbook/assets/dau_equip_connect.png)

{% hint style="success" %}
The Equipment is now linked to the DAU and data will soon be received on Insight.
{% endhint %}

