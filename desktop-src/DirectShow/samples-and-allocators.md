---
description: Exemplos e alocadores
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Exemplos e alocadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551410"
---
# <a name="samples-and-allocators"></a>Exemplos e alocadores

Quando um PIN entrega dados de mídia para outro PIN, ele não passa um ponteiro direto para o buffer de memória. Em vez disso, ele fornece um ponteiro para um objeto COM que gerencia a memória. Esse objeto, chamado de *exemplo de mídia*, expõe a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . O PIN de recebimento acessa o buffer de memória chamando métodos **IMediaSample** , como [**IMediaSample:: getpointr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)e [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength).

Os exemplos sempre viajam downstream, do pino de saída para o pino de entrada. No modelo de push, o pino de saída entrega um exemplo chamando [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada. O PIN de entrada processará os dados de forma síncrona (ou seja, completamente dentro do método **Receive** ) ou o processará de maneira assíncrona em um thread de trabalho. O PIN de entrada tem permissão para bloquear dentro do método **Receive** , se precisar aguardar recursos.

Outro objeto COM, chamado de *alocador*, é responsável por criar e gerenciar exemplos de mídia. Os alocadores expõem a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Sempre que um filtro precisa de um exemplo de mídia com um buffer vazio, ele chama o método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , que retorna um ponteiro para o exemplo. Cada conexão de PIN compartilha um alocador. Quando dois Pins se conectam, eles decidem qual filtro fornecerá o alocador. Os Pins também definem as propriedades no alocador, como o número de buffers e o tamanho de cada buffer. (Para obter detalhes, consulte [como os filtros se conectam](how-filters-connect.md) e [negociam os alocadores](negotiating-allocators.md).)

A ilustração a seguir mostra as relações entre o alocador, os exemplos de mídia e o filtro.

![exemplos de mídia e alocadores](images/mediasamples.png)

**Contagens de referência de exemplo de mídia**

Um alocador cria um pool finito de exemplos. A qualquer momento, alguns exemplos podem estar em uso, enquanto outros estão disponíveis para chamadas **GetBuffer** . O alocador usa a contagem de referência para acompanhar os exemplos. O método **GetBuffer** retorna um exemplo com uma contagem de referência de 1. Se a contagem de referência chegar a zero, o exemplo voltará para o pool do alocador, onde ele poderá ser usado na próxima chamada **GetBuffer** . Desde que a contagem de referência permaneça acima de zero, o exemplo não estará disponível para **GetBuffer**. Se cada amostra pertencente ao alocador estiver em uso, o método **GetBuffer** será bloqueado até que um exemplo se torne disponível.

Por exemplo, suponha que um PIN de entrada receba um exemplo. Se ele processa o exemplo de forma síncrona, dentro do método **Receive** , ele não incrementa a contagem de referência. Após **Receive** Returns, o pino de saída libera o exemplo, a contagem de referência vai para zero e o exemplo retorna ao pool do alocador. Por outro lado, se o pino de entrada processar o exemplo em um thread de trabalho, ele incrementará a contagem de referência antes de sair do método **Receive** . A contagem de referência agora é 2. Quando o pino de saída libera o exemplo, a contagem vai para 1; o exemplo ainda não retorna ao pool. Depois que o thread de trabalho é concluído com o exemplo, ele chama **Release** para liberar o exemplo. Agora, o exemplo retorna ao pool.

Quando um PIN recebe um exemplo, ele pode copiar os dados para outro exemplo ou pode modificar o exemplo original e entregá-lo para o próximo filtro. Potencialmente, um exemplo pode viajar toda a duração do grafo, cada filtro chamando **AddRef** e **Release** por vez. Portanto, o pino de saída nunca deve reutilizar um exemplo depois de chamar **Receive**, pois um filtro downstream pode estar usando o exemplo. O pino de saída deve sempre chamar **GetBuffer** para obter um novo exemplo.

Esse mecanismo reduz a quantidade de alocação de memória, pois os filtros reutilizam os mesmos buffers. Ele também impede que os filtros gravem acidentalmente dados que não foram processados, pois o alocador mantém uma lista de exemplos disponíveis.

Um filtro pode usar alocadores separados para entrada e saída. Isso poderá fazer isso se expandir os dados de entrada (por exemplo, descompactando-os). Se a saída não for maior que a entrada, um filtro poderá processar os dados no local, sem copiá-los para um novo exemplo. Nesse caso, duas ou mais conexões de PIN podem compartilhar um alocador.

**Confirmando e confirmando alocadores**

Quando um filtro cria primeiro um alocador, o alocador não reservou nenhum buffer de memória. Neste ponto, todas as chamadas para o método **GetBuffer** falharão. Quando o streaming começa, o pino de saída chama [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit), que confirma o alocador, fazendo com que ele aloque memória. Os Pins agora podem chamar **GetBuffer**.

Quando o streaming é interrompido, o PIN chama [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit), que desconfirma o alocador. Todas as chamadas subsequentes para **GetBuffer** falham até que o alocador seja confirmado novamente. Além disso, se todas as chamadas para **GetBuffer** estiverem atualmente bloqueadas aguardando um exemplo, elas retornarão imediatamente um código de falha. O método de **desconfirmação** pode ou não liberar a memória, dependendo da implementação. Por exemplo, a classe [**CMemAllocator**](cmemallocator.md) aguarda até que seu método destruidor Libere memória.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
