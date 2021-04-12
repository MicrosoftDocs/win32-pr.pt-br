---
title: IAgentCharacter parar
description: IAgentCharacter parar
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364254"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter:: Stop

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Interrompe a animação especificada (solicitação) e a remove da fila de animação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

A ID da solicitação a ser interrompida.

</dd> </dl>

**Stop** também pode ser usado para interromper qualquer chamada de [**preparação**](iagentcharacter--prepare.md) em fila.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::P reparêntese**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)


 

 




