---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005334"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="97ac8-103">IAgentCharacterEx::GetOriginalSize</span><span class="sxs-lookup"><span data-stu-id="97ac8-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="97ac8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="97ac8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="97ac8-105">Recupera o tamanho original do quadro de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="97ac8-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="97ac8-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="97ac8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="97ac8-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="97ac8-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="97ac8-108">Endereço de uma variável que recebe a largura original do quadro de animação de caracteres em pixels.</span><span class="sxs-lookup"><span data-stu-id="97ac8-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="97ac8-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="97ac8-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="97ac8-110">Endereço de uma variável que recebe a altura original do quadro de animação de caracteres em pixels.</span><span class="sxs-lookup"><span data-stu-id="97ac8-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="97ac8-111">Essa chamada retorna o tamanho original do quadro de caracteres como interno no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="97ac8-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="97ac8-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="97ac8-112">See Also</span></span>

[<span data-ttu-id="97ac8-113">**IAgentCharacter::GetSize**</span><span class="sxs-lookup"><span data-stu-id="97ac8-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




