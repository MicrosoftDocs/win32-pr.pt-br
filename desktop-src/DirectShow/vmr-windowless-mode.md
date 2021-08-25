---
description: Modo sem janela da VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modo sem janela da VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830576"
---
# <a name="vmr-windowless-mode"></a>Modo sem janela da VMR

O modo sem janelas é a maneira preferencial para os aplicativos renderizarem vídeo dentro de uma janela do aplicativo. No modo sem janelas, o Renderização de Combinação de Vídeo não carrega seu componente do Gerenciador de Janelas e, portanto, não dá suporte às interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) ou [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Em vez disso, o aplicativo fornece a janela de reprodução e define um retângulo de destino na área do cliente para a VMR desenhar o vídeo. A VMR usa um objeto clipper directDraw para garantir que o vídeo seja recortado na janela do aplicativo e não apareça em nenhuma outra janela. A VMR não subclasse a janela do aplicativo nem instala nenhum gancho de sistema/processo.

No modo sem janelas, a sequência de eventos durante a conexão e a transição para o estado de run é a seguinte:

-   O filtro upstream propõe um tipo de mídia, que a VMR aceita ou rejeita.
-   Se o tipo de mídia for aceito, a VMR chamará o allocator-presenter para obter uma superfície directDraw. Se a superfície for criada com êxito, os pinos se conectarão e a VMR estará pronta para fazer a transição para o estado de executar.
-   Quando o grafo de filtro é executado, o decodificador chama **GetBuffer** para obter um exemplo de mídia do alocador. A VMR consulta o allocator-presenter para garantir que a profundidade do pixel, o tamanho do retângulo e outros parâmetros em sua superfície do DirectDraw sejam compatíveis com o vídeo de entrada. Se eles são compatíveis, a VMR retorna a superfície directDraw para o decodificador. Depois que o decodificador tiver sido decodificado na superfície, a Unidade de Sincronização Principal da VMR validará os carimbos de data/hora. Esta unidade bloqueia a **chamada De** recebimento até a hora da apresentação chegar. Nesse ponto, a VMR chama **PresentImage** no allocator-presenter, que apresenta a superfície para a placa gráfica.

A ilustração a seguir mostra a VMR no modo sem janelas com vários fluxos de entrada.

![vmr no modo sem janelas](images/vmr-windowless-mult-streams.png)

**Configurando a VMR-7 para o modo sem janelas**

Para configurar a VMR-7 para o modo sem janela, execute todas as seguintes etapas antes de conectar qualquer um dos pinos de entrada da VMR:

1.  Crie o filtro e adicione-o ao grafo.
2.  Chame o [**método IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) com o sinalizador sem janela VMRMode. \_
3.  Opcionalmente, configure a VMR para vários fluxos de entrada chamando [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). A VMR cria um pino de entrada para cada fluxo. Use a interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para definir a ordem Z e outros parâmetros para o fluxo. Para obter mais informações, [consulte VMR com vários Fluxos (modo de combinação).](vmr-with-multiple-streams--mixing-mode.md)

    Se você não chamar **SetNumberOfStreams,** a VMR-7 assume como padrão um pino de entrada. Depois que os pinos de entrada são conectados, o número de pinos não pode ser alterado.

4.  Chame [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar a janela na qual o vídeo renderizado será exibido.

Depois que essas etapas são concluídas, você pode conectar os pinos de entrada do filtro VMR. Há várias maneiras de criar o grafo, como conectar pinos diretamente, usando métodos de Conexão inteligentes, como [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)ou usando o método [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do Construtor de Captura do Graph. Para obter mais informações, consulte [Técnicas Graph-Building geral.](general-graph-building-techniques.md)

Para definir a posição do vídeo dentro da janela do aplicativo, chame o [**método IVMRWindowlessControl::SetVideoPosition.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) O [**método IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) retorna o tamanho do vídeo nativo. Durante a reprodução, o aplicativo deve notificar a VMR das seguintes Windows mensagens:

-   WM \_ PAINT: chame [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para repintar a imagem.
-   WM \_ DISPLAYCHANGE: chame [**IVMRWindowlessControl::D isplayModeChanged.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged) A VMR toma todas as ações necessárias para exibir o vídeo na nova resolução ou profundidade de cor.
-   WM \_ SIZE: recalcula a posição do vídeo e chame [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) novamente, se necessário.

> [!Note]  
> Os aplicativos MFC devem definir um manipulador de mensagens WM ERASEBKGND vazio ou a área de exibição de vídeo \_ não será reintint corretamente.

 

**Configurando a VMR-9 para o modo sem janelas**

Para configurar a VMR-9 para o modo sem janela, use as etapas descritas para a VMR-7 para o modo sem janela, mas use as interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) A única diferença significativa é que a VMR-9 cria quatro pinos de entrada por padrão, em vez de um pino de entrada. Portanto, você só precisará chamar **SetNumberOfStreams** se estiver combinando mais de quatro fluxos de vídeo.

**Código de exemplo**

O código a seguir mostra como criar um filtro VMR-7, adicioná-lo ao grafo de filtro DirectShow e, em seguida, colocar a VMR no modo sem janelas. Para a VMR-9, use CLSID \_ VideoMixingRenderer9 em **CoCreateInstance** e as interfaces VMR-9 correspondentes.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo sem janelas](using-windowless-mode.md)
</dt> </dl>

 

 



