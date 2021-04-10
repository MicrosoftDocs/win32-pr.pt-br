---
title: GetPosition IAgentCharacter
description: GetPosition IAgentCharacter
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292879"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="580af-103">IAgentCharacter:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="580af-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="580af-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="580af-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="580af-105">Recupera a posição do quadro de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="580af-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="580af-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="580af-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="580af-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="580af-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="580af-108">Endereço de uma variável que recebe a coordenada de tela da borda esquerda do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="580af-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="580af-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="580af-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="580af-110">Endereço de uma variável que recebe a coordenada de tela da borda superior do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="580af-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="580af-111">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.</span><span class="sxs-lookup"><span data-stu-id="580af-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="580af-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="580af-112">See Also</span></span>

<span data-ttu-id="580af-113">[**IAgentCharacter:: SETPOSITION**](iagentcharacter--setposition.md), [ **IAgentCharacter:: GetSize**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="580af-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




