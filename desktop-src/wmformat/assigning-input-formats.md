---
title: Atribuindo formatos de entrada
description: Atribuindo formatos de entrada
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- ASF (Advanced Systems Format), atribuindo formatos de entrada
- ASF (formato de sistemas avançados), atribuindo formatos de entrada
- perfis, atribuindo formatos de entrada
- codecs, atribuindo formatos de entrada
- ASF (Advanced Systems Format), atribuições de formato de entrada
- ASF (formato de sistemas avançados), atribuições de formato de entrada
- perfis, atribuições de formato de entrada
- codecs, atribuições de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f87ec74bc5d3750d65ecc91e2df4640a6ed02c9e9a9425b27897e70f825983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840326"
---
# <a name="assigning-input-formats"></a>Atribuindo formatos de entrada

Quando você tiver identificado o formato de entrada que corresponde aos seus dados, poderá defini-lo para uso pelo gravador chamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).

Para fluxos de vídeo, você deve definir o tamanho dos quadros nos exemplos de entrada. O código de exemplo a seguir demonstra como configurar e definir uma entrada de vídeo. Ele usa a função **FindInputFormat** definida na seção [para enumerar formatos de entrada](to-enumerate-input-formats.md) para obter o formato de entrada para vídeo RGB de 24 bits. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Get the size of the media type structure.
    hr = pProps->GetMediaType(NULL, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Allocate memory for the media type structure.
    pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
    if (pType == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }
    
    // Get the media type structure.
    hr = pProps->GetMediaType(pType, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 




