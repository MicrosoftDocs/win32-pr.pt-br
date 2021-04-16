---
description: O filtro de apoio de exemplo é um filtro de transformação que pode ser usado para obter amostras de mídia de um fluxo à medida que eles passam pelo gráfico de filtro.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Usando o exemplo de apoio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758505"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="92dba-103">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="92dba-103">Using the Sample Grabber</span></span>

<span data-ttu-id="92dba-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="92dba-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="92dba-105">O filtro de [**apoio de exemplo**](sample-grabber-filter.md) é um filtro de transformação que pode ser usado para obter amostras de mídia de um fluxo à medida que eles passam pelo gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="92dba-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="92dba-106">Se você simplesmente deseja pegar um bitmap de um arquivo de vídeo, é mais fácil usar o objeto [detector de mídia (MediaDet)](media-detector--mediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="92dba-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="92dba-107">Consulte [captando um quadro de cartaz](grabbing-a-poster-frame.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="92dba-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="92dba-108">No entanto, o exemplo de apoio é mais flexível porque funciona com quase qualquer tipo de mídia (consulte [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) para as poucas exceções) e oferece mais controle ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92dba-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="92dba-109">Criar o Gerenciador de gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="92dba-110">Adicionar o exemplo de apoio ao grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="92dba-111">Definir o tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="92dba-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="92dba-112">Criar o grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="92dba-113">Executar o grafo</span><span class="sxs-lookup"><span data-stu-id="92dba-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="92dba-114">Obter o exemplo</span><span class="sxs-lookup"><span data-stu-id="92dba-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="92dba-115">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="92dba-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="92dba-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92dba-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="92dba-117">Criar o Gerenciador de gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="92dba-118">Para começar, crie o [Gerenciador do grafo de filtro](filter-graph-manager.md) e consulte as interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="92dba-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="92dba-119">Adicionar o exemplo de apoio ao grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="92dba-120">Crie uma instância do filtro de apoio de exemplo e addit para o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="92dba-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="92dba-121">Consulte o filtro de apoio de exemplo para a interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="92dba-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="92dba-122">Definir o tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="92dba-122">Set the Media Type</span></span>

<span data-ttu-id="92dba-123">Quando você cria o exemplo de apoio pela primeira vez, ele não tem nenhum tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="92dba-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="92dba-124">Isso significa que você pode se conectar a praticamente qualquer filtro no grafo, mas não teria nenhum controle sobre o tipo de dados que ele recebeu.</span><span class="sxs-lookup"><span data-stu-id="92dba-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="92dba-125">Antes de compilar o restante do grafo, portanto, você deve definir um tipo de mídia para o exemplo de apoio, chamando o método [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="92dba-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="92dba-126">Quando o elemento de exemplo se conecta, ele compara esse tipo de mídia com o tipo de mídia oferecido pelo outro filtro.</span><span class="sxs-lookup"><span data-stu-id="92dba-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="92dba-127">Os únicos campos que ele verifica são o tipo principal, subtipo e tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="92dba-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="92dba-128">Para qualquer um deles, o valor GUID \_ null significa "aceitar qualquer valor".</span><span class="sxs-lookup"><span data-stu-id="92dba-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="92dba-129">Na maioria das vezes, você desejará definir o tipo e subtipo principais.</span><span class="sxs-lookup"><span data-stu-id="92dba-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="92dba-130">Por exemplo, o código a seguir especifica um vídeo RGB não compactado de 24 bits:</span><span class="sxs-lookup"><span data-stu-id="92dba-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="92dba-131">Criar o grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="92dba-131">Build the Filter Graph</span></span>

<span data-ttu-id="92dba-132">Agora você pode criar o restante do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="92dba-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="92dba-133">Como o exemplo de apoio se conectará apenas usando o tipo de mídia que você especificou, isso permite que você aproveite os mecanismos de [conexão inteligente](intelligent-connect.md) do Gerenciador de grafo de filtro ao criar o grafo.</span><span class="sxs-lookup"><span data-stu-id="92dba-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="92dba-134">Por exemplo, se você tiver especificado vídeo descompactado, poderá conectar um filtro de origem ao complemento de exemplo e o Gerenciador de gráfico de filtro adicionará automaticamente o analisador de arquivo e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="92dba-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="92dba-135">O exemplo a seguir usa a função auxiliar ConnectFilters, que está listada em [conectar dois filtros](connect-two-filters.md):</span><span class="sxs-lookup"><span data-stu-id="92dba-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="92dba-136">O exemplo de apoio é um filtro de transformação, portanto, o pino de saída deve estar conectado a outro filtro.</span><span class="sxs-lookup"><span data-stu-id="92dba-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="92dba-137">Muitas vezes, talvez você queira simplesmente descartar os exemplos depois de concluí-los.</span><span class="sxs-lookup"><span data-stu-id="92dba-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="92dba-138">Nesse caso, conecte o exemplo de apoio ao [**filtro de renderizador nulo**](null-renderer-filter.md), que descarta os dados que recebe.</span><span class="sxs-lookup"><span data-stu-id="92dba-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="92dba-139">O exemplo a seguir conecta o exemplo de apoio ao filtro de renderizador nulo:</span><span class="sxs-lookup"><span data-stu-id="92dba-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="92dba-140">Lembre-se de que colocar o exemplo de apoio entre um decodificador de vídeo e o renderizador de vídeo pode prejudicar significativamente o desempenho da renderização.</span><span class="sxs-lookup"><span data-stu-id="92dba-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="92dba-141">O exemplo de amostra é um filtro de trans-in-Place, o que significa que o buffer de saída é o mesmo que o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="92dba-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="92dba-142">Para a renderização de vídeo, é provável que o buffer de saída esteja localizado na placa gráfica, em que as operações de leitura são muito mais lentas, comparadas com as operações de leitura na memória principal.</span><span class="sxs-lookup"><span data-stu-id="92dba-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="92dba-143">Executar o grafo</span><span class="sxs-lookup"><span data-stu-id="92dba-143">Run the Graph</span></span>

<span data-ttu-id="92dba-144">O exemplo de apoio Opera em um dos dois modos:</span><span class="sxs-lookup"><span data-stu-id="92dba-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="92dba-145">O modo de buffer faz uma cópia de cada amostra antes de entregar o downstream de exemplo.</span><span class="sxs-lookup"><span data-stu-id="92dba-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="92dba-146">O modo de retorno de chamada invoca uma função de retorno de chamada definida pelo aplicativo em cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="92dba-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="92dba-147">Este artigo descreve o modo de buffer.</span><span class="sxs-lookup"><span data-stu-id="92dba-147">This article describes buffering mode.</span></span> <span data-ttu-id="92dba-148">(Antes de usar o modo de retorno de chamada, lembre-se de que a função de retorno de chamada deve ser bastante limitada.</span><span class="sxs-lookup"><span data-stu-id="92dba-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="92dba-149">Caso contrário, ele pode reduzir drasticamente o desempenho ou até mesmo causar deadlocks.</span><span class="sxs-lookup"><span data-stu-id="92dba-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="92dba-150">Para obter mais informações, consulte [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).) Para ativar o modo de buffer, chame o método [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="92dba-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="92dba-151">Opcionalmente, chame o método [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="92dba-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="92dba-152">Isso faz com que o exemplo de apoio Pare depois de receber o primeiro exemplo de mídia, o que é útil se você quiser pegar um único quadro a partir do fluxo.</span><span class="sxs-lookup"><span data-stu-id="92dba-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="92dba-153">Procure o tempo desejado, execute o grafo e aguarde o evento de [**\_ conclusão do EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="92dba-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="92dba-154">Observe que o nível de precisão do quadro depende da origem.</span><span class="sxs-lookup"><span data-stu-id="92dba-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="92dba-155">Por exemplo, procurar um arquivo MPEG geralmente não é preciso de quadros.</span><span class="sxs-lookup"><span data-stu-id="92dba-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="92dba-156">Para executar o grafo o mais rápido possível, ative o relógio do grafo, conforme descrito em [definindo o relógio do grafo](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="92dba-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="92dba-157">O exemplo a seguir habilita o modo único e o modo de buffer, executa o gráfico de filtro e aguarda a conclusão.</span><span class="sxs-lookup"><span data-stu-id="92dba-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="92dba-158">Obter o exemplo</span><span class="sxs-lookup"><span data-stu-id="92dba-158">Grab the Sample</span></span>

<span data-ttu-id="92dba-159">No modo de buffer, o exemplo de apoio armazena uma cópia de cada amostra.</span><span class="sxs-lookup"><span data-stu-id="92dba-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="92dba-160">O método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia o buffer em uma matriz alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="92dba-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="92dba-161">Para determinar o tamanho da matriz que é necessária, primeiro chame **GetCurrentBuffer** com um ponteiro **nulo** para o endereço da matriz.</span><span class="sxs-lookup"><span data-stu-id="92dba-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="92dba-162">Em seguida, aloque a matriz e chame o método uma segunda vez para copiar o buffer.</span><span class="sxs-lookup"><span data-stu-id="92dba-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="92dba-163">O exemplo a seguir mostra estas etapas.</span><span class="sxs-lookup"><span data-stu-id="92dba-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="92dba-164">Você precisará saber o formato exato dos dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="92dba-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="92dba-165">Para obter essas informações, chame o método [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="92dba-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="92dba-166">Esse método preenche uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) com o formato.</span><span class="sxs-lookup"><span data-stu-id="92dba-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="92dba-167">Para um fluxo de vídeo descompactado, as informações de formato estão contidas em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="92dba-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="92dba-168">O exemplo a seguir mostra como obter as informações de formato de um fluxo de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="92dba-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="92dba-169">O exemplo de apoio não oferece suporte a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="92dba-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="92dba-170">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="92dba-170">Example Code</span></span>

<span data-ttu-id="92dba-171">Aqui está o código completo para os exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="92dba-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="92dba-172">Este exemplo usa a função [SafeRelease](../medfound/saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="92dba-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="92dba-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92dba-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92dba-174">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="92dba-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
