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
ms.openlocfilehash: 6dcbb9f0c9c39da17c4f60af3dfb9c3a7e0179ebf4c8ed6e5bcac4cdc6f24828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496706"
---
# <a name="drawing-data"></a>Dados de desenho

O exemplo a seguir usa a função [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) e as macros [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop), [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)e [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) para desenhar dados na tela.


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



 

 




