---
title: Práticas recomendadas da infraestrutura de gráficos do DirectX (DXGI)
description: Este artigo aborda os principais problemas de portabilidade.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f576368674d05af74e3161d4251301ebc066a489
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366470"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DXGI (infra-estrutura de gráficos do DirectX): práticas recomendadas

A DXGI (DirectX Graphic Infrastructure) da Microsoft é um novo subsistema que foi introduzido com o Windows Vista que encapsula algumas das tarefas de baixo nível que são necessárias pelo Direct3D 10, 10.1, 11 e 11.1. Da perspectiva de um programador do Direct3D 9, DXGI abrange a maior parte do código para enumeração, criação da cadeia de permuta e apresentação que anteriormente foi empacotada nas APIs do Direct3D 9. Quando você porta um aplicativo para DXGI e o Direct3D 10. x e o Direct3D 11. x, precisa levar em conta algumas considerações para garantir que o processo seja executado sem problemas.

Este artigo aborda os principais problemas de portabilidade.

-   [Problemas de tela inteira](#full-screen-issues)
-   [Vários monitores](#multiple-monitors)
-   [Estilos de janela e DXGI](#window-styles-and-dxgi)
-   [Multithread e DXGI](#multithreading-and-dxgi)
-   [Gama e DXGI](#gamma-and-dxgi)
-   [DXGI 1,1](#dxgi-11)
-   [DXGI 1,2](#dxgi-12)

## <a name="full-screen-issues"></a>Problemas de Full-Screen

Em portamento do Direct3D 9 para DXGI e para o Direct3D 10. x ou Direct3D 11. x, os problemas associados à mudança de janelas para o modo de tela inteira geralmente podem causar dores de cabeça para os desenvolvedores. Os principais problemas surgem porque os aplicativos do Direct3D 9, diferentemente dos aplicativos DXGI, exigem uma abordagem mais prática para rastrear estilos de janela e Estados de janela. Quando o código de alteração de modo é portado para ser executado em DXGI, ele geralmente causa um comportamento inesperado.

Muitas vezes, os aplicativos do Direct3D 9 trataram a transição para o modo de tela inteira definindo a resolução do buffer frontal, forçando o dispositivo para o modo exclusivo de tela inteira e, em seguida, definindo as resoluções de buffer de fundo para corresponder. Um caminho separado foi usado para alterações no tamanho da janela porque eles precisavam ser gerenciados a partir do processo de janela sempre que o aplicativo recebeu uma mensagem de tamanho do WM \_ .

DXGI tenta simplificar essa abordagem combinando os dois casos. Por exemplo, quando a borda da janela é arrastada no modo de janela, o aplicativo recebe uma mensagem de tamanho do WM \_ . DXGI intercepta essa mensagem e redimensiona automaticamente o buffer frontal. Tudo o que o aplicativo precisa fazer é chamar [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) para redimensionar o buffer de fundo para o tamanho que foi passado como parâmetros no tamanho do WM \_ . Da mesma forma, quando o aplicativo precisa alternar entre o modo de tela inteira e de janela, o aplicativo pode simplesmente chamar [**IDXGISwapChain:: Setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI redimensiona o buffer frontal para corresponder ao modo de tela inteira selecionado recentemente e envia uma \_ mensagem de tamanho do WM para o aplicativo. O aplicativo novamente chama **ResizeBuffers**, assim como faria se a borda da janela fosse arrastada.

A metodologia da explicação anterior segue um caminho muito específico. DXGI definiu a resolução de tela inteira para a resolução de desktop por padrão. No entanto, muitos aplicativos mudam para uma resolução de tela inteira preferida. Nesse caso, DXGI fornece [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Isso deve ser chamado antes de chamar [**Setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). Embora esses métodos possam ser chamados na ordem **oposta (primeiro** , seguido por **ResizeTarget**), fazer isso faz com que uma mensagem de tamanho extra \_ do WM seja enviada ao aplicativo. (Fazer isso também pode causar oscilação, já que DXGI pode ser forçado a executar duas alterações no modo.) Depois de chamar **Setfullscreenstate**, é aconselhável chamar **ResizeTarget** novamente com o membro **Taxa_de_Atualização** do [**\_ modo dxgi \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) . Isso resulta em uma instrução de não operação em DXGI, mas pode evitar problemas com a taxa de atualização, que são discutidas a seguir.

Quando estiver no modo de tela inteira, o Gerenciador de Janelas da Área de Trabalho (DWM) será desabilitado. DXGI pode executar uma inversão para apresentar o conteúdo do buffer de fundo em vez de fazer um blit, o que faria no modo de janela. Esse lucro de desempenho pode ser desfeito, no entanto, se determinados requisitos não forem atendidos. Para garantir que DXGI faça uma inversão em vez de um blit, o buffer frontal e o buffer de fundo devem ser dimensionados de forma idêntica. Se o aplicativo manipula corretamente suas mensagens de tamanho do WM \_ , isso não deve ser um problema. Além disso, os formatos devem ser idênticos.

O problema para a maioria dos aplicativos é a taxa de atualização. A taxa de atualização especificada na chamada para [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) deve ser uma taxa de atualização que é enumerada pelo objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que a cadeia de permuta está usando. DXGI pode calcular esse valor automaticamente se o aplicativo zerar o membro **Taxa_de_Atualização** do [**modo dxgi \_ \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) que é passado para **ResizeTarget**. É importante não supor que certas taxas de atualização sempre terão suporte e simplesmente embutir um valor em código. Geralmente, os desenvolvedores escolhem 60 Hz como a taxa de atualização, não sabendo que a taxa de atualização enumerada do monitor é de aproximadamente 60.000/1.001 Hz do monitor. Se a taxa de atualização não corresponder à taxa de atualização esperada de 60, DXGI será forçado a executar um blit no modo de tela inteira em vez de uma inversão.

O último problema que os desenvolvedores enfrentam com freqüência é como alterar as resoluções de tela inteira enquanto permanecem no modo de tela inteira. A chamada de [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) e [**setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) às vezes é bem sucedido, mas a resolução de tela inteira permanece na resolução da área de trabalho. Além disso, os desenvolvedores podem criar uma cadeia de troca de tela inteira e fornecer uma resolução específica, apenas para descobrir que o DXGI usa como padrão a resolução da área de trabalho, independentemente dos números passados. Salvo indicação em contrário, o DXGI usa como padrão a resolução da área de trabalho para cadeias de troca de tela inteira. Ao criar uma cadeia de troca de tela inteira, o membro **flags** da [**estrutura \_ \_ \_ desc da cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) deve ser definido como o sinalizador de cadeia de permuta de [**dxgi \_ \_ \_ \_ \_ \_ alternar**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) para o comportamento padrão de dxgi. Esse sinalizador também pode ser passado para **ResizeTarget** para habilitar ou desabilitar essa funcionalidade dinamicamente.

## <a name="multiple-monitors"></a>Vários monitores

Ao usar DXGI com vários monitores, há duas regras a serem seguidas.

A primeira regra se aplica à criação de duas ou mais cadeias de permuta de tela inteira em vários monitores. Ao criar essas cadeias de troca, é melhor criar todas as cadeias de permuta como janelas e, em seguida, defini-las como tela inteira. Se as cadeias de permuta forem criadas no modo de tela inteira, a criação de uma segunda cadeia de permuta fará com que uma alteração de modo seja enviada para a primeira cadeia de permuta, o que poderia causar o encerramento do modo de tela inteira.

A segunda regra se aplica a saídas. Ser olhar de saídas usadas ao criar cadeias de permuta. Com DXGI, o objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controla qual monitor a cadeia de permuta usa ao se tornar uma tela inteira. Ao contrário de DXGI, o Direct3D 9 não tinha nenhum conceito de saídas.

## <a name="window-styles-and-dxgi"></a>Estilos de janela e DXGI

Os aplicativos do Direct3D 9 tinham muito trabalho a fazer ao alternar entre os modos de tela inteira e de janela. Grande parte desse trabalho envolvia a alteração de estilos de janela para adicionar e remover bordas, adicionar barras de rolagem e assim por diante. Quando os aplicativos são portados para DXGI e Direct3D 10. x ou Direct3D 11. x, esse código geralmente é deixado em vigor. Dependendo das alterações que estão sendo feitas, alternar entre os modos pode causar um comportamento inesperado. Por exemplo, ao alternar para o modo de janela, o aplicativo pode não ter mais um quadro de janela ou uma borda de janela apesar de ter um código que defina especificamente esses estilos. Isso ocorre porque DXGI agora lida com grande parte dessa alteração de estilo por conta própria. A configuração manual de estilos de janela pode interferir com DXGI, e isso pode causar um comportamento inesperado.

O comportamento recomendado é fazer o menor trabalho possível e permitir que DXGI manipule a maior parte da interação com as janelas. No entanto, se o aplicativo precisar tratar seu próprio comportamento de janela, [**IDXGIFactory:: MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) poderá ser usado para informar ao dxgi para desabilitar parte de seu manuseio automático de janela.

## <a name="multithreading-and-dxgi"></a>Multithread e DXGI

Deve-se ter um cuidado especial ao usar a DXGI em um aplicativo multithread para garantir que não ocorram deadlocks. Devido à interação de fechamento de DXGI com janelas, ele ocasionalmente envia mensagens de janela para a janela do aplicativo associado. DXGI precisa que as alterações na janela ocorram antes que ela possa continuar, portanto, usará [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que é uma chamada síncrona. O aplicativo deve processar a mensagem de janela antes de **SendMessage** retornar.

Em um aplicativo em que as chamadas DXGI e a bomba de mensagens estão no mesmo thread (ou em um aplicativo de thread único), poucas precisam ser feitas. Quando a chamada DXGI está no mesmo thread que a bomba de mensagem, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) chama o [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))da janela. Isso ignora a bomba de mensagem e permite que a execução continue após a chamada para **SendMessage**. Lembre-se de que chamadas [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) , como [**IDXGISwapChain::P reenviada**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), também são consideradas chamadas dxgi; DXGI pode adiar o trabalho de [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) ou [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) até que **Present** seja chamado.

Se a chamada DXGI e a bomba de mensagem estiverem em threads diferentes, deve-se ter cuidado para evitar deadlocks. Quando o bombeamento e o SendMessage da mensagem estiverem em threads diferentes, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) adicionará uma mensagem à fila de mensagens da janela e aguardará que a janela processe a mensagem. Se o procedimento de janela estiver ocupado ou não for chamado pela bomba de mensagem, a mensagem poderá nunca ser processada e DXGI aguardará indefinidamente.

Por exemplo, se um aplicativo que tem seu bombeamento de mensagem em um thread e seu processamento em outro, talvez queira alterar os modos. O thread de bombeamento de mensagens informa o thread de renderização para alterar os modos e aguarda até que a alteração do modo seja concluída. No entanto, o thread de renderização chama funções DXGI que, por sua vez, chamam [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que é bloqueado até que a bomba de mensagem processe a mensagem. Um deadlock ocorre porque os dois threads agora são bloqueados e estão aguardando uns aos outros. Para evitar isso, nunca bloqueie a bomba da mensagem. Se um bloco for inevitável, toda a interação de DXGI deverá ocorrer no mesmo thread que a bomba de mensagem.

## <a name="gamma-and-dxgi"></a>Gama e DXGI

Embora o gama possa ser tratado melhor no Direct3D 10. x ou no Direct3D 11. x usando texturas SRGB, a rampa de gama ainda pode ser útil para os desenvolvedores que desejam um valor de gama diferente de 2,2 ou que estejam usando um formato de destino de renderização que não ofereça suporte a SRGB. Esteja ciente de dois problemas ao definir a rampa de gama por meio de DXGI. O primeiro problema é que os valores de Rampes passados para [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) são valores float, não valores de **palavra** . Além disso, certifique-se de que o código portado do Direct3D 9 não tente converter em valores de palavras antes de passá **-** los para **SetGammaControl**.

O segundo problema é que, depois de alterar para o modo de tela inteira, [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) pode não parecer funcionar, dependendo do objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que está sendo usado. Ao mudar para o modo de tela inteira, DXGI cria um novo objeto de saída e usa o objeto para todas as operações subsequentes na saída. Se chamar **SetGammaControl** em uma saída que é enumerada antes de uma opção de modo de tela inteira, a chamada não será direcionada para a saída que dxgi está usando no momento. Para evitar isso, chame [**IDXGISwapChain:: GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) para obter a saída atual e, em seguida, chame **SetGammaControl** dessa saída para obter o comportamento correto.

Para obter informações sobre como usar a correção gama, consulte [usando a correção gama](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1,1

O tempo de execução do Direct3D 11 incluído no Windows 7 e instalado no Windows Vista (consulte [KB971644](https://support.microsoft.com/kb/971644)) inclui a versão 1,1 do dxgi. Essa atualização adiciona definições para vários formatos novos (particularmente BGRA, tendência de X2 de 10 bits e compactação de textura BC6H e BC7 do Direct3D 11), bem como uma nova versão da fábrica de DXGI e interfaces de adaptador ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) para enumerar conexões de área de trabalho remota.

Quando você usa o Direct3D 11, o tempo de execução usará DXGI 1,1 por padrão ao chamar [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) com um ponteiro [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) nulo. Não há suporte para a combinação do uso de DXGI 1,0 e DXGI 1,1 no mesmo processo. A combinação de instâncias de objeto DXGI de fábricas diferentes no mesmo processo também não é suportada. Portanto, quando você usa o DirectX 11, qualquer uso explícito das interfaces DXGI usa um [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) criado pelo ponto de entrada [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) em "DXGI.DLL" para garantir que o aplicativo esteja sempre usando dxgi 1,1.

## <a name="dxgi-12"></a>DXGI 1,2

O tempo de execução do Direct3D 11,1 que está incluído no Windows 8 também inclui a versão 1,2 do DXGI.

DXGI 1,2 habilita estes recursos:

-   renderização de estéreo
-   16 formatos de bit por pixel

    -   O formato DXGI \_ \_ B5G6R5 \_ UNORM e \_ dxgi \_ B5G5R5A1 \_ UNORM agora são totalmente suportados
    -   um novo formato \_ dxgi \_ B5G5R5A1 \_ UNORM foi adicionado

-   formatos de vídeo
-   novas interfaces DXGI

Para obter mais informações sobre os recursos do DXGI 1,2, consulte [melhorias do dxgi 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 