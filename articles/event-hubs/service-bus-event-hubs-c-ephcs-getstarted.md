<properties
	pageTitle="Get Started with Event Hubs"
	description="Follow this tutorial to get started using Azure Event Hubs sending events with C and receiving in C# using EventProcessorHost"
	services="event-hubs,service-bus"
	documentationCenter=""
	authors="fsautomata"
	manager="timlt"
	editor=""/>

<tags
	ms.service="event-hubs"
	ms.workload="core"
	ms.tgt_pltfrm="c"
	ms.devlang="csharp"
	ms.topic="get-started-article"
	ms.date="06/17/2015"
	ms.author="sethm"/>

# Get started with Event Hubs

[AZURE.INCLUDE [service-bus-selector-get-started](../../includes/service-bus-selector-get-started.md)]

## Introduction

Event Hubs is a highly scalable ingestion system that can intake millions of events per second, enabling an application to process and analyze the massive amounts of data produced by your connected devices and applications. Once collected into Event Hubs, you can transform and store data using any real-time analytics provider or storage cluster.

For more information, please see [Event Hubs Overview].

In this tutorial, you will learn how to ingest messages into an Event Hub using a console application in C, and to retrieve them in parallel using the C# [Event Processor Host] library.

In order to complete this tutorial you will need the following:

+ A C development environment. For this tutorial, we will assume the gcc stack on an [Azure Linux VM](../virtual-machines-linux-tutorial.md) with Ubuntu 14.04. Instructions for other environments will be provided in external links.

+ Microsoft Visual Studio Express 2013 for Windows

+ An active Azure account. <br/>If you don't have an account, you can create a free trial account in just a couple of minutes. For details, see <a href="http://azure.microsoft.com/pricing/free-trial/?WT.mc_id=A0E0E5C02&amp;returnurl=http%3A%2F%2Fazure.microsoft.com%2Fen-us%2Fdevelop%2Fmobile%2Ftutorials%2Fget-started%2F" target="_blank">Azure Free Trial</a>.

## Create an Event Hub

1. Log on to the [Azure management portal], and click **NEW** at the bottom of the screen.

2. Click **App Services**, then **Service Bus**, then **Event Hub**, then **Quick Create**.

   	![][1]

3. Type a name for your Event Hub, select your desired region, and then click **Create a new Event Hub**.

   	![][2]

4. Click the namespace you just created (usually ***event hub name*-ns**).

   	![][3]

5. Click the **Event Hubs** tab at the top of the page, and then click the Event Hub you just created.

   	![][4]

6. Click the **Configure** tab at the top of the page, add a rule named **SendRule** with *Send* rights, add another rule called **ReceiveRule** with *Manage, Send, Listen* rights, and then click **Save**.

   	![][5]

7. On the same page, take note of the generated keys for **SendRule**.

   	![][6b]

8. Click the **Dashboard** tab at the top of the page, and then click **Connection Information**. Take note of the two connection strings.

   	![][6]

Your Event Hub is now created, and you have the connection strings you need to send and receive events.

[AZURE.INCLUDE [service-bus-event-hubs-get-started-send-c](../../includes/service-bus-event-hubs-get-started-send-c.md)]


[AZURE.INCLUDE [service-bus-event-hubs-get-started-receive-ephcs](../../includes/service-bus-event-hubs-get-started-receive-ephcs.md)]

## Run the applications

Now you are ready to run the applications.

1.	Run the **Receiver** project from Visual Studio, then wait for it to start the receivers for all the partitions.

   	![][21]

2.	Run the **sender** program, and see the events appear in the receiver window.

   	![][24]

<!-- Images. -->
[1]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub1.png
[2]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub2.png
[3]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub3.png
[4]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub4.png
[5]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub5.png
[6]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub6.png
[6b]: ./media/service-bus-event-hubs-c-ephcs-getstarted/create-event-hub6b.png


[21]: ./media/service-bus-event-hubs-c-ephcs-getstarted/run-csharp-ephcs1.png
[24]: ./media/service-bus-event-hubs-c-ephcs-getstarted/receive-eph-c.png

<!-- Links -->
[Azure Management Portal]: https://manage.windowsazure.com/
[Event Processor Host]: https://www.nuget.org/packages/Microsoft.Azure.ServiceBus.EventProcessorHost
[Event Hubs Overview]: http://msdn.microsoft.com/library/azure/dn836025.aspx
 