---
title: IAgentNotifySink ocioso
description: IAgentNotifySink ocioso
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105162"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink::Idle

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica um aplicativo cliente quando o estado de **Idling** de um caractere é alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador da solicitação iniciada.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

Sinalizador de início. Esse valor booliana é **True** quando o caractere começa a idling e **False** quando ele para a idling.

</dd> </dl>

Esse evento permite que você acompanhe quando o servidor do Microsoft Agent inicia ou interrompe o processamento ocioso de um caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::GetIdleOn,**](iagentcharacter--getidleon.md) [ **IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




