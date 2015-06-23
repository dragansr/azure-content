<properties 
	pageTitle="Release notes for Application Insights" 
	description="The latest updates." 
	services="application-insights" 
    documentationCenter=""
	authors="alancameronwills" 
	manager="ronmart"/>
<tags 
	ms.service="application-insights" 
	ms.workload="tbd" 
	ms.tgt_pltfrm="ibiza" 
	ms.devlang="na" 
	ms.topic="article" 
	ms.date="04/28/2015" 
	ms.author="sergkanz"/>
 
# Release Notes for Application Insights SDK for .NET

[Using the SDK for .NET](app-insights-start-monitoring-app-health-usage.md)

## Version 1.0

- Moved telemetry initializers and telemetry modules from separate sub-namespaces to the root `Microsoft.ApplicationInsights.Extensibility.Web` namespace.
- Removed "Web" prefix from names of telemetry initializers and telemetry modules because it is already included in the `Microsoft.ApplicationInsights.Extensibility.Web` namespace name.
- Moved `DeviceContextInitializer` from the `Microsoft.ApplicationInsights` assembly to the `Microsoft.ApplicationInsights.Extensibility.Web` assembly and converted it to an `ITelemetryInitializer`.
- Change namespace and assembly names from `Microsoft.ApplicationInsights.Extensibility.RuntimeTelemetry` to `Microsoft.ApplicationInsights.Extensibility.DependencyCollector` for consistency with the name of the NuGet package.
- Rename `RemoteDependencyModule` to `DependencyTrackingTelemetryModule`.
- Rename `CustomPerformanceCounterCollectionRequest` to `PerformanceCounterCollectionRequest`.

## Version 0.17
- Removed dependency to EventSource NuGet for the framework 4.5 applications.
- Anonymous User and Session cookies will not be generated on server side. Telemetry modules ```WebSessionTrackingTelemetryModule``` and ```WebUserTrackingTelemetryModule``` are no longer supported and were removed from ApplicationInsights.config file. Cookies from JavaScript SDK will be respected.
- Persistence channel optimized for high-load scenarios is used for web SDK. "Spiral of death" issue fixed. Spiral of death is a condition when spike in telemetry items count that greatly exceeds throttling limit on endpoint will lead to retry after certain time and will be throttled during retry again.
- Developer Mode is optimized for production. If left by mistake it will not cause as big overhead as before attempting to output additional information.
- Developer Mode by default will only be enabled when application is under debugger. You can override it using ```DeveloperMode``` property of  ```ITelemetryChannel``` interface.

## Version 0.16 

2015-04-28 preview

- SDK now supports DNX target platform to enable monitoring of [.NET Core framework](http://www.dotnetfoundation.org/NETCore5) applications.
- Instances of ```TelemetryClient``` do not cache Instrumentation Key anymore. Now if instrumentation key wasn't set in ```TelemetryClient``` explicitly ```InstrumentationKey``` will return null. It fixes an issue when you set ```TelemetryConfiguration.Active.InstrumentationKey``` after some telemetry was already collected, telemetry modules like dependency collector, web requests data collection and performance counters collector will use new instrumentation key.

## Version 0.15

- New property ```Operation.SyntheticSource``` now available on ```TelemetryContext```. Now you can mark your telemetry items as "not a real user traffic" and specify how this traffic was generated. As an example by setting this property you can distinguish traffic from your test automation from load test traffic.
- Channel logic was moved to the separate NuGet called Microsoft.ApplicationInsights.PersistenceChannel. Default channel is now called InMemoryChannel
- New method ```TelemetryClient.Flush``` allows to flush telemetry items from the buffer synchronously

## Version 0.13

No release notes for older versions available.
