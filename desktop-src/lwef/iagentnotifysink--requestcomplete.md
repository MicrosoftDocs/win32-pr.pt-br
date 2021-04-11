---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292689"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Notifica um aplicativo cliente quando uma solicitação é concluída.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificador da solicitação iniciada.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

Código de status. Esse parâmetro retorna o código de status para a solicitação.

</dd> </dl>

Esse evento permite que você acompanhe quando um método enfileirado é concluído usando sua ID de solicitação.

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySink:: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupção**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md), [**IAgentCharacter::P Laye**](iagentcharacter--play.md), [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Fale**](iagentcharacter--speak.md), [**IAgentCharacter:: Wait**](iagentcharacter--wait.md)


 

 




