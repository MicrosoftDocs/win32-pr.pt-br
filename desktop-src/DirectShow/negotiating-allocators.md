---
description: Negociando alocadores
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Negociando alocadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780047"
---
# <a name="negotiating-allocators"></a>Negociando alocadores

Quando dois Pins se conectam, eles precisam de um mecanismo para a troca de dados de mídia. Esse mecanismo é chamado de *transporte*. Em geral, a arquitetura do DirectShow é neutra em relação aos transportes. Dois filtros podem concordar em se conectar usando qualquer transporte com suporte.

O transporte mais comum é o transporte de *memória local* , no qual os dados de mídia residem na memória principal. Existem dois tipos de transporte de memória local, o *modelo de push* e o modelo de *pull*. No modelo de push, o filtro de origem envia dados por push para o filtro downstream, usando a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) no pino de entrada do filtro downstream. No modelo de pull, o filtro downstream solicita dados do filtro de origem, usando a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) no pino de saída do filtro de origem. Para obter mais informações sobre esses dois modelos de fluxo de dados, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).

No transporte de memória local, o objeto responsável pela alocação de buffers de memória é chamado de *alocador*. Um alocador dá suporte à interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Ambos os Pins compartilham um único alocador. O PIN pode fornecer um alocador, mas o PIN de saída seleciona qual alocador usar.

O PIN de saída também define as propriedades do alocador, que determinam quantos buffers são criados pelo alocador, o tamanho de cada buffer e o alinhamento da memória. O pino de saída pode adiar para o pino de entrada para os requisitos de buffer.

Em uma conexão **IMemInputPin** , a negociação de alocador funciona da seguinte maneira:

1.  Opcionalmente, o pino de saída chama [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Esse método recupera os requisitos de buffer do pino de entrada, como o alinhamento de memória. Em geral, o pino de saída deve respeitar a solicitação do pino de entrada, a menos que haja um bom motivo para não.
2.  Opcionalmente, o pino de saída chama [**IMemInputPin:: Getalocador**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Esse método solicita um alocador do PIN de entrada. O PIN de entrada fornece um ou retorna um código de erro.
3.  O pino de saída seleciona um alocador. Ele pode usar um fornecido pelo PIN de entrada ou criar seu próprio.
4.  O pino de saída chama [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) para definir as propriedades do alocador. No entanto, o alocador pode não honrar as propriedades solicitadas. (Por exemplo, isso pode acontecer se o PIN de entrada fornecer o alocador.) O alocador retorna as propriedades reais como um parâmetro de saída no método **SetProperties** .
5.  O outpin chama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para informar o pino de entrada da seleção.
6.  O pino de entrada deve chamar [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) para verificar se as propriedades do alocador são aceitáveis.
7.  O pino de saída é responsável por confirmar e desconfirmar o alocador. Isso ocorre quando o streaming começa e para.

Em uma conexão **IAsyncReader** , a negociação de alocador funciona da seguinte maneira:

1.  O pino de entrada chama [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) no pino de saída. O PIN de entrada especifica seus requisitos de buffer e, opcionalmente, fornece um alocador.
2.  O pino de saída seleciona um alocador. Ele pode usar aquele fornecido pelo PIN de entrada, se houver, ou criar seu próprio.
3.  O pino de saída retorna o alocador como um parâmetro de saída no método **RequestAllocator** . O PIN de entrada deve verificar as propriedades do alocador.
4.  O PIN de entrada é responsável por confirmar e desconfirmar o alocador.
5.  A qualquer momento durante o processo de negociação de alocador, o PIN pode falhar na conexão.
6.  Se o pino de saída usar o alocador do pino de entrada, ele poderá usar esse alocador somente para fornecer amostras para esse pino de entrada. O filtro proprietário não deve usar o alocador para fornecer amostras a outros Pins.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fornecendo um alocador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 



