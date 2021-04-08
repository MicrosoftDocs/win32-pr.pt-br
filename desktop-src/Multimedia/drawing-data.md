---
title: Dados de desenho
description: Dados de desenho
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- VCM (Gerenciador de compactação de vídeo), desenho
- VCM (Gerenciador de compactação de vídeo), desenho
- Função ICDraw
- Macro ICDrawStart
- Macro ICDrawStop
- Macro ICDrawFlush
- Macro ICDrawEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f598ef47bbbf6b8f53c7fb2639c9ddff1390ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005273"
---
# <a name="drawing-data"></a><span data-ttu-id="8ae3d-110">Dados de desenho</span><span class="sxs-lookup"><span data-stu-id="8ae3d-110">Drawing Data</span></span>

<span data-ttu-id="8ae3d-111">O exemplo a seguir usa a função [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) e as macros [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop), [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)e [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) para desenhar dados na tela.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-111">The following example uses the [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) function and the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop), [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush), and [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macros to draw data on the screen.</span></span>


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




