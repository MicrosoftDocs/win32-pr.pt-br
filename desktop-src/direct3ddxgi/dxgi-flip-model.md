---
description: O Windows 8 adiciona suporte para o modelo de apresentação de flip e suas estatísticas atuais associadas no DXGI 1,2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modelo de flip DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825824"
---
# <a name="dxgi-flip-model"></a>Modelo de flip DXGI

O Windows 8 adiciona suporte para o modelo de apresentação de flip e suas estatísticas atuais associadas no DXGI 1,2. O modelo de apresentação de inversão DXGI do Windows 8 é semelhante à [apresentação do modo de inversão do Direct3D 9EX](../direct3darticles/direct3d-9ex-improvements.md)do Windows 7. Aplicativos de apresentação baseados em taxas de vídeo ou quadros, como jogos, podem se beneficiar mais usando o modelo de apresentação de flip. Os aplicativos que usam o modelo de apresentação de flip DXGI reduzem a carga de recursos do sistema e aumentam o desempenho. Os aplicativos também podem usar os aprimoramentos de estatísticas atuais com o modelo de apresentação de inversão para controlar melhor a taxa de apresentação, fornecendo comentários em tempo real e mecanismos de correção.

-   [Comparando o modelo de inversão DXGI e o modelo BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Como usar o modelo de flip DXGI](#how-to-use-dxgi-flip-model)
-   [Sincronização de quadros de aplicativos de modelo de flip-DXGI](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Evitando, detectando e recuperando de falhas](#avoiding-detecting-and-recovering-from-glitches)
-   [Tópicos relacionados](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Comparando o modelo de inversão DXGI e o modelo BitBlt

O tempo de execução usa a BitBlt (transferência de bloco de bits) e os modelos de apresentação de flip para apresentar conteúdo gráfico em monitores de exibição. A maior diferença entre os modelos de apresentação BitBlt e flip é como o conteúdo de back-buffer chega ao DWM do Windows 8 para composição. No modelo BitBlt, o conteúdo do buffer de fundo é copiado para a superfície de redirecionamento em cada chamada para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). No modelo inverter, todos os buffers de fundo são compartilhados com o Gerenciador de Janelas da Área de Trabalho (DWM). Portanto, o DWM pode compor diretamente dos buffers de fundo sem nenhuma operação de cópia adicional. Em geral, o modelo de inversão é mais eficiente. O modelo de inversão também fornece mais recursos, como as estatísticas presentes aprimoradas.

Se você tiver componentes herdados que usam o Windows Graphics Device Interface (GDI) para gravar em um [**HWND**](../winprog/windows-data-types.md) diretamente, use o modelo BitBlt.

As melhorias de desempenho do modelo de inversão DXGI são significativas quando o aplicativo está no modo de janela. A sequência nesta tabela e a ilustração comparam os usos de largura de banda da memória e as leituras do sistema e as gravações de aplicativos em janelas que escolhem o modelo de flip versus o modelo BitBlt.



| Etapa | Modelo BitBlt presente para DWM                                                                               | Modelo de flip DXGI presente para DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | O aplicativo atualiza seu quadro (gravação)<br/>                                                              | O aplicativo atualiza seu quadro (gravação)<br/>                     |
| 2.   | O Direct3D Runtime copia o conteúdo da superfície para uma superfície de redirecionamento de DWM (leitura, gravação)<br/>            | O tempo de execução do Direct3D passa a superfície do aplicativo para o DWM<br/>        |
| 3.   | Após a conclusão da cópia de superfície compartilhada, o DWM renderiza a superfície do aplicativo na tela (leitura, gravação)<br/> | O DWM renderiza a superfície do aplicativo na tela (leitura, gravação)<br/> |



 

![ilustração de uma comparação do modelo BLT e do flip Model](images/blt-flip-mode-present.png)

O flip Model reduz o uso de memória do sistema, reduzindo o número de leituras e gravações pelo tempo de execução do Direct3D para a composição de quadro em janela pelo DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Como usar o modelo de flip DXGI

Os aplicativos do Direct3D 11,1 destinados ao Windows 8 usam o flip Model criando a cadeia de permuta com o [**efeito de permuta de dxgi \_ \_ \_ inverter \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) valor de enumeração sequencial definido no membro **SwapEffect** da estrutura [**\_ DESC1 da \_ cadeia \_ de permuta dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) . Quando você define **SwapEffect** para o **efeito de permuta de dxgi \_ \_ \_ inverter \_ sequencial**, também define esses membros da **cadeia de permuta dxgi \_ \_ \_ DESC1** com os valores indicados:

-   **BufferCount** a um valor entre 2 e 16 para evitar uma penalidade de desempenho como resultado da espera do DWM para liberar o buffer de apresentação anterior.
-   **Formato** para o \_ formato dxgi \_ R16G16B16A16 \_ float, \_ formato dxgi \_ B8G8R8A8 \_ UNORM ou formato dxgi \_ \_ R8G8B8A8 \_ UNORM
-   **Contagem** de membros da [**estrutura \_ \_ desc de exemplo de dxgi**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) que o membro **SampleDesc** especifica para um e o membro de **qualidade** do **\_ exemplo \_ desc de dxgi** a zero porque não há suporte para a MSAA (várias amostras de anti-aliasing)

Se você usar [**o \_ efeito de permuta dxgi \_ \_ inverter \_ sequencialmente**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) no sistema operacional Windows 7 ou anterior, a criação do dispositivo falhará. Ao usar o flip Model, você pode usar as estatísticas de apresentação em tela inteira no modo de janela. O comportamento de tela inteira não é afetado. Se você passar **NULL** para o parâmetro *pFullscreenDesc* de [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) para uma cadeia de permuta em janela e definir **SwapEffect** como efeito de permuta de **dxgi, \_ \_ \_ inverter \_ sequencialmente**, o tempo de execução criará um buffer de fundo extra e girará qualquer identificador que pertença ao buffer que se torna o buffer frontal no momento da apresentação.

Ao usar o flip Model, considere estas dicas:

-   Use uma cadeia de permuta de modelo de flip por [**HWND**](../winprog/windows-data-types.md). Não direcione vários cadeias de permuta de modelo de flip para o mesmo **HWND**.
-   Não use a cadeia de permuta de modelo de flip com a função [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) ou [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) da GDI. Alguns aplicativos do Direct3D usam as funções **ScrollWindow** e **ScrollWindowEx** da GDI para atualizar o conteúdo da janela após a ocorrência de um evento de rolagem do usuário. **ScrollWindow** e **ScrollWindowEx** executam bitblts de conteúdo da janela na tela enquanto o usuário rola uma janela. Essas funções também exigem atualizações de modelo BitBlt para conteúdo GDI e Direct3D. Os aplicativos que usam qualquer função não exibirão, necessariamente, a rolagem do conteúdo da janela visível na tela quando o aplicativo estiver no modo de janela. Recomendamos que você não use as funções **ScrollWindow** e **ScrollWindowEx** da GDI e, em vez disso, Redesenhe o conteúdo GDI e Direct3D na tela em resposta à rolagem.
-   Use o flip Model em um [**HWND**](../winprog/windows-data-types.md) que não é também direcionado por outras APIs, incluindo o modelo de apresentação dxgi BitBlt, outras versões do Direct3D ou GDI. Como o modelo BitBlt mantém uma cópia adicional da superfície, você pode adicionar o GDI e outros conteúdos do Direct3D ao mesmo **HWND** por meio de atualizações por etapas do Direct3D e GDI. Quando você usa o modelo inverter, somente o conteúdo do Direct3D no flip Model troca cadeias que o tempo de execução passa para o DWM é visível. O tempo de execução ignora todas as outras atualizações de conteúdo do modelo BitBlt Direct3D ou GDI.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronização de quadros de aplicativos de modelo de flip-DXGI

As estatísticas atuais são informações de tempo de quadro que os aplicativos de mídia usam para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo. Os aplicativos podem usar as informações de tempo de quadro em atuais estatísticas para ajustar a taxa de apresentação de seus quadros de vídeo para uma apresentação mais suave. Para obter informações sobre estatísticas presentes, chame o método [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) para obter a estrutura de [**\_ \_ estatísticas do quadro dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . **Dxgi \_ As \_ Estatísticas de quadro** contêm estatísticas sobre chamadas [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Uma cadeia de permuta do flip Model fornece informações de estatísticas presentes nos modos de tela inteira e em janelas. Para cadeias de troca de modelo BitBlt no modo de janela, todos os valores de **\_ \_ Estatísticas de quadro dxgi** são zeros.

Para estatísticas presentes do modelo de flip, [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) retorna **\_ Estatísticas de quadro de erro \_ \_ \_ dxgi** nessas situações:

-   Primeira chamada para [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics), que indica o início de uma sequência
-   Alteração de modo: qualquer modo de janela para ou de tela inteira ou tela inteira para transições de tela inteira

Os valores nos membros **PresentRefreshCount**, **SyncRefreshCount** e **SyncQPCTime** das [**\_ \_ Estatísticas de quadro dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) têm as seguintes características:

-   **PresentRefreshCount** é igual a **SyncRefreshCount** quando o aplicativo apresenta em cada vsync.
-   **SyncRefreshCount** é obtido no intervalo de vsync quando o presente foi enviado, **SyncQPCTime** é aproximadamente o tempo associado ao intervalo de vsync.

O método [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) retorna a última contagem presente, ou seja, a ID atual da última IDXGISwapChain1 bem-sucedida [**::P**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) chamada de resent1 feita por um dispositivo de vídeo associado à cadeia de permuta. Essa ID atual é o valor do membro **PresentCount** da estrutura de [**\_ \_ estatísticas do quadro dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . Para cadeias de troca de modelo BitBlt, no modo de janela, todos os valores de **\_ \_ Estatísticas de quadro dxgi** são zeros.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Evitando, detectando e recuperando de falhas

Execute estas etapas para evitar, detectar e recuperar-se de falhas na apresentação de quadros:

1.  IDXGISwapChain1 da fila: chamadas de [**resent1 de:P**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (ou seja, chamada **IDXGISwapChain1::P resent1** várias vezes, o que faz com que elas sejam coletadas em uma fila).
2.  Crie uma estrutura de fila atual para armazenar todos os IDXGISwapChain1 enviados com êxito [**::P**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)a ID atual do resent1 (retornada por [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) e valores de **PresentRefreshCount** associados, calculados/esperados.
3.  Para detectar uma falha:

    -   Chame [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Para esse quadro, obtenha a ID atual (**PresentCount**) e a contagem de vsync em que o sistema operacional apresentou a última imagem ao monitor (**PresentRefreshCount**).
    -   Recupere o **PresentRefreshCount** esperado que está associado à ID atual e que você armazenou anteriormente na estrutura de fila atual.
    -   Se o **PresentRefreshCount** real for posterior ao esperado **PresentRefreshCount**, ocorrerá uma falha.

4.  Para se recuperar do problema:

    -   Calcule o número de quadros a serem ignorados para a recuperação da falha. Por exemplo, se a etapa 3 revelar que a contagem vsync esperada (**PresentRefreshCount**) para uma ID presente (**PresentCount**) é 5 e a contagem vsync real para a ID atual for 8, o número de quadros a serem ignorados para recuperação da falha será de 3 quadros.
    -   Passe 0 para o parâmetro *SyncInterval* neste número de chamadas para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para descartar e ignorar esse número de quadros.

        > [!Note]  
        > Se o problema consistir em um grande número de quadros, chame [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) com o parâmetro *flags* definido como [**dxgi \_ presente \_ Restart**](dxgi-present.md) para descartar e ignorar todos os presentes enfileirados pendentes.

         

Aqui está um cenário de exemplo de recuperação de falhas na apresentação de quadros:

![ilustração de um cenário de exemplo de recuperação de falhas na apresentação de quadros](images/frame-sync-glitch-recover.png)

No cenário de exemplo, você espera que o quadro A passe na tela em uma contagem de vsync de 1. Mas, na verdade, você detecta a contagem de vsync que o quadro A aparece na tela como 4. Portanto, você determina que ocorreu uma falha. Em seguida, você pode descartar 3 quadros, ou seja, você pode passar 0 para o parâmetro *SyncInterval* em 3 chamadas para [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). No cenário de exemplo anterior, para se recuperar da falha, você precisa de um total de 8 **IDXGISwapChain1:** chamadas de resent1 de:P. Em seguida, o nono quadro é visível de acordo com a contagem de vsync esperada.

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

 

 
