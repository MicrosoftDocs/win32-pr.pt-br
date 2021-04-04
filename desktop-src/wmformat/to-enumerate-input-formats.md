---
title: Para enumerar formatos de entrada
description: Para enumerar formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Formato de sistema avançado (ASF), enumerando formatos de entrada
- ASF (formato de sistemas avançados), enumerando formatos de entrada
- perfis, enumerando formatos de entrada
- codecs, enumerando formatos de entrada
- ASF (Advanced Systems Format), enumerações de formato de entrada
- ASF (formato de sistemas avançados), enumerações de formato de entrada
- perfis, enumerações de formato de entrada
- codecs, enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007243"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="c2efd-111">Para enumerar formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="c2efd-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="c2efd-112">Cada um dos codecs de mídia do Windows aceita um ou mais tipos de mídia de entrada para compactação.</span><span class="sxs-lookup"><span data-stu-id="c2efd-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="c2efd-113">O Windows Media Format SDK permite que você insira uma variedade maior de formatos do que aqueles com suporte nos codecs.</span><span class="sxs-lookup"><span data-stu-id="c2efd-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="c2efd-114">O SDK faz isso executando transformações de pré-processamento nas entradas quando necessário, como redimensionar quadros de vídeo ou reamostrar áudio.</span><span class="sxs-lookup"><span data-stu-id="c2efd-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="c2efd-115">Em qualquer caso, você deve garantir que os formatos de entrada para os arquivos gravados correspondam aos dados enviados para o gravador.</span><span class="sxs-lookup"><span data-stu-id="c2efd-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="c2efd-116">Cada codec tem um formato de mídia de entrada padrão definido no gravador quando o perfil é carregado.</span><span class="sxs-lookup"><span data-stu-id="c2efd-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="c2efd-117">Você pode examinar o formato de entrada padrão chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="c2efd-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="c2efd-118">Os codecs de vídeo dão suporte aos seguintes formatos: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 e RGB 8.</span><span class="sxs-lookup"><span data-stu-id="c2efd-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="c2efd-119">Os codecs de áudio dão suporte a áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="c2efd-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="c2efd-120">Para enumerar os formatos de entrada com suporte por um codec, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="c2efd-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="c2efd-121">Crie um objeto do gravador e defina um perfil a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c2efd-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="c2efd-122">Para obter mais informações sobre como configurar perfis no gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="c2efd-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="c2efd-123">Identifique o número de entrada para o qual você deseja verificar os formatos.</span><span class="sxs-lookup"><span data-stu-id="c2efd-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="c2efd-124">Para obter mais informações sobre como identificar números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="c2efd-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="c2efd-125">Recupere o número total de formatos de entrada com suporte pela entrada desejada chamando [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span><span class="sxs-lookup"><span data-stu-id="c2efd-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="c2efd-126">Execute o loop por todos os formatos de entrada com suporte, executando as etapas a seguir para cada um.</span><span class="sxs-lookup"><span data-stu-id="c2efd-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="c2efd-127">Recupere a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para o formato de entrada chamando [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span><span class="sxs-lookup"><span data-stu-id="c2efd-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="c2efd-128">Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2efd-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="c2efd-129">Chame [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passando **NULL** para o parâmetro *pType* para obter o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="c2efd-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="c2efd-130">Em seguida, aloque memória para manter a estrutura e chamar **GetMediaType** novamente para obter a estrutura.</span><span class="sxs-lookup"><span data-stu-id="c2efd-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="c2efd-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) herda de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), para que você possa fazer as chamadas para **GetMediaType** da instância do **IWMInputMediaProps** recuperada na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="c2efd-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="c2efd-132">O formato descrito na estrutura [**do \_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contém todas as informações pertinentes sobre o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2efd-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="c2efd-133">O formato básico da mídia é identificado pela **mídia do \_ WM \_ tipo. subtipo**.</span><span class="sxs-lookup"><span data-stu-id="c2efd-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="c2efd-134">Para fluxos de vídeo, o membro **pbFormat** aponta para uma estrutura de [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) alocada dinamicamente que contém mais detalhes sobre o fluxo, incluindo o tamanho do retângulo.</span><span class="sxs-lookup"><span data-stu-id="c2efd-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="c2efd-135">O tamanho dos quadros de entrada não é necessário para corresponder exatamente a um tamanho suportado pelo codec.</span><span class="sxs-lookup"><span data-stu-id="c2efd-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="c2efd-136">Se eles não corresponderem, os componentes de tempo de execução do SDK, em muitos casos, redimensionarão automaticamente os quadros de vídeo de entrada para algo que o codec possa aceitar.</span><span class="sxs-lookup"><span data-stu-id="c2efd-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="c2efd-137">O código de exemplo a seguir localiza o formato de entrada do subtipo passado como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c2efd-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="c2efd-138">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c2efd-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
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

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c2efd-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2efd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2efd-140">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="c2efd-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="c2efd-141">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="c2efd-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




