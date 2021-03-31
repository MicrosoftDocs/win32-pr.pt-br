---
title: SETPOSITION de IAgentCharacter
description: SETPOSITION de IAgentCharacter
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005298"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="c65f4-103">IAgentCharacter:: SETPOSITION</span><span class="sxs-lookup"><span data-stu-id="c65f4-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="c65f4-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c65f4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="c65f4-105">Define a posição do quadro de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="c65f4-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="c65f4-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c65f4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c65f4-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span><span class="sxs-lookup"><span data-stu-id="c65f4-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="c65f4-108">Coordenada de tela da borda esquerda do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="c65f4-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="c65f4-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span><span class="sxs-lookup"><span data-stu-id="c65f4-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="c65f4-110">Coordenada de tela da borda superior do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="c65f4-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="c65f4-111">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="c65f4-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="c65f4-112">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.</span><span class="sxs-lookup"><span data-stu-id="c65f4-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="c65f4-113">Ao contrário do método [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , essa função não é enfileirada.</span><span class="sxs-lookup"><span data-stu-id="c65f4-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c65f4-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c65f4-114">See Also</span></span>

[<span data-ttu-id="c65f4-115">**IAgentCharacter:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="c65f4-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 




