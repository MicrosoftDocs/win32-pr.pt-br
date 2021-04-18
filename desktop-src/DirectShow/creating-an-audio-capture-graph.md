---
description: Criando um grafo de captura de áudio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Criando um grafo de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757023"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="70d27-103">Criando um grafo de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="70d27-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="70d27-104">A primeira etapa para um aplicativo de captura de áudio é criar um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="70d27-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="70d27-105">A configuração do grafo depende do tipo de arquivo que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="70d27-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="70d27-106">Arquivo AVI somente de áudio: filtro de captura de áudio para filtro [AVI Mux](avi-mux-filter.md) e AVI Mux para filtro de [gravador de arquivo](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="70d27-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="70d27-107">Arquivo WAV: filtro de captura de áudio para [exemplo de filtro WavDest](wavdest-filter-sample.md) para o filtro de gravador de arquivo</span><span class="sxs-lookup"><span data-stu-id="70d27-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="70d27-108">Arquivo de áudio do Windows Media (. WMA): filtro de captura de áudio para o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="70d27-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="70d27-109">O filtro WavDest é fornecido como um exemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="70d27-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="70d27-110">Para usá-lo, você deve criar e registrar o filtro.</span><span class="sxs-lookup"><span data-stu-id="70d27-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="70d27-111">Para usar o filtro do gravador ASF, você deve instalar o SDK do Windows Media e obter uma chave de software para desbloquear o filtro.</span><span class="sxs-lookup"><span data-stu-id="70d27-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="70d27-112">Para obter mais informações, consulte [usando o Windows Media no DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="70d27-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="70d27-113">Você pode criar o grafo de filtro usando o objeto do [construtor do grafo de captura](capture-graph-builder.md) ou pode criar o grafo "manualmente"; ou seja, faça com que o aplicativo adicione e conecte cada filtro programaticamente.</span><span class="sxs-lookup"><span data-stu-id="70d27-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="70d27-114">Este artigo descreve a abordagem manual.</span><span class="sxs-lookup"><span data-stu-id="70d27-114">This article describes the manual approach.</span></span> <span data-ttu-id="70d27-115">Para obter mais informações sobre como usar o construtor de gráficos de captura, consulte [captura de vídeo](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="70d27-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="70d27-116">Grande parte das informações nesse artigo aplica-se a gráficos somente de áudio.</span><span class="sxs-lookup"><span data-stu-id="70d27-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="70d27-117">Adicionando o dispositivo de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="70d27-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="70d27-118">Como o filtro de captura de áudio se comunica com um dispositivo de hardware específico, você não pode simplesmente chamar **CoCreateInstance** para criar o filtro.</span><span class="sxs-lookup"><span data-stu-id="70d27-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="70d27-119">Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar todos os dispositivos na categoria "fontes de captura de áudio", que é identificada pelo CLSID AudioInputDeviceCategory do identificador de classe \_ .</span><span class="sxs-lookup"><span data-stu-id="70d27-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="70d27-120">O enumerador de dispositivo do sistema retorna uma lista de monikers para os dispositivos; o nome amigável de cada moniker corresponde ao nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="70d27-121">Escolha um dos monikers retornados e use-o para criar uma instância do filtro de captura de áudio para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="70d27-122">Adicione o filtro ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="70d27-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="70d27-123">O dispositivo de gravação de áudio preferencial do usuário aparece primeiro na lista moniker.</span><span class="sxs-lookup"><span data-stu-id="70d27-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="70d27-124">(O usuário seleciona um dispositivo preferencial clicando em sons e multimídia no painel de controle.)</span><span class="sxs-lookup"><span data-stu-id="70d27-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="70d27-125">Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="70d27-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="70d27-126">Para especificar a entrada a ser capturada, obtenha a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) do filtro de captura de áudio e chame o método **Put \_ Enable** para especificar a entrada.</span><span class="sxs-lookup"><span data-stu-id="70d27-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="70d27-127">No entanto, uma limitação desse método é que diferentes dispositivos de hardware podem usar cadeias de caracteres diferentes para identificar suas entradas.</span><span class="sxs-lookup"><span data-stu-id="70d27-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="70d27-128">Por exemplo, um cartão pode usar "microfone" para identificar a entrada do microfone e outro cartão pode usar "MIC".</span><span class="sxs-lookup"><span data-stu-id="70d27-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="70d27-129">Para determinar o identificador de cadeia de caracteres de uma determinada entrada, use as funções de multimídia do Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70d27-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="70d27-130">Consulte o tópico do MSDN no [mixer consultas de dispositivo](/windows/desktop/Multimedia/mixer-device-queries) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="70d27-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="70d27-131">Adicionando o multiplexador e o gravador de arquivos</span><span class="sxs-lookup"><span data-stu-id="70d27-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="70d27-132">Um grafo de captura de áudio deve conter um multiplexador e um gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="70d27-133">Um *multiplexador* é um filtro que combina um ou mais fluxos em um único fluxo com um formato específico.</span><span class="sxs-lookup"><span data-stu-id="70d27-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="70d27-134">Por exemplo, o filtro AVI Mux combina fluxos de áudio e vídeo em um fluxo AVI intercalado.</span><span class="sxs-lookup"><span data-stu-id="70d27-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="70d27-135">Para captura de áudio, normalmente há apenas um único fluxo de áudio, mas os dados de áudio ainda devem ser empacotados em um formato que possa ser salvo em disco, o que requer um multiplexador.</span><span class="sxs-lookup"><span data-stu-id="70d27-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="70d27-136">A escolha do Multiplexador depende do formato de destino:</span><span class="sxs-lookup"><span data-stu-id="70d27-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="70d27-137">AVI: multiplexador AVI</span><span class="sxs-lookup"><span data-stu-id="70d27-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="70d27-138">WAV: WavDest</span><span class="sxs-lookup"><span data-stu-id="70d27-138">WAV: WavDest</span></span>
-   <span data-ttu-id="70d27-139">WMA: gravador ASF</span><span class="sxs-lookup"><span data-stu-id="70d27-139">WMA: ASF Writer</span></span>

<span data-ttu-id="70d27-140">Um *gravador de arquivo* é um filtro que grava dados de entrada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="70d27-141">Para arquivos AVI ou WAV, use o [filtro gravador de arquivo](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="70d27-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="70d27-142">Para arquivos WMA, o gravador ASF atua como Multiplexador e gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="70d27-143">Depois de criar os filtros e adicioná-los ao grafo, conecte o pino de saída do filtro de captura de áudio ao pino de entrada do Multiplexador e conecte o pino de saída do Multiplexador ao pino de entrada do gravador de filtro (supondo que eles sejam filtros separados).</span><span class="sxs-lookup"><span data-stu-id="70d27-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="70d27-144">Para especificar o nome do arquivo, consulte o gravador de arquivo para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chame o método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .</span><span class="sxs-lookup"><span data-stu-id="70d27-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="70d27-145">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="70d27-145">Example Code</span></span>

<span data-ttu-id="70d27-146">O exemplo a seguir mostra como criar um grafo de captura de áudio usando o filtro WavDest.</span><span class="sxs-lookup"><span data-stu-id="70d27-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="70d27-147">Os mesmos princípios se aplicam a outros tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="70d27-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="70d27-148">Este exemplo usa a `AddFilterByCLSID` função descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md)e a `ConnectFilters` função descrita em [conectar dois filtros](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="70d27-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="70d27-149">Nenhuma delas é uma API do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="70d27-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70d27-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70d27-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70d27-151">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="70d27-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
