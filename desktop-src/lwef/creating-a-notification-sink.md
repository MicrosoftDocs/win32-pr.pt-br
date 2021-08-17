---
title: Criando um sink de notificação
description: Criando um sink de notificação
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480088"
---
# <a name="creating-a-notification-sink"></a>Criando um sink de notificação

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para ser notificado sobre eventos pelo Microsoft Agent, você deve implementar a interface [**IAgentNotifySink**](events.md)ou [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e criar e registrar um objeto desse tipo seguindo as convenções COM:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Lembre-se de encerrar o registro do seu sink de notificação quando o aplicativo for desligado e liberar as interfaces do Microsoft Agent.

 

 




