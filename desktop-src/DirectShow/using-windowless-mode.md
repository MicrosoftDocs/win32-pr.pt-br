---
description: Usando o modo sem janela
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Usando o modo sem janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829054"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="5385d-103">Usando o modo sem janela</span><span class="sxs-lookup"><span data-stu-id="5385d-103">Using Windowless Mode</span></span>

<span data-ttu-id="5385d-104">O [filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) e o filtro de processador de mixagem de [vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) dão suporte ao *modo sem janela*, que representa uma grande melhoria na interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="5385d-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="5385d-105">Este tópico descreve as diferenças entre o modo sem janela e o modo de janela e como usar o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="5385d-106">Para manter a compatibilidade com versões anteriores com os aplicativos existentes, o VMR usa como padrão o modo de janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="5385d-107">No modo de janela, o renderizador cria sua própria janela para exibir o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="5385d-108">Normalmente, o aplicativo define a janela de vídeo como um filho da janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5385d-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="5385d-109">No entanto, a existência de uma janela de vídeo separada causa alguns problemas:</span><span class="sxs-lookup"><span data-stu-id="5385d-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="5385d-110">O mais importante é que haja um potencial para deadlocks se as mensagens de janela forem enviadas entre threads.</span><span class="sxs-lookup"><span data-stu-id="5385d-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="5385d-111">O Gerenciador do grafo de filtro deve encaminhar certas mensagens da janela, como \_ o WM Paint, ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="5385d-112">O aplicativo deve usar a implementação do Gerenciador de grafo de filtro do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (e não do processador de vídeo), para que o Gerenciador do grafo de filtro Mantenha o estado interno correto.</span><span class="sxs-lookup"><span data-stu-id="5385d-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="5385d-113">Para receber eventos de mouse ou de teclado da janela de vídeo, o aplicativo deve definir uma *drenagem de mensagem*, fazendo com que a janela de vídeo encaminhe essas mensagens para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5385d-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="5385d-114">Para evitar problemas de recorte, a janela de vídeo deve ter os estilos de janela corretos.</span><span class="sxs-lookup"><span data-stu-id="5385d-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="5385d-115">O modo sem janela evita esses problemas fazendo com que o VMR desenhe diretamente na área do cliente da janela do aplicativo, usando o DirectDraw para recortar o retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="5385d-116">O modo sem janela reduz significativamente a chance de deadlocks.</span><span class="sxs-lookup"><span data-stu-id="5385d-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="5385d-117">Além disso, o aplicativo não precisa definir a janela do proprietário nem os estilos da janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="5385d-118">Na verdade, quando o VMR está no modo sem janela, ele nem mesmo expõe a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , que não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="5385d-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="5385d-119">Para usar o modo sem janela, você deve configurar explicitamente o VMR.</span><span class="sxs-lookup"><span data-stu-id="5385d-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="5385d-120">No entanto, você verá que é mais flexível e mais fácil de usar do que o modo em janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="5385d-121">O filtro VMR-7 e o filtro VMR-9 expõem interfaces diferentes, mas as etapas são equivalentes para cada uma.</span><span class="sxs-lookup"><span data-stu-id="5385d-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="5385d-122">Configurar o VMR para o modo sem janela</span><span class="sxs-lookup"><span data-stu-id="5385d-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="5385d-123">Para substituir o comportamento padrão do VMR, configure o VMR antes de criar o grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="5385d-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="5385d-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5385d-124">**VMR-7**</span></span>

1.  <span data-ttu-id="5385d-125">Crie o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5385d-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="5385d-126">Crie o VMR-7 e adicione-o ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5385d-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="5385d-127">Chame [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) no VMR-7 com o sinalizador **VMRMode \_ sem janela** .</span><span class="sxs-lookup"><span data-stu-id="5385d-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="5385d-128">Consulte o VMR-7 para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="5385d-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="5385d-129">Chame [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) no VMR-7.</span><span class="sxs-lookup"><span data-stu-id="5385d-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="5385d-130">Especifique um identificador para a janela em que o vídeo deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="5385d-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="5385d-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5385d-131">**VMR-9**</span></span>

1.  <span data-ttu-id="5385d-132">Crie o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5385d-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="5385d-133">Crie o VMR-9 e adicione-o ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5385d-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="5385d-134">Chame [**IVMRFilterConfig9:: Setrenderizamode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) no VMR-9 com o sinalizador **VMR9Mode \_ sem janela** .</span><span class="sxs-lookup"><span data-stu-id="5385d-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="5385d-135">Consulte o VMR-9 para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="5385d-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="5385d-136">Chame [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) no VMR-9.</span><span class="sxs-lookup"><span data-stu-id="5385d-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="5385d-137">Especifique um identificador para a janela em que o vídeo deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="5385d-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="5385d-138">Agora, compile o restante do grafo de filtro chamando [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou outros métodos de criação de grafo.</span><span class="sxs-lookup"><span data-stu-id="5385d-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="5385d-139">O Gerenciador de gráfico de filtro usa automaticamente a instância do VMR que você adicionou ao grafo.</span><span class="sxs-lookup"><span data-stu-id="5385d-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="5385d-140">(Para obter detalhes sobre por que isso acontece, consulte [conexão inteligente](intelligent-connect.md).)</span><span class="sxs-lookup"><span data-stu-id="5385d-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="5385d-141">O código a seguir mostra uma função auxiliar que cria o VMR-7, adiciona-o ao grafo e define o modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="5385d-142">Essa função pressupõe que está exibindo apenas um fluxo de vídeo e não está misturando um bitmap estático no vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="5385d-143">Para obter detalhes, consulte [modo sem janela do VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="5385d-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="5385d-144">Você chamaria essa função da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5385d-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="5385d-145">Posicionar o vídeo</span><span class="sxs-lookup"><span data-stu-id="5385d-145">Position the Video</span></span>

<span data-ttu-id="5385d-146">Depois de configurar o VMR, a próxima etapa é definir a posição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="5385d-147">Há dois retângulos a serem considerados, o retângulo de *origem* e o retângulo de *destino* .</span><span class="sxs-lookup"><span data-stu-id="5385d-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="5385d-148">O retângulo de origem define a parte do vídeo a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="5385d-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="5385d-149">O retângulo de destino especifica a região na área do cliente da janela que conterá o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="5385d-150">O VMR corta a imagem de vídeo para o retângulo de origem e amplia a imagem cortada para se ajustar ao retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="5385d-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="5385d-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5385d-151">**VMR-7**</span></span>

1.  <span data-ttu-id="5385d-152">Chame o método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para especificar os dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="5385d-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="5385d-153">O retângulo de origem deve ser igual ou menor que o tamanho de vídeo nativo; Você pode usar o método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) para obter o tamanho do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="5385d-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="5385d-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5385d-154">**VMR-9**</span></span>

1.  <span data-ttu-id="5385d-155">Chame o método [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para especificar os dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="5385d-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="5385d-156">O retângulo de origem deve ser igual ou menor que o tamanho de vídeo nativo; Você pode usar o método [**IVMRWindowlessControl9:: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) para obter o tamanho do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="5385d-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="5385d-157">Por exemplo, o código a seguir define os retângulos de origem e de destino para o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="5385d-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="5385d-158">Ele define o retângulo de origem igual à imagem de vídeo inteira e o retângulo de destino igual a toda a área do cliente da janela:</span><span class="sxs-lookup"><span data-stu-id="5385d-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="5385d-159">Se você quiser que o vídeo ocupe uma parte menor da área do cliente, modifique o parâmetro *rcDest* .</span><span class="sxs-lookup"><span data-stu-id="5385d-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="5385d-160">Se você quiser cortar a imagem de vídeo, modifique o parâmetro *rcSrc* .</span><span class="sxs-lookup"><span data-stu-id="5385d-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="5385d-161">Processar mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="5385d-161">Handle Window Messages</span></span>

<span data-ttu-id="5385d-162">Como o VMR não tem sua própria janela, ele deve ser notificado se precisar redesenhar ou redimensionar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="5385d-163">Responda às mensagens da janela a seguir chamando os métodos do VMR listados.</span><span class="sxs-lookup"><span data-stu-id="5385d-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="5385d-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5385d-164">**VMR-7**</span></span>

1.  <span data-ttu-id="5385d-165">[**WM \_ PINTAR**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="5385d-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="5385d-166">Chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="5385d-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="5385d-167">Esse método faz com que o VMR-7 repinte o quadro de vídeo mais recente.</span><span class="sxs-lookup"><span data-stu-id="5385d-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="5385d-168">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chamar [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="5385d-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="5385d-169">Esse método notifica o VMR-7 que o vídeo deve ser mostrado em uma nova resolução ou profundidade de cor.</span><span class="sxs-lookup"><span data-stu-id="5385d-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="5385d-170">[**WM \_ TAMANHO**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule a posição do vídeo e chame [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para atualizar a posição, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5385d-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="5385d-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5385d-171">**VMR-9**</span></span>

1.  <span data-ttu-id="5385d-172">[**WM \_ PINTAR**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="5385d-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="5385d-173">Chame [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="5385d-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="5385d-174">Esse método faz com que o VMR-9 repinte o quadro de vídeo mais recente.</span><span class="sxs-lookup"><span data-stu-id="5385d-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="5385d-175">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chamar [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="5385d-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="5385d-176">Esse método notifica o VMR-9 que o vídeo deve ser mostrado em uma nova resolução ou profundidade de cor.</span><span class="sxs-lookup"><span data-stu-id="5385d-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="5385d-177">[**WM \_ TAMANHO**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule a posição do vídeo e chame [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para atualizar a posição, se necessário.</span><span class="sxs-lookup"><span data-stu-id="5385d-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="5385d-178">O manipulador padrão para a mensagem do [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) envia uma mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) .</span><span class="sxs-lookup"><span data-stu-id="5385d-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="5385d-179">Mas se seu aplicativo intercepta o **WM \_ WINDOWPOSCHANGED** e não o passa para o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), você deve chamar **SetVideoPosition** em seu manipulador de **\_ WINDOWPOSCHANGED do WM** , além do seu manipulador de **\_ tamanho do WM** .</span><span class="sxs-lookup"><span data-stu-id="5385d-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="5385d-180">O exemplo a seguir mostra um manipulador de mensagens de [**\_ pintura do WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="5385d-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="5385d-181">Ele pinta uma região definida pelo retângulo do cliente menos o retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="5385d-182">Não desenhe no retângulo de vídeo, pois o VMR irá pintar sobre ele, causando oscilação.</span><span class="sxs-lookup"><span data-stu-id="5385d-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="5385d-183">Pelo mesmo motivo, não defina um pincel de plano de fundo em sua classe de janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="5385d-184">Embora seja necessário responder às mensagens do [**WM \_ Paint**](../gdi/wm-paint.md) , não há nada que você precise fazer entre as mensagens do **WM \_ Paint** para atualizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5385d-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="5385d-185">Como mostra este exemplo, o modo sem janela permite tratar a imagem de vídeo simplesmente como uma região de desenho automático na janela.</span><span class="sxs-lookup"><span data-stu-id="5385d-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5385d-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5385d-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5385d-187">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="5385d-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="5385d-188">Renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="5385d-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
