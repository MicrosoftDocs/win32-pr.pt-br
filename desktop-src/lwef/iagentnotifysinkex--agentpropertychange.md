---
title: Agente IAgentNotifySinkExPropertyChange
description: Agente IAgentNotifySinkExPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961486"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Notifica um aplicativo cliente quando o usuário altera uma configuração de propriedade do Microsoft Agent.

-   Sem valor de retorno.

Quando o usuário altera uma configuração de propriedade do Microsoft Agent na folha de propriedades do Microsoft Agent, o servidor envia esse evento para todos os clientes, a menos que o servidor esteja suspenso no momento.

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




