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
# <a name="iagentcharacterwait"></a><span data-ttu-id="763fa-103">IAgentCharacter:: aguardar</span><span class="sxs-lookup"><span data-stu-id="763fa-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="763fa-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="763fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="763fa-105">Mantém a fila de animação do caractere na animação especificada (solicitação) até que outra solicitação de outro caractere seja concluída.</span><span class="sxs-lookup"><span data-stu-id="763fa-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="763fa-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="763fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="763fa-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="763fa-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="763fa-108">A ID da solicitação a ser esperada.</span><span class="sxs-lookup"><span data-stu-id="763fa-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="763fa-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="763fa-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="763fa-110">Endereço de uma variável que recebe a ID da solicitação de **espera** .</span><span class="sxs-lookup"><span data-stu-id="763fa-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="763fa-111">Use esse método somente quando você der suporte a vários caracteres (simultâneos) e quiser sequenciar sua interação.</span><span class="sxs-lookup"><span data-stu-id="763fa-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="763fa-112">(Para um único caractere, cada solicitação de animação é executada sequencialmente--após a conclusão da solicitação anterior.) Se você tiver dois caracteres e quiser que a solicitação de animação de um caractere aguarde até que a animação do outro caractere seja concluída, defina o método **Wait** como a ID de solicitação de animação do outro caractere.</span><span class="sxs-lookup"><span data-stu-id="763fa-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




