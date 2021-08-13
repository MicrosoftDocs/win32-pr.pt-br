---
title: Práticas recomendadas DirectX Graphic Infrastructure (DXGI)
description: Este artigo aborda os principais problemas de portação.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be992fe2346868eb3481482325297a2c9ec27ee61bdd2c65f83b0f916fc22308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290233"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX Graphic Infrastructure (DXGI): Práticas recomendadas

A DXGI (DirectX Graphic Infrastructure) da Microsoft é um novo subsistema que foi introduzido com o Windows Vista que encapsula algumas das tarefas de baixo nível que são necessárias pelo Direct3D 10, 10.1, 11 e 11.1. Da perspectiva de um programador do Direct3D 9, o DXGI abrange a maior parte do código para enumeração, criação de cadeia de permuta e apresentação que anteriormente era empacotada nas APIs do Direct3D 9. Quando você porta um aplicativo para DXGI e Direct3D 10.x e Direct3D 11.x, você precisa levar algumas considerações em consideração para garantir que o processo seja executado sem problemas.

Este artigo aborda os principais problemas de portação.

-   [Problemas de tela inteira](#full-screen-issues)
-   [Vários monitores](#multiple-monitors)
-   [Estilos de janela e DXGI](#window-styles-and-dxgi)
-   [Multithreading e DXGI](#multithreading-and-dxgi)
-   [Gama e DXGI](#gamma-and-dxgi)
-   [DXGI 1.1](#dxgi-11)
-   [DXGI 1.2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen problemas

Na portação do Direct3D 9 para o DXGI e para o Direct3D 10.x ou Direct3D 11.x, problemas associados à mudança da janela para o modo de tela inteira geralmente podem causar problemas para desenvolvedores. Os principais problemas surgem porque os aplicativos Direct3D 9, ao contrário de aplicativos DXGI, exigem uma abordagem mais prática para acompanhar estilos de janela e estados de janela. Quando o código que altera o modo é portado para ser executado no DXGI, ele geralmente causa um comportamento inesperado.

Geralmente, os aplicativos Direct3D 9 manipulam a transição para o modo de tela inteira definindo a resolução do buffer frontal, forçando o dispositivo no modo exclusivo de tela inteira e, em seguida, definindo as resoluções de buffer de fundo para corresponder. Um caminho separado foi usado para alterações no tamanho da janela porque elas tinham que ser gerenciadas do processo de janela sempre que o aplicativo recebe uma mensagem WM \_ SIZE.

O DXGI tenta simplificar essa abordagem combinando os dois casos. Por exemplo, quando a borda da janela é arrastada no modo de janela, o aplicativo recebe uma mensagem WM \_ SIZE. O DXGI intercepta essa mensagem e reamostra automaticamente o buffer frontal. Tudo o que o aplicativo precisa fazer é chamar [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) para resize o buffer de fundo para o tamanho que foi passado como parâmetros no WM \_ SIZE. Da mesma forma, quando o aplicativo precisa alternar entre o modo de tela inteira e janela, o aplicativo pode simplesmente chamar [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). O DXGI resize o buffer frontal para corresponder ao modo de tela inteira recém-selecionado e envia uma mensagem WM \_ SIZE para o aplicativo. O aplicativo chama novamente **ResizeBuffers**, assim como faria se a borda da janela fosse arrastada.

A metodologia da explicação anterior segue um caminho muito específico. O DXGI definiu a resolução de tela inteira para a resolução da área de trabalho por padrão. Muitos aplicativos, no entanto, alternam para uma resolução de tela inteira preferencial. Nesse caso, o DXGI fornece [**IDXGISwapChain::ResizeTarget.**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) Isso deve ser chamado antes de chamar [**SetFullscreenState.**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) Embora esses métodos possam ser chamados na ordem oposta (**SetFullscreenState** primeiro, seguido por **ResizeTarget**), fazer isso faz com que uma mensagem WM SIZE extra seja enviada ao \_ aplicativo. (Isso também pode causar cintilação, pois o DXGI pode ser forçado a executar duas alterações de modo.) Depois de **chamar SetFullscreenState**, é aconselhável chamar **ResizeTarget** novamente com o membro **RefreshRate** do [**\_ DXGI MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) zerado. Isso equivale a uma instrução sem operação no DXGI, mas pode evitar problemas com a taxa de atualização, que são discutidas a seguir.

Quando estiver no modo de tela inteira, a Gerenciador de Janelas da Área de Trabalho (DWM) será desabilitada. O DXGI pode executar uma in flip para apresentar o conteúdo do buffer de fundo em vez de fazer um blit, o que ele faria no modo em janelas. Esse ganho de desempenho pode ser desfeito, no entanto, se determinados requisitos não são atendidos. Para garantir que o DXGI faça uma in flip em vez de um blit, o buffer frontal e o buffer de fundo devem ser dimensionados de forma idêntica. Se o aplicativo tratar corretamente suas mensagens WM \_ SIZE, isso não deverá ser um problema. Além disso, os formatos devem ser idênticos.

O problema para a maioria dos aplicativos é a taxa de atualização. A taxa de atualização especificada na chamada para [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) deve ser uma taxa de atualização enumerada pelo objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que a cadeia de permuta está usando. O DXGI poderá calcular automaticamente esse valor se o aplicativo zerar o membro **RefreshRate** do [**\_ DXGI MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) que é passado para **ResizeTarget.** É importante não supor que determinadas taxas de atualização sempre terão suporte e simplesmente codificar um valor. Geralmente, os desenvolvedores escolhem 60 Hz como a taxa de atualização, sem saber que a taxa de atualização enumerada do monitor é de aproximadamente 60.000 /1.001 Hz do monitor. Se a taxa de atualização não corresponder à taxa de atualização esperada de 60, o DXGI será forçado a executar um blit no modo de tela inteira em vez de uma in flip.

O último problema que os desenvolvedores geralmente enfrentam é como alterar as resoluções de tela inteira enquanto permanecem no modo de tela inteira. Chamar [**ResizeTarget e**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) às vezes é bem-sucedido, mas a resolução de tela inteira permanece a resolução da área de trabalho. Além disso, os desenvolvedores podem criar uma cadeia de permuta de tela inteira e dar uma resolução específica, apenas para descobrir que o DXGI assume como padrão a resolução da área de trabalho, independentemente dos números passados. A menos que seja instruído de outra forma, o DXGI assume como padrão a resolução da área de trabalho para cadeias de permuta de tela inteira. Ao criar uma cadeia de permuta de tela inteira, o membro **Flags** da estrutura [**\_ DXGI SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) deve ser definido como [**DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) para substituir o comportamento padrão do DXGI. Esse sinalizador também pode ser passado para **ResizeTarget** para habilitar ou desabilitar essa funcionalidade dinamicamente.

## <a name="multiple-monitors"></a>Vários monitores

Ao usar o DXGI com vários monitores, há duas regras a seguir.

A primeira regra se aplica à criação de duas ou mais cadeias de permuta de tela inteira em vários monitores. Ao criar essas cadeias de permuta, é melhor criar todas as cadeias de permuta como janelas e, em seguida, defini-las como tela inteira. Se cadeias de permuta são criadas no modo de tela inteira, a criação de uma segunda cadeia de permuta faz com que uma alteração de modo seja enviada para a primeira cadeia de permuta, o que pode causar o encerramento do modo de tela inteira.

A segunda regra se aplica às saídas. Fique atento às saídas usadas ao criar cadeias de permuta. Com o DXGI, o [**objeto IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controla que monitoram o uso da cadeia de permuta ao se tornar tela inteira. Ao contrário do DXGI, o Direct3D 9 não tinha nenhum conceito de saídas.

## <a name="window-styles-and-dxgi"></a>Estilos de janela e DXGI

Os aplicativos Direct3D 9 tinham muito trabalho a fazer ao alternar entre os modos de tela inteira e em janelas. Grande parte desse trabalho envolve a alteração de estilos de janela para adicionar e remover bordas, adicionar barras de rolagem e assim por diante. Quando os aplicativos são portados para DXGI e Direct3D 10.x ou Direct3D 11.x, esse código geralmente é deixado no lugar. Dependendo das alterações feitas, alternar entre modos pode causar um comportamento inesperado. Por exemplo, ao alternar para o modo em janela, o aplicativo pode não ter mais um quadro de janela ou borda de janela, apesar de ter código que define especificamente esses estilos. Isso ocorre porque o DXGI agora lida com grande parte desse estilo mudando por conta própria. A configuração manual de estilos de janela pode interferir no DXGI e isso pode causar um comportamento inesperado.

O comportamento recomendado é fazer o menos trabalho possível e permitir que o DXGI manipular a maior parte da interação com as janelas. No entanto, se o aplicativo precisar lidar com seu próprio comportamento de janela, [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) poderá ser usado para dizer ao DXGI para desabilitar parte de seu tratamento automático de janela.

## <a name="multithreading-and-dxgi"></a>Multithreading e DXGI

Deve-se ter um cuidado especial ao usar a DXGI em um aplicativo multithread para garantir que não ocorram deadlocks. Devido à interação próxima do DXGI com a janela, ele ocasionalmente envia mensagens de janela para a janela do aplicativo associado. O DXGI precisa que as alterações de janela ocorram antes de continuar, portanto, ele usará [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que é uma chamada síncrona. O aplicativo deve processar a mensagem de janela antes **que SendMessage** retorne.

Em um aplicativo em que as chamadas DXGI e a bomba de mensagens estão no mesmo thread (ou em um aplicativo de thread único), pouco precisa ser feito. Quando a chamada DXGI está no mesmo thread que a bomba de mensagens, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) chama [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))da janela. Isso ignora a bomba de mensagens e permite que a execução continue após a chamada para **SendMessage.** Lembre-se de que chamadas [**IDXGISwapChain,**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) como [**IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), também são consideradas chamadas DXGI; O DXGI pode adiar o trabalho de [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) [**ou ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) até **que Present** seja chamado.

Se a chamada DXGI e a bomba de mensagens estão em threads diferentes, é necessário ter cuidado para evitar deadlocks. Quando a bomba de mensagens e SendMessage estão em threads diferentes, [**o SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) adiciona uma mensagem à fila de mensagens da janela e aguarda a janela processar essa mensagem. Se o procedimento de janela estiver ocupado ou não for chamado pela bomba de mensagem, a mensagem poderá nunca ser processada e o DXGI aguardará indefinidamente.

Por exemplo, se um aplicativo que tem sua bomba de mensagem em um thread e sua renderização em outro, talvez queira alterar os modos. O thread de bomba de mensagem informa o thread de renderização para alterar os modos e aguarda até que a alteração do modo seja concluída. No entanto, o thread de renderização chama funções DXGI, que, por sua vez, chamam [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que bloqueia até que a bomba de mensagens processe a mensagem. Um deadlock ocorre porque ambos os threads agora estão bloqueados e estão aguardando uns nos outros. Para evitar isso, nunca bloqueie a bomba de mensagens. Se um bloco for inevitável, toda a interação DXGI deverá ocorrer no mesmo thread que a bomba de mensagem.

## <a name="gamma-and-dxgi"></a>Gama e DXGI

Embora a gama gama possa ser melhor tratada no Direct3D 10.x ou direct3D 11.x usando texturas SRGB, a rampa gama ainda pode ser útil para desenvolvedores que querem um valor gama diferente de 2.2 ou que estão usando um formato de destino de renderização que não dá suporte ao SRGB. Esteja ciente de dois problemas ao definir a rampa gama por meio do DXGI. O primeiro problema é que os valores de rampa passados para [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) são valores float, não **valores WORD.** Além disso, verifique se o código portado do Direct3D 9 não tenta converter em valores **WORD** antes de passá-los **para SetGammaControl.**

O segundo problema é que, depois de alterar para o modo de tela inteira, [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) pode não parecer funcionar, dependendo do objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que está sendo usado. Ao alterar para o modo de tela inteira, o DXGI cria um novo objeto de saída e usa o objeto para todas as operações subsequentes na saída. Se chamar **SetGammaControl em** uma saída enumerada antes de uma opção de modo de tela inteira, a chamada não será direcionada para a saída que o DXGI está usando no momento. Para evitar isso, chame [**IDXGISwapChain::GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) para obter a saída atual e, em seguida, chame **SetGammaControl** fora dessa saída para obter o comportamento correto.

Para obter informações sobre como usar a correção gama, consulte [Usando a correção gama](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1.1

O runtime do Direct3D 11 incluído no Windows 7 e instalado no Windows Vista (consulte [KB971644](https://support.microsoft.com/kb/971644)) inclui a versão 1.1 do DXGI. Essa atualização adiciona definições para vários novos formatos (especialmente BGRA, desvio X2 de 10 bits e compactação de textura BC6H e BC7 do Direct3D 11), bem como uma nova versão das interfaces de adaptador e fábrica DXGI ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) para enumerar conexões de área de trabalho remota.

Quando você usa o Direct3D 11, o runtime usará o DXGI 1.1 por padrão ao chamar [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) com um ponteiro [**NULL IDXGIAdapter.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) Não há suporte para a combinação do uso do DXGI 1.0 e do DXGI 1.1 no mesmo processo. Também não há suporte para a combinação de instâncias de objeto DXGI de fábricas diferentes no mesmo processo. Portanto, quando você usa o DirectX 11, qualquer uso explícito das interfaces DXGI usa um [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) criado pelo ponto de entrada [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) em "DXGI.DLL" para garantir que o aplicativo sempre está usando o DXGI 1.1.

## <a name="dxgi-12"></a>DXGI 1.2

O runtime do Direct3D 11.1 incluído no Windows 8 também inclui a versão 1.2 do DXGI.

O DXGI 1.2 habilita estes recursos:

-   renderização estéreo
-   Formatos de 16 bits por pixel

    -   Formato DXGI \_ \_ B5G6R5 \_ UNORM e FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM agora têm suporte total
    -   um novo formato DXGI \_ \_ B5G5R5A1 \_ UNORM foi adicionado

-   formatos de vídeo
-   novas interfaces DXGI

Para obter mais informações sobre os recursos do DXGI 1.2, consulte [Melhorias do DXGI 1.2.](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

 

 