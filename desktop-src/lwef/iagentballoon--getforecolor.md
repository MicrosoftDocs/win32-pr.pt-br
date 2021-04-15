---
title: GetForeColor IAgentBalloon
description: GetForeColor IAgentBalloon
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105768310"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="86b35-103">IAgentBalloon:: GetForeColor</span><span class="sxs-lookup"><span data-stu-id="86b35-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="86b35-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86b35-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="86b35-105">Recupera o valor da cor de primeiro plano exibida em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="86b35-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="86b35-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="86b35-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="86b35-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span><span class="sxs-lookup"><span data-stu-id="86b35-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="86b35-108">O endereço de uma variável que recebe a configuração de cor do primeiro plano do balão.</span><span class="sxs-lookup"><span data-stu-id="86b35-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="86b35-109">A cor de primeiro plano usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="86b35-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="86b35-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86b35-110">It cannot be changed by an application.</span></span> <span data-ttu-id="86b35-111">No entanto, o usuário pode substituir a cor de primeiro plano dos balões de palavras de todos os caracteres por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="86b35-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="86b35-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="86b35-112">See Also</span></span>

[<span data-ttu-id="86b35-113">**IAgentBalloon:: GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="86b35-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




