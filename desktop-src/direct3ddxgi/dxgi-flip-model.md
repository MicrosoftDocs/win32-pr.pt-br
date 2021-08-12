---
description: Windows 8 adiciona suporte para o modelo de apresentação in flip e suas estatísticas presentes associadas no DXGI 1.2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modelo de in flip do DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b4b4cf8f792a23d4d32e5cb4b4273594745283cb803a638ea3d0cf4c45977f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289426"
---
# <a name="dxgi-flip-model"></a>Modelo de in flip do DXGI

Windows 8 adiciona suporte para o modelo de apresentação in flip e suas estatísticas presentes associadas no DXGI 1.2. Windows 8 modelo de apresentação de flip do DXGI é semelhante Windows apresentação do modo de in flip do [Direct3D 9EX do 7.](../direct3darticles/direct3d-9ex-improvements.md) Aplicativos de apresentação baseados em taxa de quadros ou vídeo, como jogos, podem se beneficiar mais usando o modelo de apresentação in flip. Os aplicativos que usam o modelo de apresentação de invasão DXGI reduzem a carga de recursos do sistema e aumentam o desempenho. Os aplicativos também podem usar aprimoramentos de estatísticas atuais com o modelo de apresentação de invasões para controlar melhor a taxa de apresentação fornecendo mecanismos de correção e comentários em tempo real.

-   [Comparando o modelo de in flip do DXGI e o modelo BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Como usar o modelo de in flip do DXGI](#how-to-use-dxgi-flip-model)
-   [Sincronização de quadros de aplicativos de modelo de invasão DXGI](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Evitando, detectando e recuperando de falhas](#avoiding-detecting-and-recovering-from-glitches)
-   [Tópicos relacionados](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Comparando o modelo de in flip do DXGI e o modelo BitBlt

O runtime usa os modelos de transferência de bloco de bits (bitblt) e inverter a apresentação para apresentar conteúdo gráfico em monitores de exibição. A maior diferença entre modelos de apresentação bitblt e flip é como o conteúdo do buffer de back-buffer é direcionado Windows 8 DWM para composição. No modelo bitblt, o conteúdo do buffer de fundo é copiado para a superfície de redirecionamento em cada chamada para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). No modelo de invasão, todos os buffers de fundo são compartilhados com o Gerenciador de Janelas da Área de Trabalho (DWM). Portanto, o DWM pode compor diretamente desses buffers de fundo sem nenhuma operação de cópia adicional. Em geral, o modelo de in flip é mais eficiente. O modelo de in flip também fornece mais recursos, como estatísticas atuais aprimoradas.

Se você tiver componentes herdados que usam Windows Graphics Device Interface (GDI) para gravar em um [**HWND**](../winprog/windows-data-types.md) diretamente, use o modelo bitblt.

As melhorias de desempenho do modelo de in flip do DXGI são significativas quando o aplicativo está no modo em janelas. A sequência nesta tabela e a ilustração comparam os usos de largura de banda de memória e as leituras e gravações do sistema de aplicativos em janelas que escolhem inverter modelo versus o modelo bitblt.



| Etapa | Modelo BitBlt presente no DWM                                                                               | Modelo de in flip do DXGI presente no DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | O aplicativo atualiza seu quadro (Gravação)<br/>                                                              | O aplicativo atualiza seu quadro (Gravação)<br/>                     |
| 2.   | O runtime do Direct3D copia o conteúdo da superfície para uma superfície de redirecionamento DWM (Leitura, Gravação)<br/>            | O runtime do Direct3D passa a superfície do aplicativo para o DWM<br/>        |
| 3.   | Depois que a cópia da superfície compartilhada é concluída, a DWM renderiza a superfície do aplicativo na tela (Leitura, Gravação)<br/> | A DWM renderiza a superfície do aplicativo na tela (Leitura, Gravação)<br/> |



 

![ilustração de uma comparação do modelo blt e do modelo de invasão](images/blt-flip-mode-present.png)

O modelo de inatividade reduz o uso de memória do sistema reduzindo o número de leituras e gravações pelo runtime do Direct3D para a composição de quadro em janela pela DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Como usar o modelo de in flip do DXGI

Os aplicativos Direct3D 11.1 destinados Windows 8 usam o modelo de invasão criando a cadeia de permuta com o valor de enumeração FLIP [**\_ \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) DE EFEITO SWAP DXGI definido no membro **SwapEffect** da estrutura [**DXGI \_ SWAP CHAIN \_ \_ DESC1.**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Quando você definir **SwapEffect** como **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL,** também de definir esses membros de **DXGI \_ SWAP CHAIN \_ \_ DESC1** para os valores indicados:

-   **BufferCount** para um valor entre 2 e 16 para evitar uma penalidade de desempenho como resultado da espera da DWM para liberar o buffer de apresentação anterior.
-   **Formatar** para FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT, FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM ou FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM
-   **Contar** membro da estrutura [**\_ DXGI SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) que o membro **SampleDesc** especifica como um e o membro **Quality** do **\_ DXGI SAMPLE \_ DESC** como zero porque não há suporte para várias MSAA (antialiasing de exemplo)

Se você usar [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Windows sistema operacional 7 ou anterior, a criação do dispositivo falhará. Ao usar o modelo de invasões, você pode usar estatísticas de apresentação de tela inteira no modo de janela. O comportamento de tela inteira não é afetado. Se você passar **NULL** para o parâmetro *pFullscreenDesc* [**de IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) para uma cadeia de permuta em janelas e definir **SwapEffect** como **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL,** o runtime criará um buffer de back extra e girará qualquer alça que pertence ao buffer que se torna o buffer frontal no momento da apresentação.

Ao usar o modelo de in flip, considere estas dicas:

-   Use uma cadeia de permuta de modelo in flip por [**HWND.**](../winprog/windows-data-types.md) Não direcionar várias cadeias de troca de modelo de invasão para o **mesmo HWND.**
-   Não use a cadeia de permuta de modelo flip com a [**função ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) ou [**ScrollWindowEx da**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) GDI. Alguns aplicativos Direct3D usam as funções **ScrollWindow** e **ScrollWindowEx** da GDI para atualizar o conteúdo da janela depois que um evento de rolagem do usuário ocorre. **ScrollWindow** e **ScrollWindowEx** executam bitblts do conteúdo da janela na tela à medida que o usuário rola uma janela. Essas funções também exigem atualizações de modelo bitblt para conteúdo GDI e Direct3D. Os aplicativos que usam uma das funções não exibirão necessariamente o conteúdo visível da janela que rola na tela quando o aplicativo estiver no modo de janela. Recomendamos que você não use as funções **ScrollWindow** e **ScrollWindowEx** da GDI e, em vez disso, redesenhar o conteúdo GDI e Direct3D na tela em resposta à rolagem.
-   Use o modelo de inversões em um [**HWND**](../winprog/windows-data-types.md) que também não seja direcionado por outras APIs, incluindo o modelo de apresentação de bitblt DXGI, outras versões do Direct3D ou GDI. Como o modelo bitblt mantém uma cópia adicional da superfície, você pode adicionar GDI e outros conteúdos do Direct3D ao mesmo **HWND** por meio de atualizações por etapa do Direct3D e GDI. Quando você usa o modelo de inatividade, somente o conteúdo do Direct3D em cadeias de troca de modelo in flip que o runtime passa para a DWM ficam visíveis. O runtime ignora todas as outras atualizações de conteúdo do Direct3D ou GDI do modelo bitblt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronização de quadros de aplicativos de modelo de invasão DXGI

As estatísticas presentes são informações de tempo de quadros que os aplicativos de mídia usam para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo. Os aplicativos podem usar as informações de tempo de quadros nas estatísticas atuais para ajustar a taxa de apresentação de seus quadros de vídeo para uma apresentação mais suave. Para obter informações de estatísticas presentes, chame o método [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) para obter a [**estrutura DXGI \_ FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) **DXGI \_ FRAME \_ STATISTICS** contém estatísticas sobre [**chamadas IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Uma cadeia de troca de modelo de invasões fornece informações de estatísticas presentes nos modos de tela inteira e janela. Para cadeias de permuta de modelo bitblt no modo de janela, todos os valores de ESTATÍSTICAS DE **\_ QUADROS \_ DXGI** são zeros.

Para ver as estatísticas presentes no modelo flip, [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) retorna **\_ \_ \_ \_ DISJOINT** DE ESTATÍSTICAS DE QUADRO DE ERRO DO DXGI nessas situações:

-   Primeira chamada para [**GetFrameStatistics,**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)que indica o início de uma sequência
-   Alteração de modo: o modo em janelas para ou de tela inteira ou tela inteira para transições de tela inteira

Os valores **em PresentRefreshCount,** **SyncRefreshCount** e **syncQPCTime** membros de [**DXGI \_ FRAME \_ STATISTICS**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) têm as seguintes características:

-   **PresentRefreshCount é** igual a **SyncRefreshCount** quando o aplicativo é presente em cada vsync.
-   **SyncRefreshCount** é obtido no intervalo vsync quando o presente foi enviado, **SyncQPCTime** é aproximadamente o tempo associado ao intervalo vsync.

O método [**IDXGISwapChain::GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) retorna a última contagem atual, ou seja, a ID atual da última chamada bem-sucedida [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) feita por um dispositivo de exibição associado à cadeia de permuta. Essa ID atual é o valor do **membro PresentCount** da [**estrutura DXGI \_ FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) Para cadeias de permuta de modelo bitblt, enquanto no modo de janela, todos os valores de ESTATÍSTICAS DE **\_ QUADROS \_ DXGI** são zeros.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Evitando, detectando e recuperando de falhas

Execute estas etapas para evitar, detectar e recuperar-se de falhas na apresentação do quadro:

1.  Chamadas [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) da fila (ou seja, chame **IDXGISwapChain1::P resent1** várias vezes, o que faz com que eles coletem em uma fila).
2.  Crie uma estrutura de fila atual para armazenar todas as [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)enviadas com êxito da ID atual do (retornada por [**IDXGISwapChain::GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) e valores **presentRefreshCount** associados, calculados/esperados.
3.  Para detectar uma falha:

    -   Chame [**IDXGISwapChain::GetFrameStatistics.**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)
    -   Para esse quadro, obter a ID atual (**PresentCount**) e a contagem vsync em que o sistema operacional apresentou a última imagem ao monitor (**PresentRefreshCount**).
    -   Recupere o **PresentRefreshCount** esperado associado à ID atual e que você armazenou anteriormente na estrutura da fila atual.
    -   Se o **PresentRefreshCount real** for posterior ao **esperado de PresentRefreshCount,** ocorrerá uma falha.

4.  Para se recuperar da falha:

    -   Calcule o número de quadros a ignorar para se recuperar da falha. Por exemplo, se a etapa 3 revelar que a contagem de vsync esperada (**PresentRefreshCount**) para uma ID atual (**PresentCount**) será 5 e a contagem real de vsync para a ID atual for 8, o número de quadros a ignorar para se recuperar da falha será de 3 quadros.
    -   Passe 0 para o parâmetro *SyncInterval* nesse número de chamadas para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para descartar e ignorar esse número de quadros.

        > [!Note]  
        > Se a falha consistir em um grande número de quadros, chame [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) com o parâmetro Flags definido como [**DXGI \_ PRESENT \_ RESTART**](dxgi-present.md) para descartar e ignorar todos os presentes na fila *pendentes.*

         

Aqui está um cenário de exemplo de recuperação de falhas na apresentação do quadro:

![ilustração de um cenário de exemplo de recuperação de falhas na apresentação do quadro](images/frame-sync-glitch-recover.png)

No cenário de exemplo, você espera que o quadro A vá para a tela em uma contagem vsync de 1. Mas, na verdade, você detecta a contagem vsync que o quadro A aparece na tela como 4. Portanto, você determina que ocorreu uma falha. Em seguida, você pode descartar três quadros, ou seja, você pode passar 0 para o parâmetro *SyncInterval* em três chamadas para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). No cenário de exemplo anterior, para se recuperar da falha, você precisa de um total de 8 chamadas **IDXGISwapChain1::P resent1.** O 9º quadro fica visível de acordo com a contagem vsync esperada.

Aqui está uma linha de tempo de eventos de apresentação. Cada linha vertical representa um vsync. A direção horizontal é time, que aumenta à direita. Você pode usar a figura para imaginar como os problemas podem ocorrer.

![ilustração de uma linha de tempo de eventos de apresentação](images/present-timeline.png)

A figura ilustra esta sequência:

1.  O aplicativo é ativado em vsync, renderiza azul, chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e, em seguida, volta para o estado de suspensão.
2.  A GPU (unidade de processamento gráfico) é ativada de ocioso, executa o processamento em azul e, em seguida, volta para o estado de suspensão.
3.  O DWM é ativado no próximo vsync, compõe o azul em seu buffer de fundo, chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e, em seguida, volta para o estado de suspensão.
4.  O aplicativo é ativado, renderiza verde, chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e, em seguida, volta para o estado de suspensão.
    > [!Note]  
    > O aplicativo é executado simultaneamente enquanto a GPU executa a composição de azul.

     

5.  Em seguida, a GPU renderiza verde para o aplicativo.
6.  Por fim, o conversor de digital para analógico (DAC) mostra os resultados da composição do DWM no monitor no próximo vsync.

Na linha de tempo, você pode imaginar a latência de atuais estatísticas e como os problemas podem ocorrer. Por exemplo, para mostrar uma falha do DWM para a cor verde que aparece na tela, imagine alargar a caixa verde/vermelha para que o lado direito da caixa verde/vermelha corresponda ao lado direito da caixa roxo/vermelho. Nesse cenário, o DAC mostra dois quadros de azul e, em seguida, o quadro verde. Você pode ver que esse problema ocorreu na leitura de estatísticas presentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimorando a apresentação com o modelo de flip, retângulos sujos e áreas roladas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
