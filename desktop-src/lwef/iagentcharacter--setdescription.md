---
title: IAgentCharacter setdescritivo
description: IAgentCharacter setdescritivo
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364497"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="4ff10-103">IAgentCharacter:: SetDescription</span><span class="sxs-lookup"><span data-stu-id="4ff10-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="4ff10-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ff10-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="4ff10-105">Define a descrição do caractere.</span><span class="sxs-lookup"><span data-stu-id="4ff10-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="4ff10-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4ff10-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4ff10-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span><span class="sxs-lookup"><span data-stu-id="4ff10-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="4ff10-108">Um BSTR que define a descrição para o caractere.</span><span class="sxs-lookup"><span data-stu-id="4ff10-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="4ff10-109">A descrição padrão de um caractere é definida quando é compilada com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4ff10-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4ff10-110">A configuração descrição é opcional e pode não ser fornecida para todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="4ff10-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="4ff10-111">Você pode alterar a descrição do caractere usando **IAgentCharacter:: SetDescription**; no entanto, esse valor não é persistente (armazenado permanentemente).</span><span class="sxs-lookup"><span data-stu-id="4ff10-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="4ff10-112">A descrição do caractere é revertida para sua configuração padrão sempre que o caractere é carregado pela primeira vez por um cliente.</span><span class="sxs-lookup"><span data-stu-id="4ff10-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4ff10-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ff10-113">See Also</span></span>

[<span data-ttu-id="4ff10-114">**IAgentCharacter:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="4ff10-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




