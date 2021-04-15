---
title: Tamanho do IAgentNotifySink
description: Tamanho do IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498750"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink:: tamanho

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Notifica um aplicativo cliente quando o caractere é redimensionado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere que foi redimensionado.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

A largura do quadro de animação do caractere em pixels.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

A altura do quadro de animação do caractere em pixels.

</dd> </dl>

Esse evento é enviado a todos os clientes do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetSize**](iagentcharacter--getsize.md), [ **IAgentCharacter:: SetSize**](iagentcharacter--setsize.md)


 

 




