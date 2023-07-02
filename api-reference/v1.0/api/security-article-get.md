---
title: "Get article"
description: "Read the properties and relationships of an article object."
author: "joerattazzi-microsoft"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Get article

Namespace: microsoft.graph.security

[!INCLUDE [threatintelligence-api-disclaimer](../../includes/threatintelligence-api-disclaimer.md)]

Read the properties and relationships of an [article](../resources/security-article.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "security_article_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/security-article-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /security/threatIntelligence/articles/{articleId}
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

If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.article](../resources/security-article.md) object in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "get_article_e1",
  "sampleKeys": ["a272d5ab"]
}
-->

```http
GET https://graph.microsoft.com/v1.0/security/threatIntelligence/articles/a272d5ab
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.article"
}
-->

```json
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "$metadata#articles/$entity",
  "id": "a272d5ab",
  "createdDateTime": "2023-03-03T18:20:22.677Z",
  "lastUpdatedDateTime": "2023-03-03T18:20:22.677Z",
  "title": "Batloader Malware Abuses Legitimate Tools Uses Obfuscated JavaScript Files in Q4 2022 Attacks",
  "summary": {
      "content": "Trend Micro discusses Batloader campaigns that were observed in the last quarter of 2022.",
      "format": "markdown"
  },
  "isFeatured": false,
  "body": {
      "content": "#### Description\r\nTrend Micro discusses Batloader...",
      "format": "markdown"
  },
  "tags": [
      "OSINT",
      "Batloader",
      "RoyalRansomware",
      "Python",
      "JavaScript",
      "MSI",
      "PowerShell"
  ],
  "imageUrl": null
}
```
