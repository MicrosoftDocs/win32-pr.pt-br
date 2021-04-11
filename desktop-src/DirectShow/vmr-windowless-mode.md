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
# <a name="vmr-windowless-mode"></a>Modo sem janela do VMR

O modo sem janela é a maneira preferida para os aplicativos renderizarem o vídeo dentro de uma janela de aplicativo. No modo sem janela, o processador de mixagem de vídeo não carrega o componente do Gerenciador de janelas e, portanto, não oferece suporte às interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) ou [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Em vez disso, o aplicativo fornece a janela de reprodução e define um retângulo de destino na área do cliente para o VMR desenhar o vídeo. O VMR usa um objeto Clipper do DirectDraw para garantir que o vídeo seja recortado na janela do aplicativo e não apareça em outras janelas. O VMR não faz a subclasse da janela do aplicativo nem instala quaisquer ganchos de sistema/processo.

No modo sem janela, a sequência de eventos durante a conexão e a transição para o estado de execução é a seguinte:

-   O filtro upstream propõe um tipo de mídia, que o VMR aceita ou rejeita.
-   Se o tipo de mídia for aceito, o VMR chamará o alocador-Presenter para obter uma superfície do DirectDraw. Se a superfície for criada com êxito, os PINs se conectarão e o VMR estará pronto para fazer a transição para o estado de execução.
-   Quando o grafo de filtro é executado, o decodificador chama **GetBuffer** para obter um exemplo de mídia do alocador. O VMR consulta o alocador-apresentador para garantir que a profundidade de pixels, o tamanho do retângulo e outros parâmetros em sua superfície do DirectDraw sejam compatíveis com o vídeo de entrada. Se forem compatíveis, o VMR retornará a superfície do DirectDraw para o decodificador. Depois que o decodificador for decodificado na superfície, a unidade de sincronização principal do VMR validará os carimbos de data/hora. Essa unidade bloqueia a chamada de **recebimento** até que o tempo de apresentação chegue. Nesse ponto, o VMR chama **PresentImage** no apresentador de alocador, que apresenta a superfície para a placa gráfica.

A ilustração a seguir mostra o VMR no modo sem janela com vários fluxos de entrada.

![VMR no modo sem janela](images/vmr-windowless-mult-streams.png)

**Configurando o VMR-7 para o modo sem janela**

Para configurar o VMR-7 para o modo sem janela, execute todas as etapas a seguir antes de conectar qualquer um dos Pins de entrada do VMR:

1.  Crie o filtro e adicione-o ao grafo.
2.  Chame o método [**IVMRFilterConfig:: Setrenderizamode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) com o \_ sinalizador VMRMode sem janela.
3.  Opcionalmente, configure o VMR para vários fluxos de entrada chamando [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). O VMR cria um PIN de entrada para cada fluxo. Use a interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) para definir a ordem Z e outros parâmetros para o fluxo. Para obter mais informações, consulte [VMR com vários fluxos (modo de combinação)](vmr-with-multiple-streams--mixing-mode.md).

    Se você não chamar **SetNumberOfStreams**, o VMR-7 usa como padrão um PIN de entrada. Depois que os Pins de entrada estiverem conectados, o número de Pins não poderá ser alterado.

4.  Chame [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para especificar a janela na qual o vídeo renderizado será exibido.

Depois que essas etapas forem concluídas, você poderá conectar os Pins de entrada do filtro do VMR. Há várias maneiras de criar o grafo, como conectar Pins diretamente, usando métodos de conexão inteligente, como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ou usando o método [**ICaptureGraphBuilder2:: MessageRenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do construtor de grafo de captura. Para obter mais informações, consulte [General Graph-Building Techniques](general-graph-building-techniques.md).

Para definir a posição do vídeo dentro da janela do aplicativo, chame o método [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) . O método [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) retorna o tamanho do vídeo nativo. Durante a reprodução, o aplicativo deve notificar o VMR das seguintes mensagens do Windows:

-   WM \_ Paint: chame [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) para redesenhar a imagem.
-   WM \_ DISPLAYCHANGE: chamar [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). O VMR usa todas as ações necessárias para exibir o vídeo na nova resolução ou profundidade de cor.
-   \_Tamanho do WM: recalcule a posição do vídeo e chame [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) novamente, se necessário.

> [!Note]  
> Os aplicativos MFC devem definir um \_ manipulador de mensagens ERASEBKGND do WM vazio ou a área de exibição do vídeo não será redesenhada corretamente.

 

**Configurando o VMR-9 para o modo sem janela**

Para configurar o VMR-9 para o modo sem janela, use as etapas descritas para o VMR-7 para o modo sem janela, mas use as interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . A única diferença significativa é que o VMR-9 cria quatro Pins de entrada por padrão, em vez de um PIN de entrada. Portanto, você só precisa chamar **SetNumberOfStreams** se estiver misturando mais de quatro fluxos de vídeo.

**Código de exemplo**

O código a seguir mostra como criar um filtro do VMR-7, adicioná-lo ao grafo de filtro do DirectShow e, em seguida, colocar o VMR no modo sem janela. Para o VMR-9, use CLSID \_ VideoMixingRenderer9 em **CoCreateInstance** e as interfaces do VMR-9 correspondentes.


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

[Usando o modo sem janela](using-windowless-mode.md)
</dt> </dl>

 

 



