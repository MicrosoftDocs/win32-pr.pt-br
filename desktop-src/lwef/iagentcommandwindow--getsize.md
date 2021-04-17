---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764270"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="c3675-103">IAgentCommandWindow::GetSize</span><span class="sxs-lookup"><span data-stu-id="c3675-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="c3675-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3675-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="c3675-105">Recupera o tamanho atual da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c3675-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="c3675-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c3675-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c3675-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="c3675-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="c3675-108">Endereço de uma variável que recebe a largura da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="c3675-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="c3675-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="c3675-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="c3675-110">Endereço de uma variável que recebe a altura da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="c3675-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c3675-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c3675-111">See Also</span></span>

[<span data-ttu-id="c3675-112">**IAgentCommandWindow:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="c3675-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 




