---
description: Usando o modo sem janela
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Usando o modo sem janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5189fb52932a328493baec9a79ccd6598a9a0659c198ee3ce3d4d157574a63c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119271246"
---
# <a name="using-windowless-mode"></a>Usando o modo sem janela

O [filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) e o filtro de processador de mixagem de [vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) dão suporte ao *modo sem janela*, que representa uma grande melhoria na interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Este tópico descreve as diferenças entre o modo sem janela e o modo de janela e como usar o modo sem janela.

Para manter a compatibilidade com versões anteriores com os aplicativos existentes, o VMR usa como padrão o modo de janela. No modo de janela, o renderizador cria sua própria janela para exibir o vídeo. Normalmente, o aplicativo define a janela de vídeo como um filho da janela do aplicativo. No entanto, a existência de uma janela de vídeo separada causa alguns problemas:

-   O mais importante é que haja um potencial para deadlocks se as mensagens de janela forem enviadas entre threads.
-   o filtro Graph Manager deve encaminhar certas mensagens da janela, como \_ o WM PAINT, ao processador de vídeo. o aplicativo deve usar o filtro Graph implementação do gerenciador de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (e não do processador de vídeo), para que o filtro Graph gerenciador mantenha o estado interno correto.
-   Para receber eventos de mouse ou de teclado da janela de vídeo, o aplicativo deve definir uma *drenagem de mensagem*, fazendo com que a janela de vídeo encaminhe essas mensagens para o aplicativo.
-   Para evitar problemas de recorte, a janela de vídeo deve ter os estilos de janela corretos.

O modo sem janela evita esses problemas fazendo com que o VMR desenhe diretamente na área do cliente da janela do aplicativo, usando o DirectDraw para recortar o retângulo de vídeo. O modo sem janela reduz significativamente a chance de deadlocks. Além disso, o aplicativo não precisa definir a janela do proprietário nem os estilos da janela. Na verdade, quando o VMR está no modo sem janela, ele nem mesmo expõe a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , que não é mais necessária.

Para usar o modo sem janela, você deve configurar explicitamente o VMR. No entanto, você verá que é mais flexível e mais fácil de usar do que o modo em janela.

O filtro VMR-7 e o filtro VMR-9 expõem interfaces diferentes, mas as etapas são equivalentes para cada uma.

## <a name="configure-the-vmr-for-windowless-mode"></a>Configurar o VMR para o modo sem janela

Para substituir o comportamento padrão do VMR, configure o VMR antes de criar o grafo de filtro:

**VMR-7**

1.  crie o filtro Graph Manager.
2.  Crie o VMR-7 e adicione-o ao grafo de filtro.
3.  Chame [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) no VMR-7 com o sinalizador **VMRMode \_ sem janela** .
4.  Consulte o VMR-7 para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
5.  Chame [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) no VMR-7. Especifique um identificador para a janela em que o vídeo deve aparecer.

**VMR-9**

1.  crie o filtro Graph Manager.
2.  Crie o VMR-9 e adicione-o ao grafo de filtro.
3.  Chame [**IVMRFilterConfig9:: Setrenderizamode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) no VMR-9 com o sinalizador **VMR9Mode \_ sem janela** .
4.  Consulte o VMR-9 para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
5.  Chame [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) no VMR-9. Especifique um identificador para a janela em que o vídeo deve aparecer.

Agora, compile o restante do grafo de filtro chamando [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou outros métodos de criação de grafo. o filtro Graph Manager usa automaticamente a instância do VMR que você adicionou ao grafo. (para obter detalhes sobre por que isso acontece, consulte [Intelligent Conexão](intelligent-connect.md).)

O código a seguir mostra uma função auxiliar que cria o VMR-7, adiciona-o ao grafo e define o modo sem janela.


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



Essa função pressupõe que está exibindo apenas um fluxo de vídeo e não está misturando um bitmap estático no vídeo. Para obter detalhes, consulte [modo sem janela do VMR](vmr-windowless-mode.md). Você chamaria essa função da seguinte maneira:


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



## <a name="position-the-video"></a>Posicionar o vídeo

Depois de configurar o VMR, a próxima etapa é definir a posição do vídeo. Há dois retângulos a serem considerados, o retângulo de *origem* e o retângulo de *destino* . O retângulo de origem define a parte do vídeo a ser exibida. O retângulo de destino especifica a região na área do cliente da janela que conterá o vídeo. O VMR corta a imagem de vídeo para o retângulo de origem e amplia a imagem cortada para se ajustar ao retângulo de destino.

**VMR-7**

1.  Chame o método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para especificar os dois retângulos.
2.  O retângulo de origem deve ser igual ou menor que o tamanho de vídeo nativo; Você pode usar o método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) para obter o tamanho do vídeo nativo.

**VMR-9**

1.  Chame o método [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para especificar os dois retângulos.
2.  O retângulo de origem deve ser igual ou menor que o tamanho de vídeo nativo; Você pode usar o método [**IVMRWindowlessControl9:: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) para obter o tamanho do vídeo nativo.

Por exemplo, o código a seguir define os retângulos de origem e de destino para o VMR-7. Ele define o retângulo de origem igual à imagem de vídeo inteira e o retângulo de destino igual a toda a área do cliente da janela:


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



Se você quiser que o vídeo ocupe uma parte menor da área do cliente, modifique o parâmetro *rcDest* . Se você quiser cortar a imagem de vídeo, modifique o parâmetro *rcSrc* .

## <a name="handle-window-messages"></a>Processar mensagens de janela

Como o VMR não tem sua própria janela, ele deve ser notificado se precisar redesenhar ou redimensionar o vídeo. Responda às mensagens da janela a seguir chamando os métodos do VMR listados.

**VMR-7**

1.  [**WM \_ PINTAR**](../gdi/wm-paint.md). Chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Esse método faz com que o VMR-7 repinte o quadro de vídeo mais recente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chamar [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Esse método notifica o VMR-7 que o vídeo deve ser mostrado em uma nova resolução ou profundidade de cor.
3.  [**WM \_ TAMANHO**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule a posição do vídeo e chame [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) para atualizar a posição, se necessário.

**VMR-9**

1.  [**WM \_ PINTAR**](../gdi/wm-paint.md). Chame [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Esse método faz com que o VMR-9 repinte o quadro de vídeo mais recente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chamar [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Esse método notifica o VMR-9 que o vídeo deve ser mostrado em uma nova resolução ou profundidade de cor.
3.  [**WM \_ TAMANHO**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule a posição do vídeo e chame [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) para atualizar a posição, se necessário.

> [!Note]  
> O manipulador padrão para a mensagem do [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) envia uma mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) . Mas se seu aplicativo intercepta o **WM \_ WINDOWPOSCHANGED** e não o passa para o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), você deve chamar **SetVideoPosition** em seu manipulador de **\_ WINDOWPOSCHANGED do WM** , além do seu manipulador de **\_ tamanho do WM** .

 

O exemplo a seguir mostra um manipulador de mensagens de [**\_ pintura do WM**](../gdi/wm-paint.md) . Ele pinta uma região definida pelo retângulo do cliente menos o retângulo de vídeo. Não desenhe no retângulo de vídeo, pois o VMR irá pintar sobre ele, causando oscilação. Pelo mesmo motivo, não defina um pincel de plano de fundo em sua classe de janela.


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



Embora seja necessário responder às mensagens do [**WM \_ Paint**](../gdi/wm-paint.md) , não há nada que você precise fazer entre as mensagens do **WM \_ Paint** para atualizar o vídeo. Como mostra este exemplo, o modo sem janela permite tratar a imagem de vídeo simplesmente como uma região de desenho automático na janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 
