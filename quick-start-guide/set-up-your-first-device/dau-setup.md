---
description: >-
  This page will help you setting up the DAU and prepare it to read data from a
  Modbus TCP device.
---

# Part 1: DAU setup

## Connect DAU to PC

1. Turn on the DAU.
2. Connect the micro-USB cable to the DAU and the computer.
3. Wait a few seconds until the network connection is established.
4. Open your browser and navigate to address `http://192.168.2.2`.

![After connection is established, the result should look similar to this.](../../.gitbook/assets/image%20%281%29.png)

## Configure the DAU

Configuring the DAU is a straightforward and easy task, requiring only to define network settings \(on Modbus TCP\) and operator's APN configuration. 

### Configure network settings \(Modbus TCP only\)

When using the Ethernet variant of the DAU, it will be necessary to configure the network settings.  
This is necessary so that the DAU is in the same network as the device that will be monitored on Insight.

![](../../.gitbook/assets/dau_config_ethernet.png)

{% hint style="info" %}
Save your changes.  
You will be prompted to switch OFF the DAU and turn it ON again to restart with the new network settings.
{% endhint %}

### Configure APN settings

![](../../.gitbook/assets/image%20%283%29.png)

{% hint style="info" %}
If the data session is already connected, skip this step.
{% endhint %}

The APN configuration is an important step without which no data sessions with the operator will be started.

In some occasions, the SIM card may configure the APN automatically.

{% hint style="warning" %}
Check the APN settings with your operator before proceeding.
{% endhint %}

Click on tab "SIM Configuration" and enter the APN settings.

![](../../.gitbook/assets/dau_config_provider.png)

{% hint style="danger" %}
Don't forget to Save before leaving the page.
{% endhint %}

## End Part 1

{% hint style="success" %}
The DAU should now be configured.   
Proceed to [Part 2: Insight setup](part-2-insight-setup.md).
{% endhint %}

{% hint style="info" %}
Hint: Keep the DAU Configuration page open in your browser will be handy during the next part.
{% endhint %}
