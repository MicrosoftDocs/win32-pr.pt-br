---
title: Localizando e abrindo os descompactores e os descompactores
description: Localizando e abrindo os descompactores e os descompactores
ms.assetid: ed931f01-dbfc-4fdc-b725-c062302b037b
keywords:
- VCM (gerenciador de compactação de vídeo), abrindo os vcms
- VCM (gerenciador de compactação de vídeo), abrindo os vcms
- Função ICLocate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c861c9fb5c317b6b0fc3a48552db200389739ebd8a53dbf15fbdbd0564ba8f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139297"
---
# <a name="locating-and-opening-compressors-and-decompressors"></a>Localizando e abrindo os descompactores e os descompactores

O exemplo a seguir usa a [**função ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) para localizar um que pode compactar um bitmap de 8 bits por pixel.


```C++
BITMAPINFOHEADER bih; 
HIC              hIC 
 
// Initialize the bitmap structure. 
bih.biSize = sizeof(BITMAPINFOHEADER); 
bih.biWidth = bih.biHeight = 0; 
bih.biPlanes = 1; 
bih.biCompression = BI_RGB;      // standard RGB bitmap 
bih.biBitcount = 8;              // 8 bits-per-pixel format 
bih.biSizeImage = 0; 
bih.biXPelsPerMeter = bih.biYPelsPerMeter = 0; 
bih.biClrUsed = bih.biClrImportant = 256; 
 
hIC = ICLocate (ICTYPE_VIDEO, 0L, (LPBITMAPINFOHEADER) &bih, 
    NULL, ICMODE_COMPRESS); 
 
```



O exemplo a seguir enumera os descompactores no sistema para encontrar um que possa manipular o formato de suas imagens. Este exemplo usa **ICTYPE \_ VIDEO** (que é equivalente ao código de quatro caracteres "VIDC" ) e a macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) para determinar se um descompactador ou um descompactador dá suporte ao formato de imagem.


```C++
for (i=0; ICInfo(fccType, i, &icinfo); i++) 
{ 
    hic = ICOpen(icinfo.fccType, icinfo.fccHandler, ICMODE_QUERY); 
    if (hic) 
    { 
        // Skip this compressor if it can't handle the format. 
        if (fccType == ICTYPE_VIDEO && pvIn != NULL && 
            ICDecompressQuery(hic, pvIn, NULL) != ICERR_OK) 
        { 
            ICClose(hic); 
            continue; 
        } 
 
        // Find out the compressor name. 
        ICGetInfo(hic, &icinfo, sizeof(icinfo)); 
 
        // Add it to the combo box. 
        n = ComboBox_AddString(hwndC,icinfo.szDescription); 
        ComboBox_SetItemData(hwndC, n, hic); 
    } 
} 
 
```



O exemplo a seguir tenta localizar um grupo específico para compactar o formato RGB de 8 bits em um formato RLE de 8 bits.


```C++
BITMAPINFOHEADER    bihIn, bihOut; 
HIC                 hIC 
 
// Initialize the bitmap structure. 

biSize = bihOut.biSize = sizeof(BITMAPINFOHEADER); 
bihIn.biWidth = bihIn.biHeight = bihOut.biWidth = bihOut.biHeight = 0; 
bihIn.biPlanes = bihOut.biPlanes= 1; 
bihIn.biCompression = BI_RGB;        // standard RGB bitmap for input 
bihOut.biCompression = BI_RLE8;      // 8-bit RLE for output format 
bihIn.biBitcount = bihOut.biBitCount = 8;  // 8 bits-per-pixel format 
bihIn.biSizeImage = bihOut.biSizeImage = 0; 
bihIn.biXPelsPerMeter = bih.biYPelsPerMeter = 
    bihOut.biXPelsPerMeter = bihOut.biYPelsPerMeter = 0; 
bihIn.biClrUsed = bih.biClrImportant = 
    bihOut.biClrUsed = bihOut.biClrImportant = 256; 

hIC = ICLocate (ICTYPE_VIDEO, 0L, 
    (LPBITMAPINFOHEADER)&bihIn, 
    (LPBITMAPINFOHEADER)&bihOut, ICMODE_COMPRESS); 
 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de Compactação de Vídeo](using-the-video-compression-manager.md)
</dt> </dl>

 

 




