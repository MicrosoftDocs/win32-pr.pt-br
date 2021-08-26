---
title: Espera de IAgentCharacter
description: Espera de IAgentCharacter
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014215"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter::Wait

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Mantém a fila de animação do caractere na animação especificada (solicitação) até que outra solicitação para outro caractere seja concluída.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

A ID da solicitação a ser aguardada.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID **da** solicitação de espera.

</dd> </dl>

Use esse método somente quando você dar suporte a vários caracteres (simultâneos) e quiser sequenciar sua interação. (Para um único caractere, cada solicitação de animação é tocada sequencialmente – após a conclusão da solicitação anterior.) Se você tiver dois caracteres e quiser que a solicitação de animação de um caractere aguarde até que a animação do outro caractere seja concluída, de definir o método **Wait** como a ID da solicitação de animação do outro caractere.

 

 




