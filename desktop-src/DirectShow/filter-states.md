---
description: Estados de filtro
ms.assetid: 97418307-eb50-4c8e-b03b-a2cd08139bdc
title: Estados de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 487b2f5e71cfebd8a9c7282679aa39b2264f0460dd72ad23e1b2b26926e0c979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015734"
---
# <a name="filter-states"></a>Estados de filtro

Os filtros têm três estados possíveis: parado, em pausa e em execução. A finalidade do estado de pausa é a indicação de dados no grafo, para que um comando de execução responda imediatamente. o filtro Graph gerenciador controla todas as transições de estado. quando um aplicativo chama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)ou [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), o Filter Graph Manager chama o método [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) correspondente em todos os filtros. as transições entre a parada e a execução sempre passam pelo estado pausado, portanto, se o aplicativo chamar **executar** em um grafo interrompido, o filtro Graph Manager pausará o grafo antes de executá-lo.

Para a maioria dos filtros, os Estados em execução e em pausa são idênticos. Considere o seguinte grafo de filtro:

Processador de > de transformação de > de origem

Suponha que, por enquanto, o filtro de origem não seja uma origem de captura dinâmica. Quando o filtro de origem pausa, ele cria um thread que gera novos dados e grava-os em amostras de mídia o mais rápido possível. O thread "envia por push" as amostras downstream chamando [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada do filtro de transformação. O filtro de transformação recebe os exemplos no thread do filtro de origem. Ele pode usar um thread de trabalho para entregar os exemplos para o renderizador, mas normalmente os entrega no mesmo thread. Enquanto o renderizador está em pausa, ele aguarda para receber um exemplo. Depois de receber um, ele bloqueia e mantém esse exemplo indefinidamente. Se for um processador de vídeo, ele exibirá o exemplo como uma imagem de pôster, redesenhando a imagem conforme necessário.

Neste ponto, o fluxo é totalmente cued e está pronto para renderização. Se o grafo permanecer em pausa, os exemplos serão "acumulados" no grafo atrás do primeiro exemplo, até que cada filtro seja bloqueado em [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). No entanto, nenhum dado é perdido. Depois que o thread de origem é desbloqueado, ele simplesmente retoma a partir do ponto em que ele foi bloqueado.

O filtro de origem e o filtro de transformação ignoram a transição de em pausa para em execução – eles simplesmente continuam processando os dados o mais rápido possível. Mas quando o processador é executado, ele inicia a renderização de exemplos. Primeiro, ele renderiza o exemplo mantido enquanto ele estava em pausa. Em seguida, sempre que receber um novo exemplo, ele calculará o tempo de apresentação do exemplo. (Para obter detalhes, consulte [tempo e relógios em DirectShow](time-and-clocks-in-directshow.md).) O renderizador mantém cada amostra até o momento da apresentação, ponto em que ele renderiza o exemplo. Enquanto ele aguarda o tempo de apresentação, ele é bloqueado no método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou recebe novos exemplos em um thread de trabalho com uma fila. Os filtros upstream do renderizador não estão envolvidos no agendamento.

Fontes dinâmicas, como dispositivos de captura, são uma exceção para essa arquitetura geral. Com uma fonte dinâmica, não é apropriado marcar os dados com antecedência. O aplicativo pode pausar o grafo e aguardar um longo tempo antes de executá-lo. O grafo não deve renderizar exemplos "obsoletos". Portanto, uma fonte dinâmica não produz amostras enquanto está em pausa, somente durante a execução. para sinalizar esse fato ao filtro Graph Manager, o método [**IMediaFilter:: getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) do filtro de origem retorna VFW s não está \_ \_ \_ CUE. Esse código de retorno indica que o filtro mudou para o estado em pausa, embora o renderizador não tenha recebido nenhum dado.

Quando um filtro é interrompido, ele rejeita mais exemplos entregues a ele. Os filtros de origem desligam seus threads de streaming e outros filtros desligam quaisquer threads de trabalho que eles possam ter criado. Os Pins desconfirmam seus alocadores.

### <a name="state-transitions"></a>Transições de estado

o filtro Graph Manager executa todas as transições de estado na ordem de upstream, começando do renderizador e trabalhando de volta para o filtro de origem. Essa ordenação é necessária para evitar que amostras sejam descartadas e impedir que o grafo seja bloqueado. As transições de estado mais cruciais ficam entre pausa e parada:

-   Parado para pausado: como cada filtro é pausado, ele fica pronto para receber amostras do próximo filtro. O filtro de origem é o último a ser pausado. Ele cria o thread de streaming e começa a fornecer exemplos. Como todos os filtros downstream estão em pausa, nenhum filtro rejeita nenhuma amostra. o filtro Graph Manager não conclui a transição até que todos os renderizadores no grafo tenham recebido um exemplo (com exceção das fontes dinâmicas, conforme descrito anteriormente).
-   Em pausa para parado: quando um filtro é interrompido, ele libera todos os exemplos que ele contém, o que desbloqueia quaisquer filtros upstream aguardando em [**GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Se o filtro estiver aguardando um recurso dentro do método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , ele interromperá a espera e retornará de **Receive**, que desbloqueará o filtro de chamada. portanto, quando o filtro Graph Manager para o próximo filtro upstream, esse filtro não é bloqueado em **GetBuffer** ou **Receive** e pode responder ao comando stop. O filtro upstream pode fornecer alguns exemplos extras antes de obter o comando Stop, mas o filtro downstream simplesmente os rejeita, pois ele já parou.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Flow de dados no filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



