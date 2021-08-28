---
description: Relógios de referência
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Relógios de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ad0a262b36ce78c6a2f355b30b3c6876c7e78a7807970592b6f15287c0e2c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697106"
---
# <a name="reference-clocks"></a>Relógios de referência

Uma função do Gerenciador de Graph filtro é sincronizar todos os filtros no grafo com o mesmo relógio, chamado de *relógio de referência*.

Qualquer objeto que expõe a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) pode atuar como o relógio de referência. O relógio de referência pode ser fornecido por um filtro DirectShow , normalmente o renderdor de áudio, que tem acesso a um temporizador de hardware. Como um fallback, o Gerenciador de Graph filtro pode usar a hora do sistema.

Nominalmente, um relógio de referência mede o tempo em intervalos de 100 nanossegundos, embora a precisão real do relógio possa ser menor. Para recuperar a hora atual do relógio, chame o [**método IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) A linha de base do relógio , a hora da qual ele começa a contar, depende da implementação, portanto, o valor retornado por **GetTime** não é inerentemente significativo. O que importa é o delta de quando o grafo começou a ser executado.

Embora a precisão de um relógio de referência possa variar, os tempos retornados pelo [**método GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) têm a garantia de aumentar monotônicamente. Em outras palavras, os tempos de relógio nunca voltarão. Se um relógio de referência estiver gerando tempos de relógio de uma fonte de hardware e o relógio de hardware pular para trás (por exemplo, se houver um ajuste no relógio), o método **GetTime** deverá continuar retornando a hora relatada pela última vez até que o relógio de hardware seja atualizado. Para obter mais informações, consulte [**Classe CBaseReferenceClock**](cbasereferenceclock.md).

**Relógio de referência padrão**

O Gerenciador Graph Filtro seleciona automaticamente um relógio de referência quando o grafo é executado. Ele usa o seguinte algoritmo para selecionar o relógio:

-   Se o aplicativo tiver selecionado um relógio (veja abaixo), use esse relógio.
-   Se o grafo contiver um filtro de origem dinâmico que dá suporte [**a IReferenceClock,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)use esse filtro. Para a definição de uma fonte ao vivo, consulte [Fontes ao vivo.](live-sources.md)
-   Se o grafo NÃO contiver nenhum filtro de origem ao vivo, use qualquer filtro no grafo que dá suporte a [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), começando nos renderadores e trabalhando upstream. Prefira filtros conectados em vez de filtros não conectados. (Se o grafo estiver renderizar um fluxo de áudio, essa etapa no algoritmo normalmente selecionará o filtro do renderador de áudio.)
-   Se nenhum filtro fornece um relógio adequado, use o Relógio de [Referência do](system-reference-clock.md)Sistema , que se baseia na hora do sistema.

**Definindo o relógio de referência**

Um aplicativo pode selecionar um relógio chamando o método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador Graph Filtro. Você só deve fazer isso se tiver um motivo específico para preferir outro relógio.

Você pode instruir o Gerenciador Graph Filtro a não usar um relógio de referência chamando [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) com o valor **NULL**. Por exemplo, você pode fazer isso para processar amostras o mais rápido possível. Para restaurar o relógio de referência padrão, chame o método [**IFilterGraph::SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) no Gerenciador Graph Filtro.

Sempre que o relógio de referência muda, o Gerenciador Graph Filtrar notifica cada filtro chamando seu [**método IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) Os aplicativos nunca devem chamar esse método em filtros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo o Graph relógio](setting-the-graph-clock.md)
</dt> <dt>

[Hora e relógios em DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



