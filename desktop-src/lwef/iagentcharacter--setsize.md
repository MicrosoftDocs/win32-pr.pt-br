---
title: SetSize IAgentCharacter
description: SetSize IAgentCharacter
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636797"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="241e9-103">IAgentCharacter:: SetSize</span><span class="sxs-lookup"><span data-stu-id="241e9-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="241e9-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="241e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="241e9-105">Define o tamanho do quadro de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="241e9-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="241e9-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="241e9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="241e9-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="241e9-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="241e9-108">A largura do quadro de animação do caractere em pixels.</span><span class="sxs-lookup"><span data-stu-id="241e9-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="241e9-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="241e9-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="241e9-110">A altura do quadro de animação do caractere em pixels.</span><span class="sxs-lookup"><span data-stu-id="241e9-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="241e9-111">A alteração do tamanho do quadro do caractere dimensiona o caractere para o tamanho definido com esse método.</span><span class="sxs-lookup"><span data-stu-id="241e9-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="241e9-112">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="241e9-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="241e9-113">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.</span><span class="sxs-lookup"><span data-stu-id="241e9-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="241e9-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="241e9-114">See Also</span></span>

[<span data-ttu-id="241e9-115">**IAgentCharacter::GetSize**</span><span class="sxs-lookup"><span data-stu-id="241e9-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




