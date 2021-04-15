---
description: Configurar o formato de saída de vídeo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurar o formato de saída de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555916"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="56262-103">Configurar o formato de saída de vídeo</span><span class="sxs-lookup"><span data-stu-id="56262-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="56262-104">A funcionalidade descrita neste tópico foi preterida.</span><span class="sxs-lookup"><span data-stu-id="56262-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="56262-105">Para configurar o formato de saída do dispositivo de captura, um aplicativo deve usar a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) retornada por [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) no parâmetro *PGTO* .</span><span class="sxs-lookup"><span data-stu-id="56262-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="56262-106">Um dispositivo de captura pode dar suporte a um intervalo de formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="56262-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="56262-107">Por exemplo, um dispositivo pode dar suporte a RGB de 16 bits, a RGB de 32 bits e a YUYV.</span><span class="sxs-lookup"><span data-stu-id="56262-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="56262-108">Dentro de cada um desses formatos, o dispositivo pode dar suporte a um intervalo de tamanhos de quadros.</span><span class="sxs-lookup"><span data-stu-id="56262-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="56262-109">Em um dispositivo WDM, a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) é usada para relatar quais formatos são compatíveis com o dispositivo e para definir o formato.</span><span class="sxs-lookup"><span data-stu-id="56262-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="56262-110">(Para dispositivos VFW herdados, use a caixa de diálogo VFW do formato de vídeo, conforme descrito em [exibir caixas de diálogo de captura do VFW](display-vfw-capture-dialog-boxes.md).) A interface **IAMStreamConfig** é exposta no PIN de captura do filtro de captura, no PIN de visualização ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="56262-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="56262-111">Use o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para obter o ponteiro de interface:</span><span class="sxs-lookup"><span data-stu-id="56262-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="56262-112">O dispositivo tem uma lista de tipos de mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="56262-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="56262-113">Para cada tipo de mídia, o dispositivo também fornece um conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="56262-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="56262-114">Isso inclui o intervalo de tamanhos de quadro que estão disponíveis para esse formato, quão bem o dispositivo pode alongar ou reduzir a imagem e o intervalo de taxas de quadros.</span><span class="sxs-lookup"><span data-stu-id="56262-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="56262-115">Para obter o número de tipos de mídia, chame o método [**IAMStreamConfig:: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="56262-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="56262-116">O método retorna dois valores:</span><span class="sxs-lookup"><span data-stu-id="56262-116">The method returns two values:</span></span>

-   <span data-ttu-id="56262-117">O número de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="56262-117">The number of media types.</span></span>
-   <span data-ttu-id="56262-118">O tamanho da estrutura que contém as informações de recursos.</span><span class="sxs-lookup"><span data-stu-id="56262-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="56262-119">O valor de tamanho é necessário porque a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) é usada para áudio e vídeo (e pode ser estendida para outros tipos de mídia).</span><span class="sxs-lookup"><span data-stu-id="56262-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="56262-120">Para vídeo, os recursos são descritos usando a [**estrutura \_ \_ \_ Caps de configuração do fluxo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , enquanto o áudio usa a estrutura [**\_ \_ \_ Caps de configuração do fluxo de áudio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="56262-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="56262-121">Para enumerar os tipos de mídia, chame o método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) com um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="56262-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="56262-122">O método **GetStreamCaps** retorna um tipo de mídia e a estrutura de recursos correspondente:</span><span class="sxs-lookup"><span data-stu-id="56262-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="56262-123">Observe como as estruturas são alocadas para o método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="56262-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="56262-124">O método aloca a estrutura do tipo de mídia, enquanto o chamador aloca a estrutura de recursos.</span><span class="sxs-lookup"><span data-stu-id="56262-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="56262-125">Forçar a estrutura de recursos para um ponteiro de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="56262-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="56262-126">Depois de concluir o tipo de mídia, exclua a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , juntamente com o bloco de formato do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="56262-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="56262-127">Você pode configurar o dispositivo para usar um formato retornado no método [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="56262-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="56262-128">Basta chamar [**IAMStreamConfig:: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) com o tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="56262-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="56262-129">Se o PIN não estiver conectado, ele tentará usar esse formato quando ele se conectar.</span><span class="sxs-lookup"><span data-stu-id="56262-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="56262-130">Se o PIN já estiver conectado, ele tentará se reconectar usando o novo formato.</span><span class="sxs-lookup"><span data-stu-id="56262-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="56262-131">Em ambos os casos, é possível que o filtro downstream rejeite o formato.</span><span class="sxs-lookup"><span data-stu-id="56262-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="56262-132">Você também pode modificar o tipo de mídia antes de passá-lo para o método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) .</span><span class="sxs-lookup"><span data-stu-id="56262-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="56262-133">É aí que entra a estrutura de [**limites de configuração do fluxo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="56262-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="56262-134">Ele descreve todas as maneiras válidas de alterar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="56262-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="56262-135">Para usar essas informações, você deve entender os detalhes desse tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="56262-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="56262-136">Por exemplo, suponha que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retorne um formato RGB de 24 bits, com um tamanho de quadro de 320 x 240 pixels.</span><span class="sxs-lookup"><span data-stu-id="56262-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="56262-137">Você pode obter essas informações examinando o tipo principal, subtipo e bloco de formato do tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="56262-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="56262-138">A estrutura de [**configuração de fluxo de vídeo em \_ \_ \_ maiúsculas**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) fornece a largura e a altura mínima e máxima que podem ser usadas para esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="56262-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="56262-139">Ele também fornece o tamanho da "etapa", que define os incrementos pelos quais é possível ajustar a largura ou a altura.</span><span class="sxs-lookup"><span data-stu-id="56262-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="56262-140">Por exemplo, o dispositivo pode retornar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="56262-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="56262-141">MinOutputSize: 160 x 120</span><span class="sxs-lookup"><span data-stu-id="56262-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="56262-142">MaxOutputSize: 320 x 240</span><span class="sxs-lookup"><span data-stu-id="56262-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="56262-143">OutputGranularityX: 8 pixels (tamanho da etapa horizontal)</span><span class="sxs-lookup"><span data-stu-id="56262-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="56262-144">OutputGranularityY: 8 pixels (tamanho da etapa vertical)</span><span class="sxs-lookup"><span data-stu-id="56262-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="56262-145">Considerando esses números, você pode definir a largura como qualquer coisa no intervalo (160, 168, 176,... 304, 312, 320) e a altura para qualquer coisa no intervalo (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="56262-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="56262-146">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="56262-146">The following diagram illustrates this process.</span></span>

![tamanhos de formato de vídeo](images/strmcap3.png)

<span data-ttu-id="56262-148">Para definir um novo tamanho de quadro, modifique diretamente a estrutura [**am \_ Media \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type) retornada em [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span><span class="sxs-lookup"><span data-stu-id="56262-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="56262-149">Em seguida, passe o tipo de mídia para o método [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="56262-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="56262-150">Os membros **MinFrameInterval** e **MaxFrameInterval** das [**\_ \_ \_ tampas de configuração de fluxo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) são o comprimento mínimo e máximo de cada quadro de vídeo, que pode ser convertido em taxas de quadros da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="56262-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="56262-151">Para solicitar uma taxa de quadros específica, modifique o valor de **AvgTimePerFrame** na estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="56262-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="56262-152">O dispositivo pode não dar suporte a todos os valores possíveis entre o mínimo e o máximo, portanto, o driver usará o valor mais próximo possível.</span><span class="sxs-lookup"><span data-stu-id="56262-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="56262-153">Para ver qual valor o driver realmente usou, chame [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) depois de chamar [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span><span class="sxs-lookup"><span data-stu-id="56262-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="56262-154">Alguns drivers podem relatar **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) para o valor de **MaxFrameInterval**, o que, em vigor, significa que não há duração máxima.</span><span class="sxs-lookup"><span data-stu-id="56262-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="56262-155">No entanto, talvez você queira impor uma taxa de quadros mínima em seu aplicativo, como 1 fps.</span><span class="sxs-lookup"><span data-stu-id="56262-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56262-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56262-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56262-157">Sobre os tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="56262-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="56262-158">Configurando um dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="56262-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



