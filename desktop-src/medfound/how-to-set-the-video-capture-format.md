---
description: Um dispositivo de captura de vídeo pode dar suporte A vários formatos de captura. Formatos normalmente diferem por tipo de compactação, espaço de cores (YUV ou RGB), tamanho do quadro ou taxa de quadros.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Como definir o formato de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764417"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="2b2f9-104">Como definir o formato de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2b2f9-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="2b2f9-105">Um dispositivo de captura de vídeo pode dar suporte A vários formatos de captura.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="2b2f9-106">Formatos normalmente diferem por tipo de compactação, espaço de cores (YUV ou RGB), tamanho do quadro ou taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="2b2f9-107">A lista de formatos com suporte está contida no *descritor de apresentação*.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="2b2f9-108">Para obter mais informações, consulte [descritores de apresentação](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="2b2f9-109">Para enumerar os formatos com suporte:</span><span class="sxs-lookup"><span data-stu-id="2b2f9-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="2b2f9-110">Crie a origem de mídia para o dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-110">Create the media source for the capture device.</span></span> <span data-ttu-id="2b2f9-111">Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="2b2f9-112">Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia para obter o descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="2b2f9-113">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obter o descritor de fluxo para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="2b2f9-114">Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="2b2f9-115">Chame [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) para obter o número de formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="2b2f9-116">Em um loop, chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obter cada formato.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="2b2f9-117">O formato é representado por um *tipo de mídia*.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="2b2f9-118">Para obter mais informações, consulte [tipos de mídia de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="2b2f9-119">O exemplo a seguir enumera os formatos de captura para um dispositivo:</span><span class="sxs-lookup"><span data-stu-id="2b2f9-119">The following example enumerates the capture formats for a device:</span></span>


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="2b2f9-120">A `LogMediaType` função usada neste exemplo é listada no tópico [tipo de mídia depuração código](media-type-debugging-code.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="2b2f9-121">Para definir o formato de captura:</span><span class="sxs-lookup"><span data-stu-id="2b2f9-121">To set the capture format:</span></span>

1.  <span data-ttu-id="2b2f9-122">Obtenha um ponteiro para a interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="2b2f9-123">Chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obter o formato desejado, especificado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="2b2f9-124">Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para definir o formato.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="2b2f9-125">Se você não definir o formato de captura, o dispositivo usará seu formato padrão.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="2b2f9-126">O exemplo a seguir define o formato de captura:</span><span class="sxs-lookup"><span data-stu-id="2b2f9-126">The following example sets the capture format:</span></span>


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="2b2f9-127">A ordem na qual os formatos são retornados depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="2b2f9-128">Normalmente, eles são agrupados primeiro por tipo de compactação ou espaço de cores; e, em seguida, do menor tamanho de quadro para o maior tamanho de quadro dentro de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="2b2f9-129">A taxa de quadros é tratada de forma ligeiramente diferente dos outros atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="2b2f9-130">Para obter mais informações, consulte [como definir a taxa de quadros de captura de vídeo](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="2b2f9-131">Em alguns dispositivos, a lista de formatos conterá uma entrada duplicada para cada formato.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="2b2f9-132">Por exemplo, se o dispositivo der suporte a 15 formatos de captura distintos, a lista conterá 30 entradas.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="2b2f9-133">Dentro de cada par, um dos tipos de mídia terá o atributo [**MF \_ MT \_ am \_ Format \_ Type**](mf-mt-am-format-type-attribute.md) igual ao **Format \_ VIDEOINFO**, e o outro terá o **\_ tipo de \_ \_ formato \_ MF MT am** igual ao **formato \_ VideoInfo2**.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="2b2f9-134">(Esses dois valores são definidos no arquivo de cabeçalho UUIDs. h.) O segundo tipo também pode conter informações de cores adicionais ([informações de cores estendidas](extended-color-information.md)) ou mostrar um valor diferente para entrelaçamento ([**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="2b2f9-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="2b2f9-135">Esses tipos duplicados existem para dar suporte a aplicativos mais antigos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="2b2f9-136">Em um aplicativo Media Foundation, você deve ignorar o **formato \_ VIDEOINFO** tipo sempre que um tipo de **\_ VideoInfo2 de formato** duplicado estiver listado.</span><span class="sxs-lookup"><span data-stu-id="2b2f9-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b2f9-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b2f9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b2f9-138">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2b2f9-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



