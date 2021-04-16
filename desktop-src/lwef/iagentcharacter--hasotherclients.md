---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498820"
---
# <a name="iagentcharacterhasotherclients"></a><span data-ttu-id="e2c12-103">IAgentCharacter::HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="e2c12-103">IAgentCharacter::HasOtherClients</span></span>

<span data-ttu-id="e2c12-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2c12-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

<span data-ttu-id="e2c12-105">Recupera se um caractere tem outros clientes.</span><span class="sxs-lookup"><span data-stu-id="e2c12-105">Retrieves whether a character has other clients.</span></span>

-   <span data-ttu-id="e2c12-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e2c12-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e2c12-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span><span class="sxs-lookup"><span data-stu-id="e2c12-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span></span>
</dt> <dd>

<span data-ttu-id="e2c12-108">Endereço de uma variável que recebe o número de outros clientes conectados para o caractere (número total de clientes menos o cliente).</span><span class="sxs-lookup"><span data-stu-id="e2c12-108">Address of a variable that receives the number of other connected clients for the character (total number of clients minus your client).</span></span>

</dd> </dl>

 

 




