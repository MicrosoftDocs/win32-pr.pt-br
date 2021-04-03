---
description: Este tópico descreve como escrever um processador de vídeo personalizado para o DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Renderizadores de vídeo alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646094"
---
# <a name="alternative-video-renderers"></a>Renderizadores de vídeo alternativos

Este tópico descreve como escrever um processador de vídeo personalizado para o DirectShow.

> [!Note]  
> Em vez de escrever um processador de vídeo personalizado, é recomendável que você escreva um apresentador de plug-in-Presenter para o processador de mixagem de vídeo (VMR) ou [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR). Essa abordagem fornecerá a você todos os benefícios do VMR/EVR, incluindo suporte para a DXVA (aceleração de vídeo do DirectX), desentrelaçamento de hardware e revisão de quadros, e provavelmente será mais robusta do que um processador de vídeo personalizado. Para mais informações, consulte os seguintes tópicos:
>
> -   [Modo de reprodução do VMR (alocador personalizado-apresentadores)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Como escrever um apresentador EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Escrevendo um renderizador alternativo

O Microsoft DirectShow fornece um processador de vídeo baseado em janela; Ele também fornece um processador de tela inteira na instalação em tempo de execução. Você pode usar as classes base do DirectShow para escrever renderizadores de vídeo alternativos. Para que os renderizadores alternativos interajam corretamente com aplicativos baseados no DirectShow, os renderizadores devem aderir às diretrizes descritas neste artigo. Você pode usar as classes [**CBaseRenderer**](cbaserenderer.md) e [**CBaseVideoRenderer**](cbasevideorenderer.md) para ajudar a seguir essas diretrizes ao implementar uma renderização de vídeo alternativa. Devido ao desenvolvimento contínuo do DirectShow, revise sua implementação periodicamente para garantir que os renderizadores sejam compatíveis com a versão mais recente do DirectShow.

Este tópico discute muitas notificações que um renderizador é responsável pelo manuseio. Uma breve revisão das notificações do DirectShow pode ajudar a definir o estágio. Há basicamente três tipos de notificações que ocorrem no DirectShow:

-   *Notificações de fluxo*, que são eventos que ocorrem no fluxo de mídia e são passados de um filtro para o próximo. Elas podem ser de início-liberação, fim de liberação ou notificações de fim de fluxo e são enviadas chamando o método apropriado no pino de entrada do filtro downstream (por exemplo [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)).
-   *Filtre notificações de grafo*, que são eventos enviados de um filtro para o Gerenciador de gráfico de filtro, como o [**EC \_ Complete**](ec-complete.md). Isso é feito chamando o método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) no Gerenciador do grafo de filtro.
-   *Notificações de aplicativo*, que são recuperadas do Gerenciador de gráfico de filtro pelo aplicativo de controle. Um aplicativo chama o método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) no Gerenciador de gráfico de filtro para recuperar esses eventos. Geralmente, o Gerenciador de gráficos de filtro passa pelos eventos que recebe para o aplicativo.

Este tópico discute a responsabilidade do filtro de renderizador no tratamento de notificações de fluxo que recebe e no envio de notificações de gráfico de filtro apropriadas.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Tratamento de notificações de fim de fluxo e liberação

Uma notificação de fim de fluxo começa em um filtro upstream (como o filtro de origem) quando esse filtro detecta que ele pode não enviar mais dados. Ele é transmitido por cada filtro no grafo e, eventualmente, termina no renderizador, que é responsável por enviar posteriormente uma notificação de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro. Os renderizadores têm responsabilidades especiais quando se trata de lidar com essas notificações.

Um renderizador recebe uma notificação de fim de fluxo quando o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) de seu PIN de entrada é chamado pelo filtro upstream. Um renderizador deve observar essa notificação e continuar a renderizar os dados já recebidos. Depois que todos os dados restantes tiverem sido recebidos, o processador deverá enviar uma notificação de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro. A notificação de **\_ conclusão do EC** deve ser enviada apenas uma vez por um processador sempre que atingir o final de um fluxo. Além disso, as notificações **\_ completas do EC** nunca devem ser enviadas, exceto quando o grafo de filtro estiver em execução. Portanto, se o grafo de filtro for pausado quando um filtro de origem enviar uma notificação de fim de fluxo, o **EC \_ concluído** não deverá ser enviado até que o gráfico de filtro seja finalmente executado.

Todas as chamadas para os métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) após uma notificação de fim de fluxo são sinalizadas devem ser rejeitadas. **E \_ Inesperado** é a mensagem de erro mais apropriada para retornar nesse caso.

Quando um grafo de filtro é interrompido, todas as notificações de fim de fluxo em cache devem ser limpas e não reenviadas quando a próxima for iniciada. Isso ocorre porque o Gerenciador de gráfico de filtro sempre pausa todos os filtros antes de executá-los para que ocorra a liberação correta. Portanto, por exemplo, se o grafo de filtro for pausado e uma notificação de fim de fluxo for recebida e, em seguida, o grafo de filtro for interrompido, o renderizador não deverá enviar uma notificação de [**\_ conclusão do EC**](ec-complete.md) quando for executado posteriormente. Se nenhuma busca tiver ocorrido, o filtro de origem enviará automaticamente outra notificação de fim de fluxo durante o estado de pausa que precede um estado de execução. Se, por outro lado, ocorrer uma busca enquanto o grafo de filtro for interrompido, o filtro de origem poderá ter dados a serem enviados, portanto, não enviará uma notificação de fim de fluxo.

Os renderizadores de vídeo geralmente dependem de notificações de fim de fluxo para mais do que o envio de notificações de [**\_ conclusão do EC**](ec-complete.md) . Por exemplo, se um fluxo tiver terminado a execução (ou seja, uma notificação de fim de fluxo for enviada) e outra janela for arrastada sobre uma janela de processador de vídeo, um número de mensagens da janela de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) será gerado. A prática típica para executar renderizadores de vídeo é evitar a repintura do quadro atual no recebimento de mensagens **de \_ pintura do WM** (com base na suposição de que outro quadro a ser desenhado será recebido). No entanto, quando a notificação de fim de fluxo é enviada, o renderizador está em um estado de espera; Ele ainda está em execução, mas está ciente de que ele não receberá dados adicionais. Sob essas circunstâncias, o processador normalmente desenha a área de reprodução em preto.

A manipulação da liberação é uma complicação adicional para os renderizadores. A liberação é realizada por meio de um par de métodos [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) chamados [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush). A liberação é essencialmente um estado adicional que o renderizador deve manipular. É ilegal para um filtro de origem chamar **BeginFlush** sem chamar **EndFlush**, portanto, espero que o estado seja curto e discreto; no entanto, o renderizador deve manipular corretamente os dados ou as notificações recebidas durante a transição de liberação.

Todos os dados recebidos após chamar [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) devem ser rejeitados imediatamente retornando **S \_ false**. Além disso, qualquer notificação de fim de fluxo em cache também deve ser limpa quando um renderizador é liberado. Um renderizador normalmente será liberado em resposta a uma busca. A liberação garante que os dados antigos sejam apagados do grafo de filtro antes que os novos exemplos sejam enviados. (Normalmente, a execução de duas seções de um fluxo, uma após a outra, é melhor tratada por meio de comandos adiados em vez de esperar que uma seção seja concluída e, em seguida, emitir um comando de busca.)

## <a name="handling-state-changes-and-pause-completion"></a>Manipulando alterações de estado e pausar a conclusão

Um filtro de processador se comporta da mesma forma que qualquer outro filtro no grafo de filtro quando seu estado é alterado, com a seguinte exceção. Depois de ser pausado, o renderizador terá alguns dados em fila, prontos para serem renderizados quando executado subsequentemente. Quando o processador de vídeo é interrompido, ele mantém os dados na fila. Essa é uma exceção à regra do DirectShow de que nenhum recurso deve ser mantido por filtros enquanto o grafo de filtro é interrompido.

A razão para essa exceção é que, ao manter os recursos, o renderizador sempre terá uma imagem com a qual redesenhará a janela se receber uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Ele também tem uma imagem para satisfazer métodos, como [**CBaseControlVideo:: GetStaticImage**](cbasecontrolvideo-getstaticimage.md), que solicita uma cópia da imagem atual. Outro efeito de conter recursos é que a ativação da imagem impede que o alocador seja deconfirmado, o que, por sua vez, faz com que a próxima alteração de estado ocorra muito mais rapidamente porque os buffers de imagem já estão alocados.

Um processador de vídeo deve renderizar e liberar amostras somente durante a execução. Enquanto estiver em pausa, o filtro poderá renderizá-los (por exemplo, ao desenhar uma imagem de pôster estática em uma janela), mas não deverá liberá-las. Os renderizadores de áudio não farão renderização enquanto estiverem em pausa (embora possam executar outras atividades, como preparar o dispositivo wave, por exemplo). A hora em que as amostras devem ser renderizadas é obtida pela combinação do tempo de transmissão no exemplo com o tempo de referência passado como um parâmetro para o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Os renderizadores devem rejeitar amostras com tempos de início menores ou iguais a horários de término.

Quando um aplicativo pausa um gráfico de filtro, o grafo de filtro não retorna de seu método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) até que haja dados na fila nos renderizadores. Para garantir isso, quando um renderizador é pausado, ele deve retornar S \_ false se não houver dados aguardando para serem renderizados. Se ele tiver dados em fila, ele poderá retornar **S \_ OK**.

O Gerenciador de gráfico de filtro verifica todos os valores de retorno ao pausar um gráfico de filtro, para garantir que os renderizadores tenham dados em fila. Se um ou mais filtros não estiverem prontos, o Gerenciador do grafo de filtro sondará os filtros no grafo chamando [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). O método **GetState** usa um parâmetro de tempo limite. Um filtro (normalmente um renderizador) que ainda está aguardando a chegada dos dados antes de concluir a alteração de estado retorna **VFW \_ S \_ State \_ intermediário** se o método **GetState** expirar. Depois que os dados chegam ao renderizador, **GetState** deve ser retornado imediatamente com **S \_ OK**.

No estado intermediário e concluído, o estado de filtro relatado será \_ pausado. Somente o valor de retorno indica se o filtro está realmente pronto ou não. Se, enquanto um renderizador estiver aguardando a chegada de dados, seu filtro de origem enviará uma notificação de fim de fluxo, que também deverá concluir a alteração de estado.

Depois que todos os filtros realmente têm dados aguardando para serem processados, o grafo de filtro concluirá sua alteração no estado de pausa.

## <a name="handling-termination"></a>Tratamento de encerramento

Os renderizadores de vídeo devem lidar corretamente com os eventos de encerramento do usuário. Isso implica ocultar corretamente a janela e saber o que fazer se uma janela for subsequentemente forçada a ser exibida. Além disso, os renderizadores de vídeo devem notificar o Gerenciador do grafo de filtro quando sua janela é destruída (ou mais precisamente, quando o renderizador é removido do gráfico de filtro) para liberar recursos.

Se o usuário fechar a janela de vídeo (por exemplo pressionando ALT + F4), a Convenção será ocultar a janela imediatamente e enviar uma notificação do [**EC \_ userabort**](ec-userabort.md) para o Gerenciador do grafo de filtro. Essa notificação é passada para o aplicativo, o que irá parar a reprodução do grafo. Depois de enviar o **EC \_ userabort**, um processador de vídeo deve rejeitar quaisquer exemplos adicionais entregues a ele.

O sinalizador de grafo parado deve ser deixado pelo renderizador até que seja interrompido posteriormente, ponto em que ele deve ser redefinido para que um aplicativo possa substituir a ação do usuário e continuar jogando o grafo se desejar. Se ALT + F4 for pressionado enquanto o vídeo estiver em execução, a janela ficará oculta e todos os outros exemplos entregues serão rejeitados. Se a janela for mostrada subsequentemente (talvez por meio de [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)), nenhuma notificação de [**\_ redesenho de EC**](ec-repaint.md) deverá ser gerada.

O processador de vídeo também deve enviar a notificação [**\_ \_ destruída da janela do EC**](ec-window-destroyed.md) para o grafo de filtro quando o processador de vídeo está sendo encerrado. Na verdade, é melhor lidar com isso quando o método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do processador é chamado com um parâmetro nulo (indicando que o processador está prestes a ser removido do grafo de filtro), em vez de esperar até que a janela de vídeo real seja destruída. O envio dessa notificação permite que o distribuidor de plug-ins no Gerenciador de gráficos de filtro passe em recursos que dependem do foco da janela para outros filtros, como dispositivos de áudio.

## <a name="handling-dynamic-format-changes"></a>Manipulando alterações de formato dinâmico

Em alguns casos, o filtro upstream do renderizador pode tentar alterar o formato de vídeo durante a reprodução do vídeo. Geralmente, é o descompactador de vídeo que inicia uma alteração de formato dinâmico.

Um filtro upstream que tenta alterar formatos dinamicamente sempre deve chamar o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de entrada do processador. Um processador de vídeo tem algumas reserva para que tipos de alterações de formato dinâmico devem dar suporte. No mínimo, ele deve permitir que o filtro upstream altere as paletas. Quando um filtro upstream altera os tipos de mídia, ele anexa o tipo de mídia ao primeiro exemplo entregue no novo formato. Se o renderizador mantiver amostras em uma fila para renderização, ele não deverá alterar o formato até que ele processe o exemplo com a alteração de tipo.

Um processador de vídeo também pode solicitar uma alteração de formato do decodificador. Por exemplo, ele pode solicitar que o decodificador forneça um formato compatível com o DirectDraw com uma **superaltura** negativa. Quando o renderizador é pausado, ele deve chamar [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino upstream para ver quais formatos o decodificador pode fornecer. O decodificador pode não enumerar todos os tipos que ele pode aceitar, no entanto, portanto, o renderizador deve oferecer alguns tipos, mesmo que o decodificador não os Anuncie.

Se o decodificador puder mudar para o formato solicitado, ele retornará **S \_ OK** de [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). Em seguida, o renderizador anexa o novo tipo de mídia ao exemplo de mídia seguinte no alocador upstream. Para que isso funcione, o renderizador deve fornecer um alocador personalizado que implementa um método particular para anexar o tipo de mídia ao próximo exemplo. (Dentro desse método particular, chame [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para definir o tipo.)

O PIN de entrada do renderizador deve retornar o alocador personalizado do renderizador no método [**IMemInputPin:: Getalocador**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) . Substitua [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para que falhe se o filtro upstream não usar o alocador do processador.

Com alguns decodificadores, a configuração de **biHeight** para um número positivo em tipos YUV faz com que o decodificador desenhe a imagem de cabeça para baixo. (Isso está incorreto e deve ser considerado um bug no decodificador.)

Sempre que uma alteração de formato é detectada pelo processador de vídeo, ele deve enviar uma notificação de [**exibição de EC \_ \_ alterada**](ec-display-changed.md) . A maioria dos renderizadores de vídeo escolhe um formato durante a conexão para que o formato possa ser desenhado com eficiência por meio da GDI. Se o usuário alterar o modo de exibição atual sem reiniciar o computador, um processador poderá se encontrar com uma conexão de formato de imagem inadequada e deverá enviar essa notificação. O primeiro parâmetro deve ser o PIN que precisa ser reconectado. O Gerenciador de gráfico de filtro irá organizar o gráfico de filtro a ser interrompido e o PIN reconectado. Durante a reconexão subsequente, o renderizador pode aceitar um formato mais apropriado.

Sempre que um processador de vídeo detectar uma alteração de paleta no fluxo, ele deverá enviar a notificação de alteração da [**\_ \_ paleta do EC**](ec-palette-changed.md) para o Gerenciador do grafo de filtro. Os renderizadores de vídeo do DirectShow detectam se uma paleta realmente foi alterada em formato dinâmico ou não. Os renderizadores de vídeo fazem isso não apenas para filtrar o número de **notificações \_ \_ alteradas da paleta do EC** enviadas, mas também para reduzir a quantidade de criação, instalação e exclusão da paleta necessária.

Por fim, o processador de vídeo também pode detectar que o tamanho do vídeo foi alterado; nesse caso, ele deve enviar a notificação de [**alteração de tamanho de vídeo do EC \_ \_ \_**](ec-video-size-changed.md) . Um aplicativo pode usar essa notificação para negociar espaço em um documento composto. As dimensões de vídeo reais estão disponíveis por meio da interface de controle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Os renderizadores do DirectShow detectam se o vídeo realmente alterou o tamanho ou não antes de enviar esses eventos.

## <a name="handling-persistent-properties"></a>Manipulando propriedades persistentes

Todas as propriedades definidas por meio das interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) devem ser persistentes entre as conexões. Portanto, desconectar e reconectar um renderizador não deve mostrar nenhum efeito sobre o tamanho, a posição ou os estilos da janela. No entanto, se as dimensões de vídeo mudarem entre as conexões, o renderizador deverá redefinir os retângulos de origem e de destino para seus padrões. As posições de origem e de destino são definidas por meio da interface **IBasicVideo** .

[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) fornecem acesso suficiente às propriedades para permitir que um aplicativo salve e restaure todos os dados na interface em um formato persistente. Isso será útil para aplicativos que devem salvar a configuração e as propriedades exatas dos grafos de filtro durante uma sessão de edição e restaurá-los mais tarde.

## <a name="handling-ec_repaint-notifications"></a>Lidando com \_ notificações de REdesenho de EC

A notificação de [**\_ redesenho do EC**](ec-repaint.md) é enviada somente quando o renderizador é pausado ou parado. Essa notificação sinaliza para o Gerenciador do grafo de filtro que o renderizador precisa de dados. Se o grafo de filtro for interrompido quando receber uma dessas notificações, ele pausará o gráfico de filtro, aguardará que todos os filtros recebam dados (chamando [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)) e, em seguida, o interromperá novamente. Quando parado, um renderizador de vídeo deve ser mantido na imagem para que as mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) subsequentes possam ser tratadas.

Portanto, se um renderizador de vídeo receber uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) quando for interrompido ou pausado, e não tiver nada com o qual pintar sua janela, ele deverá enviar o [**EC \_ Repaint**](ec-repaint.md) para o Gerenciador do grafo de filtro. Se uma **notificação \_ redesenhada do EC** for recebida enquanto estiver em pausa, o Gerenciador do grafo de filtro chamará [**IMediaPosition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) com a posição atual (ou seja, busca a posição atual). Isso faz com que os filtros de origem liberem o gráfico de filtro e que os novos dados sejam enviados por meio do grafo de filtro.

Um renderizador deve enviar apenas uma dessas notificações por vez. Portanto, depois que o renderizador envia uma notificação, ele deve garantir que não seja mais enviado até que alguns exemplos sejam entregues. A maneira convencional de fazer isso é ter um sinalizador para significar que um redesenho pode ser enviado, que é desativado depois que uma notificação de [**\_ redesenho de EC**](ec-repaint.md) é enviada. Esse sinalizador deve ser redefinido quando os dados são entregues ou quando o PIN de entrada é liberado, mas não se o fim do fluxo é sinalizado no pino de entrada.

Se o renderizador não monitorar suas notificações de [**\_ redesenho de EC**](ec-repaint.md) , ele irá inundar o Gerenciador de gráficos de filtro com solicitações de **\_ redesenho de EC** (que são relativamente caras de processar). Por exemplo, se um renderizador não tiver nenhuma imagem para desenhar e outra janela for arrastada pela janela do processador em uma operação de arrastar completo, o renderizador receberá várias mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) . Somente o primeiro deles deve gerar uma notificação de evento do **EC \_ Repaint** do renderizador para o Gerenciador do grafo de filtro.

Um processador deve enviar seu PIN de entrada como o primeiro parâmetro para a notificação de [**\_ redesenho do EC**](ec-repaint.md) . Ao fazer isso, o pino de saída anexado será consultado por [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)e, se houver suporte, a notificação de **\_ redesenho do EC** será enviada primeiro. Isso permite que os Pins de saída manipulem repinturas antes que o gráfico de filtro seja tocado. Isso não será feito se o grafo de filtro for interrompido, porque nenhum buffer estaria disponível no alocador de processador descomprometido.

Se o pino de saída não puder tratar a solicitação e o grafo de filtro estiver em execução, a notificação de [**\_ redesenho do EC**](ec-repaint.md) será ignorada. Um pino de saída deve retornar **S \_ OK** de [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) para sinalizar que ele processou a solicitação redesenhada com êxito. O pino de saída será chamado no thread de trabalho do Gerenciador do grafo de filtro, que evita que o renderizador chame o pino de saída diretamente e, portanto, evita quaisquer problemas de deadlock. Se o grafo de filtro for interrompido ou pausado e a saída não tratar a solicitação, o processamento padrão será feito.

## <a name="handling-notifications-in-full-screen-mode"></a>Manipulando notificações no modo de Full-Screen

O distribuidor de plug-in do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) no gráfico de filtro gerencia a reprodução em tela inteira. Ele alternará um processador de vídeo para um processador de tela inteira de especialista, ampliará uma janela de um renderizador para tela inteira ou fará com que o renderizador implemente a reprodução de tela inteira diretamente. Para interagir em protocolos de tela inteira, um processador de vídeo deve enviar uma notificação de [**\_ ativação do EC**](ec-activate.md) sempre que sua janela for ativada ou desativada. Em outras palavras, uma notificação de **\_ ativação do EC** deve ser enviada para cada mensagem do WM \_ ACTIVATEAPP que um processador recebe.

Quando um processador está sendo usado no modo de tela inteira, essas notificações gerenciam a alternância para dentro e fora desse modo de tela inteira. A desativação de janela geralmente ocorre quando um usuário pressiona ALT + TAB para alternar para outra janela, que o processador de tela cheia do DirectShow usa como uma indicação para retornar ao modo de renderização típico.

Quando a notificação de [**\_ ativação do EC**](ec-activate.md) é enviada para o Gerenciador do grafo de filtro após a alternância do modo de tela inteira, o Gerenciador do grafo de filtro envia uma notificação de [**\_ \_ tela**](ec-fullscreen-lost.md) de ecrã do EC para o aplicativo de controle. O aplicativo pode usar essa notificação para restaurar o estado de um botão de tela inteira, por exemplo. As notificações de **\_ ativação do EC** são usadas internamente pelo DirectShow para gerenciar a alternância de tela inteira em indicações dos renderizadores de vídeo.

## <a name="summary-of-notifications"></a>Resumo de notificações

Esta seção lista as notificações de gráfico de filtro que um renderizador pode enviar.



| Notificação de eventos                                        | Descrição                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ativação do EC \_**](ec-activate.md)                       | Enviado por renderizadores de vídeo no modo de renderização de tela inteira para cada mensagem de ACTIVATEAPP do WM \_ recebida.                                                                                                  |
| [**EC \_ concluído**](ec-complete.md)                       | Enviado por renderizadores após a renderização de todos os dados.                                                                                                                                               |
| [**exibição do EC \_ \_ alterada**](ec-display-changed.md)        | Enviado por renderizadores de vídeo quando um formato de exibição é alterado.                                                                                                                                            |
| [**paleta do EC \_ \_ alterada**](ec-palette-changed.md)        | Enviado sempre que um processador de vídeo detecta uma alteração de paleta no fluxo.                                                                                                                            |
| [**redesenho de EC \_**](ec-repaint.md)                         | Enviado por renderizadores de vídeo interrompidos ou pausados quando uma mensagem de pintura do WM \_ é recebida e não há dados a serem exibidos. Isso faz com que o Gerenciador de gráfico de filtro gere um quadro para pintar para a exibição. |
| [**autoanulação do EC \_**](ec-userabort.md)                     | Enviado por renderizadores de vídeo para sinalizar um fechamento solicitado pelo usuário (por exemplo, um usuário fechando a janela de vídeo).                                                                               |
| [**tamanho de vídeo do EC \_ \_ \_ alterado**](ec-video-size-changed.md) | Enviado por renderizadores de vídeo sempre que uma alteração no tamanho de vídeo nativo é detectada.                                                                                                                       |
| [**janela do EC \_ \_ destruída**](ec-window-destroyed.md)      | Enviado por renderizadores de vídeo quando o filtro é removido ou destruído para que os recursos que dependem do foco da janela possam ser passados para outros filtros.                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo renderizadores de vídeo](writing-video-renderers.md)
</dt> </dl>

 

 
