---
description: Entregando exemplos
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Entregando exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370339"
---
# <a name="delivering-samples"></a>Entregando exemplos

Este artigo descreve como um filtro fornece um exemplo. Ele descreve o modelo de push, usando métodos [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e o modelo de pull, usando [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Modelo de push: entregando um exemplo**

O pino de saída fornece um exemplo chamando o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) , que é equivalente, mas fornece uma matriz de exemplos. O PIN de entrada pode bloquear dentro de **Receive** (ou **ReceiveMultiple**). Se o PIN puder ser bloqueado, seu método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) deverá retornar S \_ OK. Se o PIN garantir que nunca seja bloqueado, **ReceiveCanBlock** deverá retornar S \_ false. O \_ valor de retorno S OK não significa que o **Receive** Always Block, exatamente o que ele pode.

Embora **Receive** possa bloquear a espera de um recurso ficar disponível, ele não deve bloquear para aguardar mais dados do filtro upstream. Isso pode causar um deadlock em que o filtro upstream aguarda o filtro downstream liberar o exemplo, o que nunca acontece porque o filtro downstream está aguardando o filtro upstream. No entanto, se um filtro tiver vários Pins de entrada, um PIN poderá esperar por outro PIN para receber dados. Por exemplo, o filtro [AVI Mux](avi-mux-filter.md) faz isso para que ele possa intercalar dados de áudio e vídeo.

Um PIN pode rejeitar um exemplo por vários motivos:

-   O PIN está sendo liberado (consulte [liberando](flushing.md)).
-   O PIN não está conectado.
-   O filtro está parado.
-   Ocorreu algum outro erro.

O método **Receive** deve retornar S \_ false no primeiro caso e um código de falha nos outros casos. O filtro upstream deve parar de enviar amostras quando o código de retorno é algo diferente de S \_ OK.

Você pode considerar os três primeiros casos como falhas "esperadas", no sentido de que o filtro estava no estado incorreto para receber exemplos. Uma falha inesperada seria aquela que faz com que o PIN rejeite um exemplo, embora o PIN esteja em um estado de recebimento. Se ocorrer um erro desse tipo, o PIN deverá enviar um downstream de notificação de fim de fluxo e enviar um evento de [**\_ ERRORABORT do EC**](ec-errorabort.md) para o Gerenciador do grafo de filtro.

Nas classes base do DirectShow, o método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) verifica os casos de falha gerais, liberando, parou e assim por diante. A classe derivada precisará verificar se há falhas específicas para o filtro. No caso de um erro, o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) envia a notificação de fim de fluxo e o evento de \_ ERRORABORT do EC.

**Modelo de pull: solicitando um exemplo**

Na interface **IAsyncReader** , o pino de entrada solicita amostras do pino de saída chamando um dos seguintes métodos:

-   [**IAsyncReader:: solicitação**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

O método de **solicitação** é assíncrono; o pino de entrada chama [**IAsyncReader:: WaitForNext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) para aguardar a conclusão da solicitação. Os outros dois métodos são síncronos.

**Quando entregar dados**

Um filtro sempre fornece amostras enquanto está no estado executando. Na maioria dos casos, um filtro também fornece amostras enquanto está em pausa. Isso permite que o grafo marque os dados para que a reprodução seja iniciada imediatamente quando a **execução** for chamada (consulte [Estados de filtro](filter-states.md)). Se o filtro não entregar dados enquanto estiver em pausa, o método **IMediaFilter:: GetState** do filtro deverá retornar VFW \_ s não poderá \_ \_ indicar no estado pausado. Esse código de retorno sinaliza o gráfico de filtro para não aguardar dados do filtro antes de concluir a transição de pausa. Caso contrário, o método **Pause** será bloqueado indefinidamente. Para obter um exemplo de código, consulte [**CBaseFilter:: GetState**](cbasefilter-getstate.md).

Aqui estão alguns exemplos de quando um filtro pode precisar retornar VFW \_ S não \_ conseguir a \_ indicação:

-   Fontes dinâmicas, como filtros de captura, não devem enviar dados enquanto estiverem em pausa. Consulte [produzindo dados em um filtro de captura](producing-data-in-a-capture-filter.md).
-   Um filtro de divisão pode ou não enviar dados enquanto estiver em pausa, dependendo da implementação. Se o filtro usar threads separados para enfileirar dados em cada pino de saída, ele poderá enviar dados enquanto estiver em pausa. Mas se o filtro usar um único thread para cada pino de saída, o primeiro PIN poderá bloquear o thread quando ele chamar **Receive**, o que impedirá que os outros Pins enviem dados. Nesse caso, você deve retornar VFW S e não \_ \_ conseguir a \_ indicação.
-   Um filtro pode fornecer dados esporadicamente. Por exemplo, ele pode analisar um fluxo de dados personalizado e filtrar alguns pacotes ao entregar outros. Nesse caso, o filtro pode não ter a garantia de entregar dados enquanto estiver em pausa.

Um filtro de origem (usando o modelo de push) ou um filtro do analisador (usando o modelo push/pull) cria um ou mais threads de streaming, que fornecem amostras o mais rápido possível. Filtros downstream, como decodificadores e transformações, normalmente enviam dados somente quando **Receive** é chamado em seus PINs de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recebendo e entregando exemplos](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



