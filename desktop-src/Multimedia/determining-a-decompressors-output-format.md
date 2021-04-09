---
title: Determinando o formato de saída de um descompactador
description: Determinando o formato de saída de um descompactador
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- VCM (Gerenciador de compactação de vídeo), formato de saída
- VCM (Gerenciador de compactação de vídeo), formato de saída
- Macro ICDecompressGetFormatSize
- Macro ICDecompressQuery
- Macro ICDecompressGetPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084510"
---
# <a name="determining-a-decompressors-output-format"></a>Determinando o formato de saída de um descompactador

O exemplo a seguir determina o tamanho de buffer necessário para os dados que especificam o formato de descompactação usando a macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , aloca um buffer do tamanho apropriado usando a função [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e recupera as informações de formato de descompactação usando a macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



O exemplo a seguir mostra como um aplicativo pode usar a macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) para determinar se um descompactador pode manipular os formatos de entrada e saída.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



O fragmento de código a seguir mostra como obter as informações da paleta usando a macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 