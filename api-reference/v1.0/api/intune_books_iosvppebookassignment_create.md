﻿# Create iosVppEBookAssignment

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Create a new [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.
## Prerequisites
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementApps.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the iosVppEBookAssignment object.

The following table shows the properties that are required when you create the iosVppEBookAssignment.

|Property|Type|Description|
|:---|:---|:---|
|id|String|Key of the entity. Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|The assignment target for eBook. Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|
|installIntent|[installIntent](../resources/intune_shared_installintent.md)|The install intent for eBook. Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md). The possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.|



## Response
If successful, this method returns a `201 Created` response code and a [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object in the response body.

## Example
### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
Content-type: application/json
Content-length: 193

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 242

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "id": "48f05789-5789-48f0-8957-f0488957f048",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```



