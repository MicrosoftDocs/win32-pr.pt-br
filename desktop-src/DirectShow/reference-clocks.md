---
description: Relógios de referência
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Relógios de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778427"
---
# <a name="reference-clocks"></a>Relógios de referência

Uma função do Gerenciador de gráficos de filtro é sincronizar todos os filtros no grafo com o mesmo relógio, chamado *relógio de referência*.

Qualquer objeto que expõe a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) pode atuar como o relógio de referência. O relógio de referência pode ser fornecido por um filtro do DirectShow — normalmente o processador de áudio, que tem acesso a um temporizador de hardware. Como um fallback, o Gerenciador do grafo de filtro pode usar a hora do sistema.

No mínimo, um relógio de referência mede o tempo em intervalos de 100 nanossegundos, embora a precisão real do relógio possa ser menor. Para recuperar a hora atual do relógio, chame o método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) . A linha de base do relógio — o tempo de início da contagem — depende da implementação, de modo que o valor retornado por **getTime** não é inerentemente significativo. O que importa é o Delta de quando o grafo começou a ser executado.

Embora a precisão de um relógio de referência possa variar, os tempos retornados pelo método [**getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) têm a garantia de aumentar o monotônico. Em outras palavras, os horários do relógio nunca serão revertidos. Se um relógio de referência estiver gerando tempos de relógio de uma fonte de hardware e o relógio de hardware saltar para trás (por exemplo, se houver um ajuste no relógio), o método **getTime** deverá continuar a retornar o último tempo relatado até que o relógio de hardware seja atualizado. Para obter mais informações, consulte [**classe CBaseReferenceClock**](cbasereferenceclock.md).

**Relógio de referência padrão**

O Gerenciador de gráfico de filtro seleciona automaticamente um relógio de referência quando o grafo é executado. Ele usa o seguinte algoritmo para selecionar o relógio:

-   Se o aplicativo tiver selecionado um relógio (veja abaixo), use esse relógio.
-   Se o grafo contiver um filtro de origem ao vivo que dá suporte a [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), use esse filtro. Para obter a definição de uma fonte dinâmica, consulte [fontes dinâmicas](live-sources.md).
-   Se o grafo não contiver nenhum filtro de origem ao vivo, use todos os filtros no grafo que ofereçam suporte a [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), começando com os renderizadores e trabalhando upstream. Prefira filtros conectados em filtros não conectados. (Se o grafo estiver renderizando um fluxo de áudio, essa etapa no algoritmo normalmente selecionará o filtro de processador de áudio.)
-   Se nenhum filtro fornecer um relógio adequado, use o [relógio de referência do sistema](system-reference-clock.md), que se baseia na hora do sistema.

**Configurando o relógio de referência**

Um aplicativo pode selecionar um relógio chamando o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador de gráfico de filtro. Você deve fazer isso somente se tiver um motivo específico para preferir outro relógio.

Você pode instruir o Gerenciador do grafo de filtro a não usar um relógio de referência chamando [**Setsyncprovider**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) com o valor **NULL**. Por exemplo, você pode fazer isso para processar amostras o mais rápido possível. Para restaurar o relógio de referência padrão, chame o método [**IFilterGraph:: SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) no Gerenciador do grafo de filtro.

Sempre que o relógio de referência é alterado, o Gerenciador de gráfico de filtro notifica cada filtro chamando o método [**IMediaFilter:: setsync**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) . Os aplicativos nunca devem chamar esse método em filtros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o relógio do grafo](setting-the-graph-clock.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



