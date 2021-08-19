---
description: Este tópico descreve como escrever um renderador de vídeo personalizado para DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Renderadores de vídeo alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd105f406e1b39d998a027a915621f214ec2e769f373912a1e9e8525573f31aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074800"
---
# <a name="alternative-video-renderers"></a>Renderadores de vídeo alternativos

Este tópico descreve como escrever um renderador de vídeo personalizado para DirectShow.

> [!Note]  
> Em vez de escrever um renderizador de vídeo personalizado, é recomendável que você escreva um alocador-presenter de plug-in para a VMR (Renderizador de Mistura de Vídeo) ou OVR [**(Renderizador**](enhanced-video-renderer-filter.md) de Vídeo Aprimorado). Essa abordagem lhe dará todos os benefícios da VMR/EVR, incluindo suporte para DXVA (Aceleração de Vídeo) do DirectX, desintervalo de hardware e etapa de quadro e provavelmente será mais robusto do que um renderador de vídeo personalizado. Para obter mais informações, consulte estes tópicos:
>
> -   [Modo de reprodução sem renderização de VMR (alocador-presenters personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Como escrever um apresentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Escrevendo um renderdor alternativo

O Microsoft DirectShow fornece um renderador de vídeo baseado em janela; ele também fornece um renderador de tela inteira na instalação em tempo de executar. Você pode usar as classes DirectShow base para escrever renderadores de vídeo alternativos. Para que os renderadores alternativos interajam corretamente com DirectShow baseados em DirectShow, os renderadores devem seguir as diretrizes descritas neste artigo. Você pode usar as [**classes CBaseRenderer**](cbaserenderer.md) e [**CBaseVideoRenderer**](cbasevideorenderer.md) para ajudar a seguir essas diretrizes ao implementar uma renderização de vídeo alternativa. Devido ao desenvolvimento contínuo de DirectShow, revise sua implementação periodicamente para garantir que os renderadores sejam compatíveis com a versão mais recente do DirectShow.

Este tópico discute muitas notificações de que um renderador é responsável pelo tratamento. Uma breve revisão de DirectShow notificações pode ajudar a definir o estágio. Há essencialmente três tipos de notificações que ocorrem em DirectShow:

-   *Notificações de fluxo*, que são eventos que ocorrem no fluxo de mídia e são passados de um filtro para o próximo. Eles podem ser notificações de liberação de início, liberação final ou fim de fluxo e são enviados chamando o método apropriado no pino de entrada do filtro downstream (por [**exemplo, IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)).
-   *Filtrar notificações de grafo*, que são eventos enviados de um filtro para o Gerenciador Graph Filtro, como [**EC \_ COMPLETE.**](ec-complete.md) Isso é feito chamando o [**método IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) no Gerenciador de Graph Filtro.
-   *Notificações de aplicativo*, que são recuperadas do Gerenciador Graph filtro pelo aplicativo de controle. Um aplicativo chama o [**método IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) no Gerenciador Graph Filtro para recuperar esses eventos. Geralmente, o Gerenciador Graph Filtro passa pelos eventos recebidos para o aplicativo.

Este tópico discute a responsabilidade do filtro do renderdor no tratamento de notificações de fluxo que ele recebe e no envio de notificações de grafo de filtro apropriadas.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Manipulando notificações de fim de fluxo e liberação

Uma notificação de fim de fluxo começa em um filtro upstream (como o filtro de origem) quando esse filtro detecta que ele não pode enviar mais dados. Ele é passado por todos os filtros no grafo e, eventualmente, termina no renderador, que é responsável por enviar subsequentemente uma notificação [**EC \_ COMPLETE**](ec-complete.md) para o Gerenciador de Graph Filtro. Os renderadores têm responsabilidades especiais quando se trata de lidar com essas notificações.

Um renderador recebe uma notificação de fim de fluxo quando o método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) do pino de entrada é chamado pelo filtro upstream. Um renderador deve observar essa notificação e continuar a renderizar todos os dados que ele já recebeu. Depois que todos os dados restantes foram recebidos, o renderador deve enviar uma notificação [**EC \_ COMPLETE**](ec-complete.md) para o Gerenciador Graph Filtro. A **\_ notificação EC COMPLETE** deve ser enviada apenas uma vez por um renderador sempre que atingir o final de um fluxo. Além disso, **as notificações EC \_ COMPLETE** nunca devem ser enviadas, exceto quando o grafo de filtro está em execução. Portanto, se o grafo de filtro estiver em pausa quando um filtro de origem enviar uma notificação de fim de fluxo, EC **\_ COMPLETE** não deverá ser enviado até que o grafo de filtro seja finalmente executado.

Todas as chamadas para os métodos [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) depois que uma notificação de fim de fluxo é sinalizada devem ser rejeitadas. **E \_ UNEXPECTED** é a mensagem de erro mais apropriada a ser retornada nesse caso.

Quando um grafo de filtro é interrompido, qualquer notificação de fim de fluxo armazenada em cache deve ser limpa e não ressente quando a próxima vez for iniciada. Isso ocorre porque o Gerenciador de Graph Filtro sempre pausa todos os filtros antes de ser executado para que ocorra a liberação adequada. Portanto, por exemplo, se o grafo de filtro estiver em pausa e uma notificação de fim de fluxo for recebida e, em seguida, o grafo de filtro for interrompido, o renderador não deverá enviar uma notificação [**EC \_ COMPLETE**](ec-complete.md) quando for executado posteriormente. Se nenhuma busca tiver ocorrido, o filtro de origem enviará automaticamente outra notificação de fim de fluxo durante o estado de pausa que precede um estado de executar. Se, por outro lado, uma busca tiver ocorrido enquanto o grafo de filtro é interrompido, o filtro de origem poderá ter dados a enviar, portanto, ele não enviará uma notificação de fim de fluxo.

Os renderadores de vídeo geralmente dependem de notificações de fim de fluxo para mais do que o envio de [**notificações EC \_ COMPLETE.**](ec-complete.md) Por exemplo, se um fluxo tiver terminado a reprodução (ou seja, uma notificação de fim de fluxo é enviada) e outra janela for arrastada sobre uma janela do renderador de vídeo, várias mensagens da janela [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) serão geradas. A prática típica para executar renderadores de vídeo é evitar a reformulação do quadro atual após o recebimento de mensagens **WM \_ PAINT** (com base na suposição de que outro quadro a ser desenhado será recebido). No entanto, quando a notificação de fim de fluxo foi enviada, o renderador está em um estado de espera; ele ainda está em execução, mas está ciente de que não receberá nenhum dado adicional. Nessas circunstâncias, o renderista desenha a área de reprodução em preto de forma personalizada.

Lidar com a liberação é uma complicação adicional para renderdores. A liberação é executada por meio de um par de [**métodos IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) chamados [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) A liberação é essencialmente um estado adicional que o renderista deve manipular. É ilegal para um filtro de origem chamar **BeginFlush** sem chamar **EndFlush,** portanto, esperamos que o estado seja curto e discreto; no entanto, o renderador deve lidar corretamente com dados ou notificações que recebe durante a transição de liberação.

Todos os dados recebidos após [**chamar BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) devem ser rejeitados imediatamente retornando **S \_ FALSE.** Além disso, qualquer notificação de fim de fluxo armazenada em cache também deve ser limpa quando um renderador é liberado. Um renderador normalmente será liberado em resposta a uma busca. A liberação garante que os dados antigos sejam limpos do grafo de filtro antes que novas amostras sejam enviadas. (Normalmente, a reprodução de duas seções de um fluxo, uma após a outra, é melhor manipulada por meio de comandos adiados, em vez de aguardar a finalização de uma seção e, em seguida, a emissão de um comando seek.)

## <a name="handling-state-changes-and-pause-completion"></a>Manipulando alterações de estado e pausando a conclusão

Um filtro de renderador se comporta da mesma forma que qualquer outro filtro no grafo de filtro quando seu estado é alterado, com a exceção a seguir. Depois de pausar, o renderador terá alguns dados na fila, prontos para serem renderizados quando executados posteriormente. Quando o renderador de vídeo é interrompido, ele mantém esses dados na fila. Essa é uma exceção à regra DirectShow que nenhum recurso deve ser mantido por filtros enquanto o grafo de filtro é interrompido.

O motivo para essa exceção é que, mantendo os recursos, o renderador sempre terá uma imagem com a qual repintar a janela se receber uma mensagem [**WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Ele também tem uma imagem para atender a métodos, como [**CBaseControlVideo::GetStaticImage**](cbasecontrolvideo-getstaticimage.md), que solicitam uma cópia da imagem atual. Outro efeito de manter os recursos é que manter a imagem impede que o alocador seja descommitido, o que, por sua vez, faz com que a próxima alteração de estado ocorra muito mais rapidamente porque os buffers de imagem já estão alocados.

Um renderador de vídeo deve renderizar e liberar amostras somente durante a execução. Enquanto pausado, o filtro pode renderizar (por exemplo, ao desenhar uma imagem de cartaz estático em uma janela), mas não deve liberá-las. Os renderadores de áudio não realizarão nenhuma renderização durante a pausa (embora possam executar outras atividades, como preparar o dispositivo de onda, por exemplo). O tempo em que os exemplos devem ser renderizados é obtido combinando o tempo de fluxo no exemplo com o tempo de referência passado como um parâmetro para o [**método IMediaControl::Run.**](/windows/desktop/api/Control/nf-control-imediacontrol-run) Os renderizadores devem rejeitar exemplos com horários de início menores ou iguais às horas de término.

Quando um aplicativo pausa um grafo de filtro, o grafo de filtro não retorna de seu método [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) até que haja dados na fila nos renderadores. Para garantir isso, quando um renderador é pausado, ele deve retornar S FALSE se não houver dados \_ aguardando para serem renderizados. Se tiver dados na fila, ele poderá retornar **S \_ OK.**

O Gerenciador Graph Filtro verifica todos os valores de retorno ao pausar um grafo de filtro para garantir que os renderadores tenham dados na fila. Se um ou mais filtros não estão prontos, o Gerenciador de filtros Graph pesquisa os filtros no grafo chamando [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). O **método GetState** leva um parâmetro de tempo-out. Um filtro (normalmente um renderador) que ainda está aguardando a chegada dos dados antes de concluir a alteração de estado retornará **O VFW \_ S STATE \_ \_ INTERMEDIATE** se o **método GetState** expirar. Depois que os dados chegam ao renderador, **GetState** deve ser retornado imediatamente com **S \_ OK.**

No estado intermediário e concluído, o estado do filtro relatado será Estado \_ Pausado. Somente o valor de retorno indica se o filtro está realmente pronto ou não. Se, enquanto um renderador estiver aguardando a chegada dos dados, seu filtro de origem enviará uma notificação de fim de fluxo, isso também deverá concluir a alteração de estado.

Depois que todos os filtros realmente têm dados aguardando para serem renderizados, o grafo de filtro concluirá sua alteração de estado de pausa.

## <a name="handling-termination"></a>Tratamento de encerramento

Os renderadores de vídeo devem lidar corretamente com eventos de encerramento do usuário. Isso implica ocultar corretamente a janela e saber o que fazer se uma janela for subsequentemente forçada a ser exibida. Além disso, os renderadores de vídeo devem notificar o Gerenciador de filtros Graph quando sua janela for destruída (ou com mais precisão, quando o renderador for removido do grafo de filtro) para liberar recursos.

Se o usuário fechar a janela de vídeo (por exemplo, pressionando ALT+F4), a convenção será ocultar a janela imediatamente e enviar uma notificação [**EC \_ USERABORT**](ec-userabort.md) para o Gerenciador de Graph De filtro. Essa notificação é passada para o aplicativo, o que interromperá a reprodução do grafo. Depois de **enviar EC \_ USERABORT**, um renderador de vídeo deve rejeitar quaisquer exemplos adicionais entregues a ele.

O sinalizador parado no grafo deve ser deixado no renderdor até que ele seja interrompido subsequentemente. Nesse ponto, ele deve ser redefinido para que um aplicativo possa substituir a ação do usuário e continuar a tocar o grafo se desejar. Se ALT+F4 for pressionado enquanto o vídeo estiver em execução, a janela ficará oculta e todos os outros exemplos entregues serão rejeitados. Se a janela for mostrada posteriormente (talvez por meio de [**IVideoWindow::p ut \_ Visible),**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)nenhuma notificação [**EC \_ REPAINT**](ec-repaint.md) deverá ser gerada.

O renderador de vídeo também deve enviar a [**notificação EC \_ WINDOW \_ DESTROYED**](ec-window-destroyed.md) para o grafo de filtro quando o renderador de vídeo estiver encerrando. Na verdade, é melhor lidar com isso quando o método [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do renderdor é chamado com um parâmetro nulo (indicando que o renderador está prestes a ser removido do grafo de filtro), em vez de aguardar até que a janela de vídeo real seja destruída. Enviar essa notificação permite que o distribuidor de plug-in no Gerenciador de filtros Graph passe recursos que dependem do foco da janela para outros filtros, como dispositivos de áudio.

## <a name="handling-dynamic-format-changes"></a>Manipulando alterações de formato dinâmico

Em alguns casos, o filtro upstream do renderador pode tentar alterar o formato de vídeo enquanto o vídeo está sendo gravado. Geralmente, é o descompactador de vídeo que inicia uma alteração de formato dinâmico.

Um filtro upstream que tenta alterar formatos dinamicamente sempre deve chamar o método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de entrada do renderador. Um renderador de vídeo tem alguma margem de trabalho sobre quais tipos de alterações de formato dinâmico ele deve dar suporte. No mínimo, ele deve permitir que o filtro upstream altere as paletas. Quando um filtro upstream altera os tipos de mídia, ele anexa o tipo de mídia ao primeiro exemplo entregue no novo formato. Se o renderizador mantiver amostras em uma fila para renderização, ele não deverá alterar o formato até que ele processe o exemplo com a alteração de tipo.

Um processador de vídeo também pode solicitar uma alteração de formato do decodificador. Por exemplo, ele pode solicitar que o decodificador forneça um formato compatível com o DirectDraw com uma **superaltura** negativa. Quando o renderizador é pausado, ele deve chamar [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino upstream para ver quais formatos o decodificador pode fornecer. O decodificador pode não enumerar todos os tipos que ele pode aceitar, no entanto, portanto, o renderizador deve oferecer alguns tipos, mesmo que o decodificador não os Anuncie.

Se o decodificador puder mudar para o formato solicitado, ele retornará **S \_ OK** de [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). Em seguida, o renderizador anexa o novo tipo de mídia ao exemplo de mídia seguinte no alocador upstream. Para que isso funcione, o renderizador deve fornecer um alocador personalizado que implementa um método particular para anexar o tipo de mídia ao próximo exemplo. (Dentro desse método particular, chame [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para definir o tipo.)

O PIN de entrada do renderizador deve retornar o alocador personalizado do renderizador no método [**IMemInputPin:: Getalocador**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) . Substitua [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para que falhe se o filtro upstream não usar o alocador do processador.

Com alguns decodificadores, a configuração de **biHeight** para um número positivo em tipos YUV faz com que o decodificador desenhe a imagem de cabeça para baixo. (Isso está incorreto e deve ser considerado um bug no decodificador.)

Sempre que uma alteração de formato é detectada pelo processador de vídeo, ele deve enviar uma notificação de [**exibição de EC \_ \_ alterada**](ec-display-changed.md) . A maioria dos renderizadores de vídeo escolhe um formato durante a conexão para que o formato possa ser desenhado com eficiência por meio da GDI. Se o usuário alterar o modo de exibição atual sem reiniciar o computador, um processador poderá se encontrar com uma conexão de formato de imagem inadequada e deverá enviar essa notificação. O primeiro parâmetro deve ser o PIN que precisa ser reconectado. o filtro Graph Manager irá organizar o gráfico de filtro a ser interrompido e o pin reconectado. Durante a reconexão subsequente, o renderizador pode aceitar um formato mais apropriado.

sempre que um processador de vídeo detectar uma alteração de paleta no fluxo, ele deverá enviar a notificação de alteração da [**\_ \_ paleta do EC**](ec-palette-changed.md) para o gerenciador de Graph do filtro. os renderizadores de vídeo DirectShow detectam se uma paleta realmente foi alterada em formato dinâmico ou não. Os renderizadores de vídeo fazem isso não apenas para filtrar o número de **notificações \_ \_ alteradas da paleta do EC** enviadas, mas também para reduzir a quantidade de criação, instalação e exclusão da paleta necessária.

Por fim, o processador de vídeo também pode detectar que o tamanho do vídeo foi alterado; nesse caso, ele deve enviar a notificação de [**alteração de tamanho de vídeo do EC \_ \_ \_**](ec-video-size-changed.md) . Um aplicativo pode usar essa notificação para negociar espaço em um documento composto. As dimensões de vídeo reais estão disponíveis por meio da interface de controle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . os renderizadores de DirectShow detectam se o vídeo realmente alterou o tamanho ou não antes de enviar esses eventos.

## <a name="handling-persistent-properties"></a>Manipulando propriedades persistentes

Todas as propriedades definidas por meio das interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) devem ser persistentes entre as conexões. Portanto, desconectar e reconectar um renderizador não deve mostrar nenhum efeito sobre o tamanho, a posição ou os estilos da janela. No entanto, se as dimensões de vídeo mudarem entre as conexões, o renderizador deverá redefinir os retângulos de origem e de destino para seus padrões. As posições de origem e de destino são definidas por meio da interface **IBasicVideo** .

[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) fornecem acesso suficiente às propriedades para permitir que um aplicativo salve e restaure todos os dados na interface em um formato persistente. Isso será útil para aplicativos que devem salvar a configuração e as propriedades exatas dos grafos de filtro durante uma sessão de edição e restaurá-los mais tarde.

## <a name="handling-ec_repaint-notifications"></a>Lidando com \_ notificações de REdesenho de EC

A notificação de [**\_ redesenho do EC**](ec-repaint.md) é enviada somente quando o renderizador é pausado ou parado. essa notificação sinaliza para o gerenciador de Graph de filtro que o renderizador precisa de dados. Se o grafo de filtro for interrompido quando receber uma dessas notificações, ele pausará o gráfico de filtro, aguardará que todos os filtros recebam dados (chamando [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)) e, em seguida, o interromperá novamente. Quando parado, um renderizador de vídeo deve ser mantido na imagem para que as mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) subsequentes possam ser tratadas.

portanto, se um renderizador de vídeo receber uma mensagem do [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) quando for interrompido ou pausado, e não tiver nada com o qual pintar sua janela, ele deverá enviar o [**EC \_ repaint**](ec-repaint.md) para o filtro Graph Manager. se uma **notificação \_ redesenhada do EC** for recebida enquanto estiver em pausa, o filtro Graph Manager chamará [**IMediaPosition::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) com a posição atual (ou seja, busca a posição atual). Isso faz com que os filtros de origem liberem o gráfico de filtro e que os novos dados sejam enviados por meio do grafo de filtro.

Um renderizador deve enviar apenas uma dessas notificações por vez. Portanto, depois que o renderizador envia uma notificação, ele deve garantir que não seja mais enviado até que alguns exemplos sejam entregues. A maneira convencional de fazer isso é ter um sinalizador para significar que um redesenho pode ser enviado, que é desativado depois que uma notificação de [**\_ redesenho de EC**](ec-repaint.md) é enviada. Esse sinalizador deve ser redefinido quando os dados são entregues ou quando o PIN de entrada é liberado, mas não se o fim do fluxo é sinalizado no pino de entrada.

se o renderizador não monitorar suas notificações de [**\_ redesenho de ec**](ec-repaint.md) , ele irá inundar o filtro Graph Manager com solicitações de **\_ redesenho de ec** (que são relativamente caras de processar). Por exemplo, se um renderizador não tiver nenhuma imagem para desenhar e outra janela for arrastada pela janela do processador em uma operação de arrastar completo, o renderizador receberá várias mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) . somente o primeiro deles deve gerar uma notificação de evento do **EC \_ repaint** do renderizador para o filtro Graph Manager.

Um processador deve enviar seu PIN de entrada como o primeiro parâmetro para a notificação de [**\_ redesenho do EC**](ec-repaint.md) . Ao fazer isso, o pino de saída anexado será consultado por [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)e, se houver suporte, a notificação de **\_ redesenho do EC** será enviada primeiro. Isso permite que os Pins de saída manipulem repinturas antes que o gráfico de filtro seja tocado. Isso não será feito se o grafo de filtro for interrompido, porque nenhum buffer estaria disponível no alocador de processador descomprometido.

Se o pino de saída não puder tratar a solicitação e o grafo de filtro estiver em execução, a notificação de [**\_ redesenho do EC**](ec-repaint.md) será ignorada. Um pino de saída deve retornar **S \_ OK** de [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) para sinalizar que ele processou a solicitação redesenhada com êxito. o pino de saída será chamado no thread de trabalho do filtro Graph Manager, que evita que o renderizador chame o pino de saída diretamente e, portanto, evita quaisquer problemas de deadlock. Se o grafo de filtro for interrompido ou pausado e a saída não tratar a solicitação, o processamento padrão será feito.

## <a name="handling-notifications-in-full-screen-mode"></a>Manipulando notificações no modo de Full-Screen

O distribuidor de plug-in do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) no gráfico de filtro gerencia a reprodução em tela inteira. Ele alternará um processador de vídeo para um processador de tela inteira de especialista, ampliará uma janela de um renderizador para tela inteira ou fará com que o renderizador implemente a reprodução de tela inteira diretamente. Para interagir em protocolos de tela inteira, um processador de vídeo deve enviar uma notificação de [**\_ ativação do EC**](ec-activate.md) sempre que sua janela for ativada ou desativada. Em outras palavras, uma notificação de **\_ ativação do EC** deve ser enviada para cada mensagem do WM \_ ACTIVATEAPP que um processador recebe.

Quando um processador está sendo usado no modo de tela inteira, essas notificações gerenciam a alternância para dentro e fora desse modo de tela inteira. a desativação de janela geralmente ocorre quando um usuário pressiona ALT + TAB para alternar para outra janela, que o processador de tela inteira DirectShow usa como uma indicação para retornar ao modo de renderização típico.

quando a notificação de [**\_ ativação do EC**](ec-activate.md) é enviada ao filtro Graph manager ao alternar para fora do modo de tela inteira, o filtro Graph manager envia uma notificação de tela de ecrã do ec em caso de [**\_ \_ perda**](ec-fullscreen-lost.md) no aplicativo de controle. O aplicativo pode usar essa notificação para restaurar o estado de um botão de tela inteira, por exemplo. as notificações de **\_ ativação do EC** são usadas internamente pelo DirectShow para gerenciar a alternância de tela inteira em indicações dos renderizadores de vídeo.

## <a name="summary-of-notifications"></a>Resumo de notificações

Esta seção lista as notificações de gráfico de filtro que um renderizador pode enviar.



| Notificação de eventos                                        | Descrição                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ativação do EC \_**](ec-activate.md)                       | Enviado por renderizadores de vídeo no modo de renderização de tela inteira para cada mensagem de ACTIVATEAPP do WM \_ recebida.                                                                                                  |
| [**EC \_ concluído**](ec-complete.md)                       | Enviado por renderizadores após a renderização de todos os dados.                                                                                                                                               |
| [**exibição do EC \_ \_ alterada**](ec-display-changed.md)        | Enviado por renderizadores de vídeo quando um formato de exibição é alterado.                                                                                                                                            |
| [**paleta do EC \_ \_ alterada**](ec-palette-changed.md)        | Enviado sempre que um processador de vídeo detecta uma alteração de paleta no fluxo.                                                                                                                            |
| [**redesenho de EC \_**](ec-repaint.md)                         | Enviado por renderizadores de vídeo interrompidos ou pausados quando uma mensagem de pintura do WM \_ é recebida e não há dados a serem exibidos. isso faz com que o filtro Graph Manager gere um quadro para pintar para a exibição. |
| [**autoanulação do EC \_**](ec-userabort.md)                     | Enviado por renderizadores de vídeo para sinalizar um fechamento solicitado pelo usuário (por exemplo, um usuário fechando a janela de vídeo).                                                                               |
| [**tamanho de vídeo do EC \_ \_ \_ alterado**](ec-video-size-changed.md) | Enviado por renderizadores de vídeo sempre que uma alteração no tamanho de vídeo nativo é detectada.                                                                                                                       |
| [**janela do EC \_ \_ destruída**](ec-window-destroyed.md)      | Enviado por renderizadores de vídeo quando o filtro é removido ou destruído para que os recursos que dependem do foco da janela possam ser passados para outros filtros.                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo renderizadores de vídeo](writing-video-renderers.md)
</dt> </dl>

 

 
