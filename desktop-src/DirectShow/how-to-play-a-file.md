---
description: Como reproduzir um arquivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Como reproduzir um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370299"
---
# <a name="how-to-play-a-file"></a><span data-ttu-id="d5172-103">Como reproduzir um arquivo</span><span class="sxs-lookup"><span data-stu-id="d5172-103">How To Play a File</span></span>

<span data-ttu-id="d5172-104">Este artigo destina-se a dar o tipo de programação do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d5172-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="d5172-105">Ele apresenta um aplicativo de console simples que reproduz um arquivo de áudio ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5172-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="d5172-106">O programa tem apenas algumas linhas, mas demonstra algumas das eficiências da programação do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d5172-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="d5172-107">Como descreve o artigo [introdução à programação de aplicativo do DirectShow](introduction-to-directshow-application-programming.md) , um aplicativo do DirectShow sempre executa as mesmas etapas básicas:</span><span class="sxs-lookup"><span data-stu-id="d5172-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="d5172-108">Crie uma instância do [Gerenciador de gráfico de filtro](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d5172-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="d5172-109">Use o Gerenciador de gráfico de filtro para criar um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d5172-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="d5172-110">Execute o grafo, fazendo com que os dados passem pelos filtros.</span><span class="sxs-lookup"><span data-stu-id="d5172-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="d5172-111">Para compilar e vincular o código neste tópico, inclua o arquivo de cabeçalho DShow. h e vincule ao arquivo de biblioteca estática strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="d5172-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="d5172-112">Para obter mais informações, consulte [criando aplicativos do DirectShow](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d5172-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="d5172-113">Comece chamando [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com:</span><span class="sxs-lookup"><span data-stu-id="d5172-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="d5172-114">Para simplificar as coisas, este exemplo ignora o valor de retorno, mas você sempre deve verificar o valor **HRESULT** de qualquer chamada de método.</span><span class="sxs-lookup"><span data-stu-id="d5172-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="d5172-115">Em seguida, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o Gerenciador de gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="d5172-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="d5172-116">Como mostrado, o identificador de classe (CLSID) é CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="d5172-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="d5172-117">O Gerenciador de gráfico de filtro é fornecido por uma DLL em processo, portanto, o contexto de execução é o **\_ \_ servidor CLSCTX InProc**.</span><span class="sxs-lookup"><span data-stu-id="d5172-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="d5172-118">O DirectShow dá suporte ao modelo de Threading livre, de modo que você também pode chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador de **\_ vários threads de coinit** .</span><span class="sxs-lookup"><span data-stu-id="d5172-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="d5172-119">A chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retorna a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , que basicamente contém métodos para criar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d5172-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="d5172-120">Duas outras interfaces são necessárias para este exemplo:</span><span class="sxs-lookup"><span data-stu-id="d5172-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="d5172-121">Streaming de controles [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="d5172-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="d5172-122">Ele contém métodos para parar e iniciar o grafo.</span><span class="sxs-lookup"><span data-stu-id="d5172-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="d5172-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) tem métodos para obter eventos do Gerenciador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="d5172-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="d5172-124">Neste exemplo, a interface é usada para aguardar a conclusão da reprodução.</span><span class="sxs-lookup"><span data-stu-id="d5172-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="d5172-125">Ambas as interfaces são expostas pelo Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d5172-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="d5172-126">Use o ponteiro [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) retornado para consultá-los:</span><span class="sxs-lookup"><span data-stu-id="d5172-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="d5172-127">Agora você pode criar o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d5172-127">Now you can build the filter graph.</span></span> <span data-ttu-id="d5172-128">Para a reprodução de arquivos, isso é feito por uma única chamada de método:</span><span class="sxs-lookup"><span data-stu-id="d5172-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="d5172-129">O método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um gráfico de filtro que pode reproduzir o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5172-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="d5172-130">O primeiro parâmetro é o nome do arquivo, representado como uma cadeia de caracteres de caractere largo (2 bytes).</span><span class="sxs-lookup"><span data-stu-id="d5172-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="d5172-131">O segundo parâmetro é reservado e deve ser igual a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5172-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="d5172-132">Esse método pode falhar se o arquivo especificado não existir ou o formato de arquivo não for reconhecido.</span><span class="sxs-lookup"><span data-stu-id="d5172-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="d5172-133">Supondo que o método tenha sucesso, no entanto, o gráfico de filtro agora está pronto para reprodução.</span><span class="sxs-lookup"><span data-stu-id="d5172-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="d5172-134">Para executar o grafo, chame o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :</span><span class="sxs-lookup"><span data-stu-id="d5172-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="d5172-135">Quando o grafo de filtro é executado, os dados passam pelos filtros e são renderizados como vídeo e áudio.</span><span class="sxs-lookup"><span data-stu-id="d5172-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="d5172-136">A reprodução ocorre em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="d5172-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="d5172-137">Você pode aguardar a reprodução ser concluída chamando o método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :</span><span class="sxs-lookup"><span data-stu-id="d5172-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="d5172-138">Esse método é bloqueado até que o arquivo seja executado ou até que o intervalo de tempo limite especificado decorra.</span><span class="sxs-lookup"><span data-stu-id="d5172-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="d5172-139">O valor infinito significa que o aplicativo é bloqueado indefinidamente até que o arquivo seja executado.</span><span class="sxs-lookup"><span data-stu-id="d5172-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="d5172-140">Para obter um exemplo mais realista de manipulação de eventos, consulte [respondendo a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="d5172-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="d5172-141">Quando o aplicativo for concluído, libere os ponteiros de interface e feche a biblioteca COM:</span><span class="sxs-lookup"><span data-stu-id="d5172-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="d5172-142">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d5172-142">Example Code</span></span>

<span data-ttu-id="d5172-143">Este é o código completo do exemplo descrito neste artigo:</span><span class="sxs-lookup"><span data-stu-id="d5172-143">Here is the complete code for the example described in this article:</span></span>


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="d5172-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5172-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5172-145">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5172-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
