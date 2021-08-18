---
description: Um aplicativo Direct3D normalmente exibe uma sequência animada, gerando os quadros da animação nos buffers de fundo e apresentando-os em sequência.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Invertendo superfícies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c14aa7df63c3956d4974282033b44a7129853940d475b23115f9bca344ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988027"
---
# <a name="flipping-surfaces-direct3d-9"></a>Invertendo superfícies (Direct3D 9)

Um aplicativo Direct3D normalmente exibe uma sequência animada, gerando os quadros da animação nos buffers de fundo e apresentando-os em sequência. Os buffers de fundo são organizados em cadeias de troca. Uma cadeia de permuta é uma série de buffers que "invertem" para a tela um após o outro. Isso pode ser usado para renderizar uma cena na memória e, em seguida, virar a cena para a tela quando a renderização for concluída. Isso evita o fenômeno conhecido como divisão e permite uma animação mais suave.

Cada dispositivo criado no Direct3D tem pelo menos uma cadeia de permuta. Ao inicializar o primeiro dispositivo Direct3D, você define o membro BackBufferCount de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md), que informa ao Direct3D o número de buffers de fundo que estarão na cadeia de permuta. A chamada para [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cria o dispositivo Direct3D e a cadeia de permuta correspondente.

Quando você usa [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para solicitar uma operação de inversão de superfície, os ponteiros para a memória de superfície para o buffer frontal e buffers de fundo são trocados. A inversão é realizada alternando os ponteiros que o dispositivo de vídeo usa para fazer referência à memória, não copiando a memória da superfície. Quando uma cadeia de inversão contém um buffer frontal e mais de um buffer de fundo, os ponteiros são alternados em um padrão circular, conforme mostrado no diagrama a seguir.

![diagrama de uma cadeia de inversão com um buffer frontal e dois buffers de fundo](images/trplflip.png)

Você pode criar cadeias de permuta adicionais para um dispositivo chamando [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/desktop/api). Um aplicativo pode criar uma cadeia de permuta por exibição e associar cada cadeia de permuta a uma janela específica. O aplicativo renderiza as imagens nos buffers de fundo de cada cadeia de permuta e as apresenta individualmente. Os dois parâmetros que **IDirect3DDevice9:: CreateAdditionalSwapChain** usa são um ponteiro para uma estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) e o endereço de um ponteiro para uma interface [**IDirect3DSwapChain9**](/windows/desktop/api) . Em seguida, você pode usar [**IDirect3DSwapChain9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) para exibir o conteúdo do próximo buffer de fundo para o buffer frontal. Observe que um dispositivo pode ter apenas uma cadeia de troca de tela inteira.

Você pode obter acesso a um buffer de fundo específico chamando os métodos [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) ou [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , que retornam um ponteiro para uma interface [**IDirect3DSurface9**](/windows/desktop/api) que representa a superfície de buffer de fundo retornada. Observe que a chamada desse método aumenta a contagem de referência interna na interface [**IDirect3DDevice9**](/windows/desktop/api) , portanto, não se esqueça de chamar [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) quando terminar de usar essa superfície ou se você tiver um vazamento de memória.

Lembre-se de que o Direct3D inverte as superfícies alternando os ponteiros de memória da superfície dentro da cadeia de permuta, não alternando as superfícies em si. Isso significa que você sempre será renderizado para o buffer de fundo que será exibido em seguida.

É importante observar a distinção entre uma "operação de inversão", conforme executada por um driver de adaptador de vídeo, e uma operação "presente" aplicada a uma cadeia de permuta criada com D3DSWAPEFFECT \_ flip.

O termo "inverter" indica, em Convenção, uma operação que altera o intervalo de endereços de memória de vídeo que um adaptador de vídeo usa para gerar seu sinal de saída, fazendo com que o conteúdo de um buffer de fundo oculto anteriormente seja exibido. No Direct3D 9, o termo geralmente é usado com mais frequência para descrever a apresentação de um buffer de fundo em qualquer cadeia de permuta criada com o efeito de permuta inD3DSWAPEFFECT \_ invertido.

Embora essas operações "presentes" sejam quase invariavelmente implementadas por operações invertidas quando a cadeia de permuta é uma tela inteira, elas são necessariamente implementadas por operações de cópia quando a cadeia de permuta é janelada. Além disso, um driver de adaptador de vídeo pode usar inverter para implementar operações presentes em cadeias de permuta de tela inteira com base na \_ cópia D3DSWAPEFFECT e D3DSWAPEFFECT \_ .

A discussão acima se aplica ao caso usado normalmente de uma cadeia de permuta de tela inteira criada com D3DSWAPEFFECT \_ flip.

Para obter uma discussão mais geral dos diferentes efeitos de permuta para as cadeias de troca de tela inteira e em janelas, consulte [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
