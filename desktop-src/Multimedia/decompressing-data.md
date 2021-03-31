---
title: Descompactando dados
description: Descompactando dados
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Gerenciador de compactação de vídeo (VCM), descompactando dados
- VCM (Gerenciador de compactação de vídeo), descompactando dados
- Macro ICDecompressBegin
- Função ICDecompress
- Macro ICDecompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b44ea375bb1f2b5c41a361ca7f31387439b610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636003"
---
# <a name="decompressing-data"></a>Descompactando dados

O exemplo a seguir mostra como um aplicativo pode inicializar um descompactador usando a macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) , descompactar uma sequência de quadros usando a função [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) e encerrar a descompactação usando a macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




