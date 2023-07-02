---
title: "Get hostTracker"
description: "Read the properties and relationships of a hostTracker object."
author: "joerattazzi-microsoft"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Get hostTracker

Namespace: microsoft.graph.security

[!INCLUDE [threatintelligence-api-disclaimer](../../includes/threatintelligence-api-disclaimer.md)]

Read the properties and relationships of a [hostTracker](../resources/security-hosttracker.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "security_hosttracker_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/security-hosttracker-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /security/threatIntelligence/hostTrackers/{hostTrackerId}
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.hostTracker](../resources/security-hosttracker.md) object in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "get_hosttracker",
  "sampleKeys": ["Y29udG9zby1hZHZlcnRpc2luZzkyNDEwQ29udG9zb0lkOTI0MTBhYm91dC5hZHMuY29udG9zby5jb20="]
}
-->

```http
GET https://graph.microsoft.com/v1.0/security/threatIntelligence/hostTrackers/Y29udG9zby1hZHZlcnRpc2luZzkyNDEwQ29udG9zb0lkOTI0MTBhYm91dC5hZHMuY29udG9zby5jb20=
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.hostTracker"
}
-->

```json
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.security.hostTracker",
  "id": "Y29udG9zby1hZHZlcnRpc2luZzkyNDEwQ29udG9zb0lkOTI0MTBhYm91dC5hZHMuY29udG9zby5jb20=",
  "firstSeenDateTime": "2019-06-13T17:25:22.761Z",
  "lastSeenDateTime": "2023-03-25T23:59:32.157Z",
  "kind": "ContosoId",
  "value": "contoso-advertising",
    "host": {
        "id": "about.ads.contoso.com"
    }
}
```
