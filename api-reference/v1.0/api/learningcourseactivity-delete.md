---
title: "Delete learningCourseActivity"
description: "Delete a learningCourseActivity object by using the course activity ID of either an assignment or a self-initiated activity."
author: "malabikaroy"
ms.localizationpriority: medium
ms.prod: "employee-learning"
doc_type: apiPageType
---

# Delete learningCourseActivity

Namespace: microsoft.graph

Delete a [learningCourseActivity](../resources/learningcourseactivity.md) object by using the course activity ID of either an assignment or a self-initiated activity.

>**Note**: Learning course activities can be managed by a provider only when **isCourseAcitvitySyncEnabled** is set to `true`.  To update the value, use the [Update learningProvider](../api/learningprovider-update.md) method.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "learningcourseactivity_delete" } -->
[!INCLUDE [permissions-table](../includes/permissions/learningcourseactivity-delete-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

``` http
DELETE /employeeExperience/learningProviders/{registrationId}/learningCourseActivities/{id}
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "delete_learningCourseActivity",
  "sampleKeys": ["13727311-e7bb-470d-8b20-6a23d9030d70", "be2f4d76-e020-11ec-9d64-0242ac120002"]
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/employeeExperience/learningProviders/13727311-e7bb-470d-8b20-6a23d9030d70/learningCourseActivities/be2f4d76-e020-11ec-9d64-0242ac120002
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->

``` http
HTTP/1.1 204 No Content
```
