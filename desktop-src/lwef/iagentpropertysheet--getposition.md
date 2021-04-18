---
title: GetPosition IAgentPropertySheet
description: GetPosition IAgentPropertySheet
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789293"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="e8633-103">IAgentPropertySheet:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="e8633-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="e8633-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8633-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="e8633-105">Recupera a posição da janela da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e8633-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="e8633-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8633-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e8633-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="e8633-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="e8633-108">Endereço de uma variável que recebe a coordenada de tela da borda esquerda da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="e8633-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="e8633-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="e8633-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="e8633-110">Endereço de uma variável que recebe a coordenada de tela da borda superior da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="e8633-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e8633-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e8633-111">See Also</span></span>

[<span data-ttu-id="e8633-112">**IAgentPropertySheet::GetSize**</span><span class="sxs-lookup"><span data-stu-id="e8633-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




