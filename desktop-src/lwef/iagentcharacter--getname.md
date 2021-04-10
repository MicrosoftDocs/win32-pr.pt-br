---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292880"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="e6a84-103">IAgentCharacter:: GetName</span><span class="sxs-lookup"><span data-stu-id="e6a84-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="e6a84-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6a84-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="e6a84-105">Recupera o nome do caractere.</span><span class="sxs-lookup"><span data-stu-id="e6a84-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="e6a84-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e6a84-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e6a84-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="e6a84-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="e6a84-108">O endereço de um BSTR que recebe o valor do nome para o caractere.</span><span class="sxs-lookup"><span data-stu-id="e6a84-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e6a84-109">O nome padrão de um caractere é definido quando ele é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e6a84-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e6a84-110">O nome de um caractere pode variar com base na ID de idioma do caractere.</span><span class="sxs-lookup"><span data-stu-id="e6a84-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="e6a84-111">Os caracteres podem ser compilados com nomes diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e6a84-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="e6a84-112">Você também pode definir o nome do caractere usando **IAgentCharacter: SetName**; no entanto, isso altera o nome de todos os clientes atuais do caractere.</span><span class="sxs-lookup"><span data-stu-id="e6a84-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6a84-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e6a84-113">See Also</span></span>

[<span data-ttu-id="e6a84-114">**IAgentCharacter:: SetName**</span><span class="sxs-lookup"><span data-stu-id="e6a84-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




