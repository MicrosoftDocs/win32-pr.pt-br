---
title: IAgentCharacter aguardar
description: IAgentCharacter aguardar
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292542"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter:: aguardar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Mantém a fila de animação do caractere na animação especificada (solicitação) até que outra solicitação de outro caractere seja concluída.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

A ID da solicitação a ser esperada.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de **espera** .

</dd> </dl>

Use esse método somente quando você der suporte a vários caracteres (simultâneos) e quiser sequenciar sua interação. (Para um único caractere, cada solicitação de animação é executada sequencialmente--após a conclusão da solicitação anterior.) Se você tiver dois caracteres e quiser que a solicitação de animação de um caractere aguarde até que a animação do outro caractere seja concluída, defina o método **Wait** como a ID de solicitação de animação do outro caractere.

 

 




