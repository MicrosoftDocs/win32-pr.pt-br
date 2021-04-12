---
title: Criando um coletor de notificação
description: Criando um coletor de notificação
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364413"
---
# <a name="creating-a-notification-sink"></a>Criando um coletor de notificação

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para ser notificado sobre eventos pelo Microsoft Agent, você deve implementar a interface [**IAgentNotifySink**](events.md)ou [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e criar e registrar um objeto desse tipo seguindo as convenções com:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Lembre-se de cancelar o registro do seu coletor de notificações quando seu aplicativo desligar e liberar as interfaces do Microsoft Agent.

 

 




