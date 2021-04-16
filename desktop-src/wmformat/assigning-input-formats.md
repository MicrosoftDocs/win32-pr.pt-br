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
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498972"
---
# <a name="assigning-input-formats"></a><span data-ttu-id="4b0ff-111">Atribuindo formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="4b0ff-111">Assigning Input Formats</span></span>

<span data-ttu-id="4b0ff-112">Quando você tiver identificado o formato de entrada que corresponde aos seus dados, poderá defini-lo para uso pelo gravador chamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).</span><span class="sxs-lookup"><span data-stu-id="4b0ff-112">When you have identified the input format that matches your data, you can set it for use by the writer by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).</span></span>

<span data-ttu-id="4b0ff-113">Para fluxos de vídeo, você deve definir o tamanho dos quadros nos exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-113">For video streams, you must set the size of the frames in the input samples.</span></span> <span data-ttu-id="4b0ff-114">O código de exemplo a seguir demonstra como configurar e definir uma entrada de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-114">The following example code demonstrates how to configure and set a video input.</span></span> <span data-ttu-id="4b0ff-115">Ele usa a função **FindInputFormat** definida na seção [para enumerar formatos de entrada](to-enumerate-input-formats.md) para obter o formato de entrada para vídeo RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="4b0ff-115">It uses the **FindInputFormat** function defined in the [To Enumerate Input Formats](to-enumerate-input-formats.md) section to get the input format for 24-bit RGB video.</span></span> <span data-ttu-id="4b0ff-116">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="4b0ff-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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





## <a name="related-topics"></a><span data-ttu-id="4b0ff-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b0ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0ff-118">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="4b0ff-118">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




