---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new NamedLocation
{
	OdataType = "#microsoft.graph.ipNamedLocation",
	DisplayName = "Untrusted named location with only IPv4 address",
	AdditionalData = new Dictionary<string, object>
	{
		{
			"isTrusted" , false
		},
		{
			"ipRanges" , new List<>
			{
				new 
				{
					OdataType = "#microsoft.graph.iPv4CidrRange",
					CidrAddress = "6.5.4.3/18",
				},
			}
		},
	},
};
var result = await graphClient.Identity.ConditionalAccess.NamedLocations["{namedLocation-id}"].PatchAsync(requestBody);


```