---
description: Sobre exemplos de mídia e alocadores
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Sobre exemplos de mídia e alocadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9390bd99ab019effa40f9edca1f8d9e03ea73c5b0085ed8b1bc13f013cad6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430276"
---
# <a name="about-media-samples-and-allocators"></a>Sobre exemplos de mídia e alocadores

Os filtros entregam dados entre conexões de pino. Os dados são movimentados do pino de saída de um filtro para o pino de entrada de outro filtro. A maneira mais comum para o pin de saída entregar os dados é chamando o método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) na entrada, embora também existam alguns outros mecanismos.

Dependendo do filtro, a memória para os dados de mídia pode ser alocada de várias maneiras: no heap, em uma superfície directDraw, usando memória GDI compartilhada ou usando algum outro mecanismo de alocação. O objeto responsável por alocar a memória é chamado de *alocador*, que é um objeto COM que expõe a interface [**IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Quando dois pinos se conectam, um dos pinos deve fornecer um alocador. DirectShow define uma sequência de chamadas de método usada para estabelecer qual pino fornece o alocador. Os pinos também concorda com o número de buffers que o alocador criará e o tamanho dos buffers.

Antes do início do streaming, o alocador cria um pool de buffers. Durante o streaming, o filtro upstream preenche buffers com dados e os entrega ao filtro downstream. Mas o filtro upstream não dá ao filtro downstream ponteiros brutos para os buffers. Em vez disso, ele usa objetos COM chamados *amostras de mídia*, que o alocador cria para gerenciar os buffers. Exemplos de mídia expõem a interface [**IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Um exemplo de mídia contém:

-   um ponteiro para o buffer subjacente
-   um carimbo de data/hora
-   vários sinalizadores
-   opcionalmente, um tipo de mídia

O carimbo de data/hora define a hora da apresentação, que o filtro do renderdor usa para agendar a renderização. Os sinalizadores indicam coisas como se houve uma quebra nos dados desde o exemplo anterior. O tipo de mídia fornece uma maneira para os filtros alterarem os formatos no meio do fluxo. Normalmente, o exemplo não tem nenhum tipo de mídia, o que indica que o formato não foi alterado desde o exemplo anterior.

Enquanto um filtro está usando um buffer, ele mantém a contagem de referência no exemplo. O alocador usa a contagem de referência para determinar quando ele pode usar o buffer. Isso impede que um filtro sobrescreva um buffer que outro filtro ainda está usando. Um exemplo não retorna ao pool do alocador de amostras disponíveis até que cada filtro o tenha liberado.

Para obter mais informações, consulte estes tópicos:

-   O tópico [Exemplos e Alocadores](samples-and-allocators.md) fornece uma descrição mais detalhada de como os alocadores funcionam.
-   O tópico [Data Flow no filtro Graph](data-flow-in-the-filter-graph.md) fornece uma visão geral do fluxo de dados DirectShow.

Os tópicos a seguir destinam-se a desenvolvedores que estão escrevendo seus próprios filtros personalizados:

-   [Dados Flow para desenvolvedores de filtro](data-flow-for-filter-developers.md)
-   [Threads e seções críticas](threads-and-critical-sections.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O filtro Graph e seus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



