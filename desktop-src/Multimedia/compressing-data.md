---
title: Compactando dados
description: Compactando dados
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- Gerenciador de compressão de vídeo (VCM), compactando dados
- VCM (Gerenciador de compactação de vídeo), compactando dados
- Macro ICCompressBegin
- Função ICCompress
- Macro ICCompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c08308b695bf022d2d2b76bda6727d9f9c1a9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005387"
---
# <a name="compressing-data"></a>Compactando dados

O exemplo a seguir compacta os dados de imagem para uso em um arquivo AVI. Ele pressupõe que o compressor não dá suporte aos sinalizadores VIDCF de VIDCF ou de demarcações \_ \_ temporais, mas oferece suporte à qualidade de VIDCF \_ . O exemplo usa a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) , a função [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) e a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
DWORD dwCkID; 
DWORD dwCompFlags; 
DWORD dwQuality; 
LONG  lNumFrames, lFrameNum; 
// Assume dwNumFrames is initialized to the total number of frames. 
// Assume dwQuality holds the proper quality value (0-10000). 
// Assume lpbiOut, lpOut, lpbiIn, and lpIn are initialized properly. 
 
// If OK to start, compress each frame. 
if (ICCompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for ( lFrameNum = 0; lFrameNum < lNumFrames; lFrameNum++)
    { 
        if (ICCompress(hIC, 0, lpbiOut, lpOut, lpbiIn, lpIn, 
            &dwCkID, &dwCompFlags, lFrameNum, 
            0, dwQuality, NULL, NULL) == ICERR_OK)
        { 
            // Write compressed data to the AVI file. 
             
            // Set lpIn to the next frame in the sequence. 
             
        } 
        else 
        { 
            // Handle compressor error. 
        } 
    } 
    ICCompressEnd(hIC);    // terminate compression 
} 
else 
{ 
    // Handle the error identifying the unsupported format. 
} 
 
```



 

 




