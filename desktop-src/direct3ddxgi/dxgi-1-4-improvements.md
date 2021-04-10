---
description: A funcionalidade a seguir foi adicionada ou alterada na Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, em grande parte para dar suporte ao Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Aprimoramentos de DXGI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e9a8a48dd026248afac7c1a7df23a99176adef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009923"
---
# <a name="dxgi-14-improvements"></a>Aprimoramentos de DXGI 1,4

A funcionalidade a seguir foi adicionada ou alterada na Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, em grande parte para dar suporte ao Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Enumeração de adaptador mais barata

Para o Direct3D 12, não é mais possível refazer o retrocesso de um dispositivo para o [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que foi usado para criá-lo. Também não é mais possível fornecer o tipo de \_ Driver \_ D3D \_ Warp em [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Para facilitar o desenvolvimento, você pode usar o [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) para lidar com ambos. [**IDXGIFactory4:: EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (projetado para ser emparelhado com [**ID3D12Device:: GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)) permite que um aplicativo recupere informações sobre o adaptador onde um dispositivo Direct3D 12 foi criado. [**IDXGIFactory4:: EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) fornece um adaptador que pode ser fornecido ao **D3D12CreateDevice** para usar o processador de detorção.

## <a name="video-memory-budget-tracking"></a>Acompanhamento de orçamento de memória de vídeo

Os desenvolvedores de aplicativos são incentivados a usar um sistema de reserva de memória de vídeo para informar ao sistema operacional a quantidade de memória de vídeo física que o aplicativo não pode acessar sem.

A quantidade de memória física disponível para um processo é conhecida como "orçamento de memória de vídeo". O orçamento pode flutuar visivelmente enquanto os processos em segundo plano são ativados e suspensos; e flutuar drasticamente quando o usuário mudar para outro aplicativo. O aplicativo pode ser notificado quando o orçamento for alterado e sondar o orçamento atual e a quantidade de memória consumida atualmente. Se um aplicativo não permanecer dentro de seu orçamento, o processo será congelado intermitentemente para permitir que outros aplicativos sejam executados e/ou as APIs de criação retornarão uma falha. A interface [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornece os métodos que pertencem a essa funcionalidade, em particular [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Para obter mais informações, consulte o tópico do Direct3D 12 sobre [residência](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Mudanças do Direct3D 12 SwapChain

Algumas das funcionalidades existentes do Direct3D 11 SwapChain foram preteridas para alcançar as reduções de sobrecarga no Direct3D 12. Enquanto outras alterações foram feitas para se alinharem aos conceitos do Direct3D 12 ou fornecer melhor suporte para os recursos do Direct3D 12.

**Identidade de BackBuffer invariável**

No Direct3D 11, os aplicativos podiam chamar [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)(0,... ) apenas uma vez. Cada chamada para [**apresentar**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) alterou implicitamente a identidade do recurso da interface retornada. O Direct3D 12 não dá mais suporte a alterações implícitas de identidade de recurso, devido à sobrecarga de CPU necessária e ao design de descritor de recursos flexível. Como resultado, o aplicativo deve chamar manualmente o **GetBuffer** para cada buffer criado com o SwapChain. O aplicativo deve ser processado manualmente para o próximo buffer na sequência após a chamada **presente**. Os aplicativos são incentivados a criar um cache de descritores para cada buffer, em vez de recriar muitos objetos a cada **presente**.

**Suporte a vários adaptadores**

Quando um SwapChain é criado em um adaptador de várias GPU, todos os buffers são criados no nó 1 e há suporte apenas para uma única fila de comando. O [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) permite que os aplicativos criem buffers totais em nós diferentes, permitindo que uma fila de comandos diferente seja usada com cada um. Esses recursos permitem que as técnicas de renderização de quadro alternativo (AFR) sejam usadas com o SwapChain. Consulte [sistemas com vários adaptadores](../direct3d12/multi-engine.md).

**Diversos**

-   Um objeto de fila de comando deve ser passado para métodos [**CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) em vez do objeto de dispositivo Direct3D 12.
-   Há suporte apenas para os dois efeitos de troca de modelo invertido a seguir: <dl> \_ \_ O efeito de permuta de dxgi \_ flip \_ descartar deve ser preferível quando os aplicativos são totalmente renderizados no BackBuffer antes de apresentá-lo ou ainda estar interessados em dar suporte a cenários de vários adaptadores.  
    O \_ efeito de permuta de dxgi \_ \_ inverter \_ sequencial deve ser usado por aplicativos que dependem de otimizações parciais de apresentação ou lidos regularmente dos buffers anteriores apresentados anteriormente.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Tópicos relacionados

[Níveis de recursos de hardware do Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
