---
title: IAgentCharacter Stop
description: IAgentCharacter Stop
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114776"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter::Stop

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

A ID da solicitação a ser parada.

</dd> </dl>

**A** parada também pode ser usada para interromper todas as chamadas de [**Preparação**](iagentcharacter--prepare.md) na fila.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter::StopAll**](iagentcharacter--stopall.md)


 

 




