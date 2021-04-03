---
title: GetPosition IAgentCommandWindow
description: GetPosition IAgentCommandWindow
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916358"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="7c60d-103">IAgentCommandWindow:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="7c60d-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="7c60d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c60d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="7c60d-105">Recupera a posição da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="7c60d-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="7c60d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7c60d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7c60d-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="7c60d-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="7c60d-108">Endereço de uma variável que recebe a coordenada de tela da borda esquerda da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="7c60d-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="7c60d-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="7c60d-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="7c60d-110">Endereço de uma variável que recebe a coordenada de tela da borda superior da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="7c60d-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7c60d-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7c60d-111">See Also</span></span>

[<span data-ttu-id="7c60d-112">**IAgentCommandWindow::GetSize**</span><span class="sxs-lookup"><span data-stu-id="7c60d-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 




