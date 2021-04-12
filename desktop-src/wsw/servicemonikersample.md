---
title: ServiceMonikerSample
description: Este exemplo mostra um cliente que pode ser usado com o exemplo de MetadataExchange TCP. Ele utiliza o moniker do serviço WCF.
ms.assetid: cfcff5ee-c0e1-4694-831e-fed0bd0e9855
keywords:
- API de serviços Web do Windows ServiceMonikerSample
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3188b41df830f55e77e151c5be9413a986a5dcf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292138"
---
# <a name="servicemonikersample"></a>ServiceMonikerSample

Este exemplo mostra um cliente que pode ser usado com o exemplo de MetadataExchange TCP. Ele utiliza o moniker do serviço WCF.

-   [PurchaseOrderClient.vbs](#purchaseorderclientvbs)

## <a name="purchaseorderclientvbs"></a>PurchaseOrderClient.vbs


```VB
set obj = GetObject("service:mexAddress='net.tcp://localhost/example/mex', address='net.tcp://localhost/example', contract='IPurchaseOrder', contractNamespace='http://example.org', binding=PurchaseOrderBinding, bindingNamespace='http://example.org'")
for i = 1 to 100
 orderId = obj.Order(i,"Pencil", date)
 Wscript.Echo orderId, date
Next 


```



 

 




