---
description: Várias funções usam o pincel atualmente selecionado em um contexto de dispositivo para executar operações de bitmap.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps como pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165092"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="12d32-103">Bitmaps como pincéis</span><span class="sxs-lookup"><span data-stu-id="12d32-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="12d32-104">Várias funções usam o pincel atualmente selecionado em um contexto de dispositivo para executar operações de bitmap.</span><span class="sxs-lookup"><span data-stu-id="12d32-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="12d32-105">Por exemplo, a função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) Replica o pincel em uma região retangular dentro de uma janela, e a função [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) Replica o pincel dentro de uma área em uma janela limitada pela cor especificada (ao contrário de **PatBlt**, **FloodFill** faz o preenchimento de formas não retangulares).</span><span class="sxs-lookup"><span data-stu-id="12d32-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="12d32-106">A função [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) Replica o pincel dentro de uma região limitada por uma cor especificada.</span><span class="sxs-lookup"><span data-stu-id="12d32-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="12d32-107">No entanto, ao contrário da função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , o **FloodFill** não combina os dados de cor para o pincel com os dados de cor dos pixels na exibição; Ele simplesmente define a cor de todos os pixels dentro da região incluída na exibição para a cor do pincel selecionado no momento no contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12d32-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



