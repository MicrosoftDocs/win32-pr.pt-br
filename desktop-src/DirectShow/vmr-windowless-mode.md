---
description: Modo sem janela do VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modo sem janela do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296523"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="4add8-103">Modo sem janela do VMR</span><span class="sxs-lookup"><span data-stu-id="4add8-103">VMR Windowless Mode</span></span>

<span data-ttu-id="4add8-104">O modo sem janela é a maneira preferida para os aplicativos renderizarem o vídeo dentro de uma janela de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4add8-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="4add8-105">No modo sem janela, o processador de mixagem de vídeo não carrega o componente do Gerenciador de janelas e, portanto, não oferece suporte às interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) ou [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="4add8-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="4add8-106">Em vez disso, o aplicativo fornece a janela de reprodução e define um retângulo de destino na área do cliente para o VMR desenhar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="4add8-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="4add8-107">O VMR usa um objeto Clipper do DirectDraw para garantir que o vídeo seja recortado na janela do aplicativo e não apareça em outras janelas.</span><span class="sxs-lookup"><span data-stu-id="4add8-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="4add8-108">O VMR não faz a subclasse da janela do aplicativo nem instala quaisquer ganchos de sistema/processo.</span><span class="sxs-lookup"><span data-stu-id="4add8-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="4add8-109">No modo sem janela, a sequência de eventos durante a conexão e a transição para o estado de execução é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="4add8-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="4add8-110">O filtro upstream propõe um tipo de mídia, que o VMR aceita ou rejeita.</span><span class="sxs-lookup"><span data-stu-id="4add8-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="4add8-111">Se o tipo de mídia for aceito, o VMR chamará o alocador-Presenter para obter uma superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4add8-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="4add8-112">Se a superfície for criada com êxito, os PINs se conectarão e o VMR estará pronto para fazer a transição para o estado de execução.</span><span class="sxs-lookup"><span data-stu-id="4add8-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="4add8-113">Quando o grafo de filtro é executado, o decodificador chama **GetBuffer** para obter um exemplo de mídia do alocador.</span><span class="sxs-lookup"><span data-stu-id="4add8-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="4add8-114">O VMR consulta o alocador-apresentador para garantir que a profundidade de pixels, o tamanho do retângulo e outros parâmetros em sua superfície do DirectDraw sejam compatíveis com o vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4add8-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="4add8-115">Se forem compatíveis, o VMR retornará a superfície do DirectDraw para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="4add8-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="4add8-116">Depois que o decodificador for decodificado na superfície, a unidade de sincronização principal do VMR validará os carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="4add8-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="4add8-117">Essa unidade bloqueia a chamada de **recebimento** até que o tempo de apresentação chegue.</span><span class="sxs-lookup"><span data-stu-id="4add8-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="4add8-118">Nesse ponto, o VMR chama **PresentImage** no apresentador de alocador, que apresenta a superfície para a placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="4add8-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="4add8-119">A ilustração a seguir mostra o VMR no modo sem janela com vários fluxos de entrada.</span><span class="sxs-lookup"><span data-stu-id="4add8-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR no modo sem janela](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="4add8-121">**Configurando o VMR-7 para o modo sem janela**</span><span class="sxs-lookup"><span data-stu-id="4add8-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="4add8-122">Para configurar o VMR-7 para o modo sem janela, execute todas as etapas a seguir antes de conectar qualquer um dos Pins de entrada do VMR:</span><span class="sxs-lookup"><span data-stu-id="4add8-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="4add8-123">Crie o filtro e adicione-o ao grafo.</span><span class="sxs-lookup"><span data-stu-id="4add8-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="4add8-124">Chame o método [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) com o \_ sinalizador VMRMode sem janela.</span><span class="sxs-lookup"><span data-stu-id="4add8-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="4add8-125">Opcionalmente, configure o VMR para vários fluxos de entrada chamando [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="4add8-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="4add8-126">O VMR cria um PIN de entrada para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="4add8-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="4add8-127">Use a interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para definir a ordem Z e outros parâmetros para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="4add8-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="4add8-128">Para obter mais informações, consulte [VMR com vários fluxos (modo de combinação)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="4add8-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="4add8-129">Se você não chamar **SetNumberOfStreams**, o VMR-7 usa como padrão um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="4add8-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="4add8-130">Depois que os Pins de entrada estiverem conectados, o número de Pins não poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="4add8-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="4add8-131">Chame [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar a janela na qual o vídeo renderizado será exibido.</span><span class="sxs-lookup"><span data-stu-id="4add8-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="4add8-132">Depois que essas etapas forem concluídas, você poderá conectar os Pins de entrada do filtro do VMR.</span><span class="sxs-lookup"><span data-stu-id="4add8-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="4add8-133">Há várias maneiras de criar o grafo, como conectar Pins diretamente, usando métodos de conexão inteligente, como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ou usando o método [**ICaptureGraphBuilder2:: MessageRenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do construtor de grafo de captura.</span><span class="sxs-lookup"><span data-stu-id="4add8-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="4add8-134">Para obter mais informações, consulte [General Graph-Building Techniques](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="4add8-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="4add8-135">Para definir a posição do vídeo dentro da janela do aplicativo, chame o método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="4add8-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="4add8-136">O método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) retorna o tamanho do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="4add8-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="4add8-137">Durante a reprodução, o aplicativo deve notificar o VMR das seguintes mensagens do Windows:</span><span class="sxs-lookup"><span data-stu-id="4add8-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="4add8-138">WM \_ Paint: chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para redesenhar a imagem.</span><span class="sxs-lookup"><span data-stu-id="4add8-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="4add8-139">WM \_ DISPLAYCHANGE: chamar [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="4add8-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="4add8-140">O VMR usa todas as ações necessárias para exibir o vídeo na nova resolução ou profundidade de cor.</span><span class="sxs-lookup"><span data-stu-id="4add8-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="4add8-141">\_Tamanho do WM: recalcule a posição do vídeo e chame [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) novamente, se necessário.</span><span class="sxs-lookup"><span data-stu-id="4add8-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="4add8-142">Os aplicativos MFC devem definir um \_ manipulador de mensagens ERASEBKGND do WM vazio ou a área de exibição do vídeo não será redesenhada corretamente.</span><span class="sxs-lookup"><span data-stu-id="4add8-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="4add8-143">**Configurando o VMR-9 para o modo sem janela**</span><span class="sxs-lookup"><span data-stu-id="4add8-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="4add8-144">Para configurar o VMR-9 para o modo sem janela, use as etapas descritas para o VMR-7 para o modo sem janela, mas use as interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="4add8-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="4add8-145">A única diferença significativa é que o VMR-9 cria quatro Pins de entrada por padrão, em vez de um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="4add8-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="4add8-146">Portanto, você só precisa chamar **SetNumberOfStreams** se estiver misturando mais de quatro fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4add8-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="4add8-147">**Código de exemplo**</span><span class="sxs-lookup"><span data-stu-id="4add8-147">**Example Code**</span></span>

<span data-ttu-id="4add8-148">O código a seguir mostra como criar um filtro do VMR-7, adicioná-lo ao grafo de filtro do DirectShow e, em seguida, colocar o VMR no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="4add8-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="4add8-149">Para o VMR-9, use CLSID \_ VideoMixingRenderer9 em **CoCreateInstance** e as interfaces do VMR-9 correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4add8-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4add8-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4add8-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4add8-151">Usando o modo sem janela</span><span class="sxs-lookup"><span data-stu-id="4add8-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



