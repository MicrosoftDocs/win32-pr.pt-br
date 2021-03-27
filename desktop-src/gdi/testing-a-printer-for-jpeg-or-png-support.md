---
description: A função SetDIBitsToDevice usa dados de cor de um DIB para definir os pixels no retângulo especificado no dispositivo que está associado ao contexto do dispositivo de destino.
ms.assetid: 7cbb2b7a-2d95-4352-9e75-aa814e8f01bd
title: Testando uma impressora para suporte a JPEG ou PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151251a99d23913b2a515a36def6172c997ac31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921452"
---
# <a name="testing-a-printer-for-jpeg-or-png-support"></a>Testando uma impressora para suporte a JPEG ou PNG

A função [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) usa dados de cor de um DIB para definir os pixels no retângulo especificado no dispositivo que está associado ao contexto do dispositivo de destino.

[**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) é estendido para permitir que uma imagem JPEG ou png seja passada como a imagem de origem.

Por exemplo:


```C++
// 
// pvJpgImage points to a buffer containing the JPEG image 
// nJpgImageSize is the size of the buffer 
// ulJpgWidth is the width of the JPEG image 
// ulJpgHeight is the height of the JPEG image 
// 

// 
// Check if CHECKJPEGFORMAT is supported (device has JPEG support) 
// and use it to verify that device can handle the JPEG image. 
// 

ul = CHECKJPEGFORMAT;

if (
    // Check if CHECKJPEGFORMAT exists: 

    (ExtEscape(hdc, QUERYESCSUPPORT,
               sizeof(ul), &ul, 0, 0) > 0) &&

    // Check if CHECKJPEGFORMAT executed without error: 

    (ExtEscape(hdc, CHECKJPEGFORMAT,
               pvJpgImage, nJpgImageSize, sizeof(ul), &ul) > 0) &&

    // Check status code returned by CHECKJPEGFORMAT: 

    (ul == 1)
   )
{
    // 
    // Initialize the BITMAPINFO. 
    // 

    memset(&bmi, 0, sizeof(bmi));
    bmi.bmiHeader.biSize        = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth       = ulJpgWidth;
    bmi.bmiHeader.biHeight      = -ulJpgHeight; // top-down image 
    bmi.bmiHeader.biPlanes      = 1;
    bmi.bmiHeader.biBitCount    = 0;
    bmi.bmiHeader.biCompression = BI_JPEG;
    bmi.bmiHeader.biSizeImage   = nJpgImageSize;

    // 
    // Do the SetDIBitsToDevice. 
    // 

    iRet = SetDIBitsToDevice(hdc,
                             ulDstX, ulDstY,
                             ulDstWidth, ulDstHeight,
                             0, 0,
                             0, ulJpgHeight,
                             pvJpgImage,
                             &bmi,
                             DIB_RGB_COLORS);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call SetDIBitsToDevice  
    // with the DIB instead. 
    // 
}
```



 

 



