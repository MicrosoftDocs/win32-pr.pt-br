---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292878"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="2559c-103">IAgentCharacter::GetSize</span><span class="sxs-lookup"><span data-stu-id="2559c-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="2559c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2559c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="2559c-105">Recupera o tamanho do quadro de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="2559c-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="2559c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2559c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2559c-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="2559c-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="2559c-108">Endereço de uma variável que recebe a largura do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="2559c-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2559c-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="2559c-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="2559c-110">Endereço de uma variável que recebe a altura do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="2559c-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="2559c-111">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.</span><span class="sxs-lookup"><span data-stu-id="2559c-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="2559c-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2559c-112">See Also</span></span>

[<span data-ttu-id="2559c-113">**IAgentCharacter:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="2559c-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




