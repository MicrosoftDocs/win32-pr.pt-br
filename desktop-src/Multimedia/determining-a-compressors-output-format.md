---
title: Determinando o formato de saída de um compressor
description: Determinando o formato de saída de um compressor
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- VCM (Gerenciador de compactação de vídeo), formato de saída
- VCM (Gerenciador de compactação de vídeo), formato de saída
- Macro ICCompressGetFormat
- Macro ICCompressQuery
- Macro ICCompressGetSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084539"
---
# <a name="determining-a-compressors-output-format"></a><span data-ttu-id="accc1-108">Determinando o formato de saída de um compressor</span><span class="sxs-lookup"><span data-stu-id="accc1-108">Determining a Compressor's Output Format</span></span>

<span data-ttu-id="accc1-109">O exemplo a seguir usa a macro tamanho [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) para determinar o tamanho de buffer necessário para os dados que especificam o formato de compactação, aloca um buffer do tamanho apropriado usando a função [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e recupera as informações de formato de compactação usando a macro **ICCompressGetFormat** .</span><span class="sxs-lookup"><span data-stu-id="accc1-109">The following example uses the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size macro to determine the buffer size needed for the data specifying the compression format, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the compression format information using the **ICCompressGetFormat** macro.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="accc1-110">O exemplo a seguir usa a macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) para determinar se um compressor pode manipular os formatos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="accc1-110">The following example uses the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro to determine whether a compressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



<span data-ttu-id="accc1-111">O exemplo a seguir usa a macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) para determinar o tamanho do buffer e aloca um buffer desse tamanho usando [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="accc1-111">The following example uses the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro to determine the buffer size, and it allocates a buffer of that size using [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span></span>


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 