---
title: Trocar cadeias
description: As cadeias de permuta controlam a rotação do buffer de fundo, formando a base da animação de gráficos.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548263"
---
# <a name="swap-chains"></a>Trocar cadeias

As cadeias de permuta controlam a rotação do buffer de fundo, formando a base da animação de gráficos.

## <a name="overview"></a>Visão geral

O modelo de programação para cadeias de permuta no Direct3D 12 não é idêntico ao de versões anteriores do D3D. A conveniência de programação, por exemplo, de suporte à rotação automática de recursos que estava presente em D3D10 e D3D11 agora não é suportada. Aplicativos habilitados para rotação de recursos automáticos para renderizar o mesmo objeto de API enquanto a superfície real sendo processada altera cada quadro. O comportamento de cadeias de permuta é alterado com o Direct3D 12 para permitir que outros recursos do Direct3D 12 tenham baixa sobrecarga de CPU. Não há suporte para a chave de cor automática e a multiamostrar, embora ainda seja possível esticar e girar.

### <a name="buffer-lifetime"></a>Tempo de vida do buffer

Os aplicativos têm permissão para armazenar descritores pré-criados que fazem referência a buffers de fundo isso é habilitado, garantindo que o conjunto de buffers de propriedade de uma cadeia de permuta nunca seja alterado durante o tempo de vida da cadeia de permuta. O conjunto de buffers retornado por [**IDXGISwapChain:: GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) não é alterado até que determinadas APIs sejam chamadas:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

A ordem dos buffers retornados por [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) nunca muda.

[**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) retorna o índice do buffer de fundo atual para o aplicativo.

### <a name="swap-effects"></a>Efeitos de permuta

Os únicos efeitos de permuta com suporte são [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) e [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), o que exige que a contagem de buffers seja maior que um.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transição entre os modos de tela inteira e em janela

O Direct3D 12 não dá suporte ao modo de tela inteira exclusiva (FSE). Em vez disso, quando um jogo é o único aplicativo visível na tela, o sistema operacional usa uma estratégia chamada FSO (optimisations de tela inteira) para obter um efeito semelhante ao FSE sem as desvantagens de desempenho. Para obter mais informações sobre o FSO, consulte [Desmistificando a tela inteira Optimisations](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

O Direct3D 12 mantém a restrição de que os aplicativos devem chamar [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) após a transição entre os modos de tela inteira e em janela (os cadeias de troca de modelo invertida D3D11 têm as mesmas restrições).

As transições [**IDXGISwapChain:: Setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) não alteram o conjunto de buffers visíveis do aplicativo na cadeia de permuta. Somente as chamadas [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) e [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) criam ou destruim buffers visíveis ao aplicativo. No entanto, no Direct3D 12 [**IDXGISwapChain:: Setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) não entra no modo de tela inteira e simplesmente altera resoluções e taxas de atualização para permitir optimisations de tela inteira. Essas alterações podem ser feitas por um aplicativo sem o uso deste método

Quando ou [**IDXGISwapChain::P reenviado**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) ou [**IDXGISwapChain1::P reenviado**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) é chamado, o buffer de fundo a ser apresentado deve estar no estado [**\_ \_ estado \_ atual do recurso D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) . Apresentar falhará com **a \_ \_ \_ chamada inválida de erro dxgi** se não for o caso.

As cadeias de permuta em tela inteira continuam a ter a restrição de que [**Setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, NULL) deve ser chamada antes da versão final da cadeia de permuta. **Setfullscreenstate**(false) tem sucesso em cadeias de permuta em execução em dispositivos Direct3D 12.

As operações presentes ocorrem na fila 3D fornecida na criação do SwapChain, e os aplicativos são livres para apresentar simultaneamente várias cadeias de permuta e gravar e executar listas de comandos.

Quando a parte final do trabalho de gráficos (por exemplo, o processo de execução de quadros) é feita em uma fila de computação ou não envolve a fila de gráficos do dispositivo, a criação de uma segunda fila 3D para apresentar pode ser benéfica e impedir a latência da apresentação atrasar o início do próximo quadro. 

### <a name="example"></a>Exemplo

O código de exemplo a seguir estaria presente no loop de renderização principal:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Criando cadeias de permuta

Ao usar as chamadas [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) , observe que o parâmetro *pDevice* realmente requer um ponteiro para uma fila de comando direto no Direct3D 12, e não um dispositivo.

### <a name="presenting-on-windows-7"></a>Apresentação no Windows 7

Ao direcionar o Direct3D 12 no Windows 7, os tipos de DXGI necessários para o Direct3D 12 não estão presentes, portanto, você deve usar o **ID3D12CommandQueueDownLevel** fornecido pelo D3D12On7 (consultado fora da fila de comando direto) para apresentar.

Você fornece uma lista de comandos abertos para o método presente do Windows 7, que será usado, fechado e enviado automaticamente para o dispositivo para você. Você deve fornecer um buffer de fundo que deve ser criado pelo aplicativo, deve ser um recurso confirmado, deve ser de amostra única e deve ser um dos formatos a seguir.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Tópicos relacionados

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Tutoriais de vídeo do DirectX Advanced Learning: taxa de quadros não limitado](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Renderização](rendering.md)
