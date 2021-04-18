---
description: Um dispositivo de captura de vídeo pode dar suporte a um intervalo de taxas de quadros.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Como definir a taxa de quadros de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760603"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="43492-103">Como definir a taxa de quadros de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="43492-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="43492-104">Um dispositivo de captura de vídeo pode dar suporte a um intervalo de taxas de quadros.</span><span class="sxs-lookup"><span data-stu-id="43492-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="43492-105">Se essas informações estiverem disponíveis, as taxas de quadros mínima e máxima serão armazenadas como atributos de tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="43492-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="43492-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="43492-106">Attribute</span></span>                                                         | <span data-ttu-id="43492-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="43492-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="43492-108">intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ máx.</span><span class="sxs-lookup"><span data-stu-id="43492-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="43492-109">Taxa máxima de quadros.</span><span class="sxs-lookup"><span data-stu-id="43492-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="43492-110">intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ min</span><span class="sxs-lookup"><span data-stu-id="43492-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="43492-111">Taxa mínima de quadros.</span><span class="sxs-lookup"><span data-stu-id="43492-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="43492-112">O intervalo pode variar dependendo do formato de captura.</span><span class="sxs-lookup"><span data-stu-id="43492-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="43492-113">Por exemplo, em tamanhos de quadros maiores, a taxa máxima de quadros pode ser reduzida.</span><span class="sxs-lookup"><span data-stu-id="43492-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="43492-114">Para definir a taxa de quadros:</span><span class="sxs-lookup"><span data-stu-id="43492-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="43492-115">Crie a origem de mídia para o dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="43492-115">Create the media source for the capture device.</span></span> <span data-ttu-id="43492-116">Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="43492-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="43492-117">Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia para obter o descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="43492-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="43492-118">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obter o descritor de fluxo para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="43492-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="43492-119">Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="43492-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="43492-120">Enumere os formatos de captura, conforme descrito em [como definir o formato de captura de vídeo](how-to-set-the-video-capture-format.md).</span><span class="sxs-lookup"><span data-stu-id="43492-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="43492-121">Selecione o formato de saída desejado na lista.</span><span class="sxs-lookup"><span data-stu-id="43492-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="43492-122">Consulte o tipo de mídia para o intervalo de taxa de quadros do [MF \_ MT \_ \_ \_ \_ máximo](mf-mt-frame-rate-range-max.md) e o [intervalo de taxa de quadro do MF \_ MT \_ \_ \_ \_ ](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="43492-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="43492-123">Esses valores fornecem o intervalo de taxas de quadros com suporte.</span><span class="sxs-lookup"><span data-stu-id="43492-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="43492-124">O dispositivo pode dar suporte a outras taxas de quadros dentro desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="43492-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="43492-125">Defina o atributo de [**\_ \_ quadro MF MT**](mf-mt-frame-rate-attribute.md) no tipo de mídia para especificar a taxa de quadros desejada.</span><span class="sxs-lookup"><span data-stu-id="43492-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="43492-126">Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) com o tipo de mídia modificado.</span><span class="sxs-lookup"><span data-stu-id="43492-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="43492-127">O exemplo a seguir define a taxa de quadros igual à taxa máxima de quadros que o dispositivo dá suporte:</span><span class="sxs-lookup"><span data-stu-id="43492-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="43492-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43492-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43492-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="43492-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



