---
title: Descobrindo o formato de um arquivo
description: Descobrindo o formato de um arquivo
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media Gerenciador de Dispositivos, formatos de arquivo
- Gerenciador de Dispositivos, formatos de arquivo
- Guia de programação, formatos de arquivo
- aplicativos de área de trabalho, formatos de arquivo
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, formatos de arquivo
- gravando arquivos em dispositivos, formatos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635636"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="cbaa7-109">Descobrindo o formato de um arquivo</span><span class="sxs-lookup"><span data-stu-id="cbaa7-109">Discovering a File's Format</span></span>

<span data-ttu-id="cbaa7-110">Antes de enviar um arquivo para o dispositivo, um aplicativo deve determinar se o dispositivo dá suporte a esse formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="cbaa7-111">Descobrir o formato de um arquivo pode ser complexo.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="cbaa7-112">A maneira mais simples é criar uma lista de extensões de arquivo mapeadas para \_ valores de enumeração WMDM FORMATCODE específicos.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="cbaa7-113">No entanto, há alguns problemas com esse sistema: um é que um único formato pode ter várias extensões (como. jpg,. jpe e. jpeg para imagens JPEG).</span><span class="sxs-lookup"><span data-stu-id="cbaa7-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="cbaa7-114">Além disso, a mesma extensão de arquivo pode ser usada por programas diferentes para formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="cbaa7-115">Para superar as limitações de um mapeamento estrito, é melhor que um aplicativo Verifique se o formato corresponde à extensão.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="cbaa7-116">O SDK do DirectShow fornece ferramentas que permitem que um aplicativo Descubra um conjunto limitado de detalhes sobre a maioria dos tipos de arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="cbaa7-117">O Windows Media Format SDK expõe um grande número de detalhes, mas apenas sobre arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="cbaa7-118">Como todos os tipos de arquivo devem ter seu código de formato verificado se possível, é, portanto, melhor usar o DirectShow para descobrir ou verificar o código de formato básico e usar o SDK do Windows Media Format para descobrir quaisquer metadados adicionais desejados sobre arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="cbaa7-119">O DirectShow também pode ser usado para descobrir metadados básicos para arquivos não ASF.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="cbaa7-120">Veja a seguir uma maneira de descobrir um formato de arquivo usando o mapeamento de extensão e o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="cbaa7-121">Primeiro, compare a extensão de nome de arquivo com uma lista de extensões conhecidas.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="cbaa7-122">Certifique-se de fazer a comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="cbaa7-123">Se a extensão não for mapeada, defina o formato como WMDM \_ FORMATCODE \_ undefined.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="cbaa7-124">Se o código de formato não foi encontrado (ou se você deseja verificar se um arquivo é um arquivo de mídia), você pode executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="cbaa7-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="cbaa7-125">Crie um objeto de detector de mídia do DirectShow usando **CoCreateInstance**(CLSID \_ MediaDet) e recuperando a interface **IMediaDet** .</span><span class="sxs-lookup"><span data-stu-id="cbaa7-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="cbaa7-126">Abra o arquivo chamando **IMediaDet::p UT \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="cbaa7-127">Essa chamada falhará se o arquivo estiver protegido.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="cbaa7-128">Obtenha o tipo de mídia do fluxo padrão chamando **IMediaDet:: get \_ StreamMediaType**, que retorna um **tipo de \_ mídia \_ am**.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="cbaa7-129">Obtenha o número de fluxos chamando **IMediaDet:: get \_ OutputStreams**.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="cbaa7-130">Se houver apenas um fluxo e ele for áudio, o tipo de arquivo será WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO</span><span class="sxs-lookup"><span data-stu-id="cbaa7-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="cbaa7-131">Se houver apenas um fluxo e ele for vídeo, o tipo de arquivo será WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO</span><span class="sxs-lookup"><span data-stu-id="cbaa7-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="cbaa7-132">Se houver apenas um fluxo e ele for um vídeo e a taxa de bits for zero, o tipo de arquivo será WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="cbaa7-133">Você também pode tentar corresponder codecs de áudio ou vídeo dos membros **VIDEOINFOHEADER** ou **WAVEFORMATEX** recuperados de **Get \_ StreamMediaType**.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="cbaa7-134">A seguinte função C++ demonstra a correspondência da extensão de arquivo e o uso do DirectShow para tentar analisar arquivos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="cbaa7-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a><span data-ttu-id="cbaa7-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbaa7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbaa7-136">**Gravando arquivos no dispositivo**</span><span class="sxs-lookup"><span data-stu-id="cbaa7-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




