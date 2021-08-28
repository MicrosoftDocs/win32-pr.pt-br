---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d208e732a2e53d574c74f1a6f0b49aa7550b10343f1ed3b8b7348ed798363c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450476"
---
# <a name="iagentnotifysinkrequeststart"></a>IAgentNotifySink::RequestStart

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

Notifica um aplicativo cliente quando uma solicitação é iniciada.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificador da solicitação iniciada.

</dd> </dl>

Esse evento permite que você acompanhe quando uma solicitação em fila começa a usar sua ID de solicitação.

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySink:: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupção**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md), [**IAgentCharacter::P Laye**](iagentcharacter--play.md), [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Fale**](iagentcharacter--speak.md), [**IAgentCharacter:: Wait**](iagentcharacter--wait.md)


 

 




