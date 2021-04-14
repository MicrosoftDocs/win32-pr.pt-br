---
description: Capturando vídeo em um arquivo AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capturando vídeo em um arquivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564816"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="671d8-103">Capturando vídeo em um arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="671d8-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="671d8-104">A ilustração a seguir mostra o grafo mais simples possível para capturar vídeo em um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="671d8-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![Grafo de captura de vídeo AVI](images/vidcap02.png)

<span data-ttu-id="671d8-106">O filtro [AVI Mux](avi-mux-filter.md) pega o fluxo de vídeo do PIN de captura e o empacota em um fluxo avi.</span><span class="sxs-lookup"><span data-stu-id="671d8-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="671d8-107">Um fluxo de áudio também pode ser conectado ao filtro AVI Mux. nesse caso, o MUX intercalaria os dois fluxos.</span><span class="sxs-lookup"><span data-stu-id="671d8-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="671d8-108">O filtro [gravador de arquivo](file-writer-filter.md) grava o fluxo AVI em disco.</span><span class="sxs-lookup"><span data-stu-id="671d8-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="671d8-109">Para criar o grafo, comece chamando o método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="671d8-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="671d8-110">O primeiro parâmetro especifica o tipo de arquivo — nesse caso, AVI.</span><span class="sxs-lookup"><span data-stu-id="671d8-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="671d8-111">O segundo parâmetro fornece o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="671d8-111">The second parameter gives the file name.</span></span> <span data-ttu-id="671d8-112">Para AVI, o método SetOutputFileName cocria o filtro AVI Mux e o filtro do gravador de arquivo e os adiciona ao grafo.</span><span class="sxs-lookup"><span data-stu-id="671d8-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="671d8-113">Ele também define o nome do arquivo no filtro de gravador de arquivo, chamando o método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) e conecta os dois filtros.</span><span class="sxs-lookup"><span data-stu-id="671d8-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="671d8-114">O método retorna um ponteiro para o multiplexado AVI no terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="671d8-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="671d8-115">Opcionalmente, ele retorna um ponteiro para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) no quarto parâmetro.</span><span class="sxs-lookup"><span data-stu-id="671d8-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="671d8-116">Se você não precisar dessa interface, poderá definir esse parâmetro como **NULL**, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="671d8-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="671d8-117">Em seguida, chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura ao AVI Mux, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="671d8-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="671d8-118">O primeiro parâmetro fornece a categoria de PIN, que é fixar a \_ \_ captura de categoria para captura.</span><span class="sxs-lookup"><span data-stu-id="671d8-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="671d8-119">O segundo parâmetro fornece o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="671d8-119">The second parameter gives the media type.</span></span> <span data-ttu-id="671d8-120">O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="671d8-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="671d8-121">O quarto parâmetro é opcional; Ele permite rotear o fluxo de vídeo por meio de um filtro intermediário, como um codificador, antes de passá-lo para o filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="671d8-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="671d8-122">Caso contrário, defina esse parâmetro como **NULL**, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="671d8-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="671d8-123">O quinto parâmetro é o ponteiro para o filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="671d8-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="671d8-124">Esse ponteiro é obtido chamando o método SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="671d8-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="671d8-125">Para capturar áudio, chame RenderStream com o tipo de mídia \_ áudio de MediaType.</span><span class="sxs-lookup"><span data-stu-id="671d8-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="671d8-126">Se você estiver capturando áudio e vídeo de dois dispositivos separados, é uma boa ideia fazer com que o fluxo de áudio seja o fluxo mestre.</span><span class="sxs-lookup"><span data-stu-id="671d8-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="671d8-127">Isso ajuda a evitar descompasso entre os dois fluxos, pois o filtro AVI Mux ajusta a taxa de reprodução no fluxo de vídeo para corresponder ao fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="671d8-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="671d8-128">Para definir o fluxo mestre, chame o método [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) no filtro AVI Mux:</span><span class="sxs-lookup"><span data-stu-id="671d8-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="671d8-129">O parâmetro para SetMasterStream é o número de fluxo, que é determinado pela ordem em que você chama RenderStream.</span><span class="sxs-lookup"><span data-stu-id="671d8-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="671d8-130">Por exemplo, se você chamar RenderStream primeiro para vídeo e, em seguida, para áudio, o vídeo será o fluxo 0 e o áudio será o fluxo 1.</span><span class="sxs-lookup"><span data-stu-id="671d8-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="671d8-131">Talvez você também queira definir como o filtro AVI Mux intercala os fluxos de áudio e vídeo, chamando o método [**IConfigInterleaving::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="671d8-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="671d8-132">Com o sinalizador de captura de intercalação \_ , o AVI Mux executa intercalação a uma taxa adequada para captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="671d8-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="671d8-133">Você também pode usar intercalar \_ None, o que significa que não há intercalação – o AVI Mux simplesmente gravará os dados na ordem em que chegam.</span><span class="sxs-lookup"><span data-stu-id="671d8-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="671d8-134">O sinalizador completo de intercalação \_ significa que o AVI Mux executa a intercalação completa; no entanto, esse modo é menos adequado para a captura de vídeo porque ele requer o mais ouvido.</span><span class="sxs-lookup"><span data-stu-id="671d8-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="671d8-135">Codificando o fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="671d8-135">Encoding the Video Stream</span></span>

<span data-ttu-id="671d8-136">Você pode codificar o fluxo de vídeo inserindo um filtro de codificador entre o filtro de captura e o filtro AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="671d8-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="671d8-137">Use o [enumerador de dispositivo do sistema](system-device-enumerator.md) ou o [mapeador de filtro](filter-mapper.md) para selecionar um filtro de codificador.</span><span class="sxs-lookup"><span data-stu-id="671d8-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="671d8-138">(Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="671d8-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="671d8-139">Especifique o filtro do codificador como o quarto parâmetro para RenderStream, mostrado em negrito no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="671d8-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="671d8-140">O filtro do codificador pode dar suporte a [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ou outras interfaces para definir os parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="671d8-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="671d8-141">Para obter uma lista de interfaces possíveis, consulte [codificação de arquivos e decodificação de interfaces](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="671d8-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="671d8-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="671d8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="671d8-143">Capturando vídeo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="671d8-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



