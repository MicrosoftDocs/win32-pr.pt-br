---
title: Tamanho do IAgentNotifySink
description: Tamanho do IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430dc26dc4f7bb8f5c5e68fe5e9898d62f16b3480b8d8969726e8c2bec02da74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692612"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink:: tamanho

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




