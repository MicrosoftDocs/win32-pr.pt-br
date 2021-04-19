---
title: IAgentNotifySink ocioso
description: IAgentNotifySink ocioso
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811631"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink:: Idle

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica um aplicativo cliente quando o estado de **deixar** de um caractere é alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador da solicitação iniciada.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bIniciar*
</dt> <dd>

Sinalizador de início. Esse valor booliano é **true** quando o caractere começa deixar e **false** quando ele para deixar.

</dd> </dl>

Esse evento permite que você acompanhe quando o servidor do Microsoft Agent inicia ou para o processamento ocioso de um caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: getidlement**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: setidleion**](iagentcharacter--setidleon.md)


 

 




