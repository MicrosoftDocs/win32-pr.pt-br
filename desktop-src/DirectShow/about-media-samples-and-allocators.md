---
description: Sobre exemplos de mídia e alocadores
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Sobre exemplos de mídia e alocadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782858"
---
# <a name="about-media-samples-and-allocators"></a>Sobre exemplos de mídia e alocadores

Os filtros entregam dados entre conexões de PIN. Os dados se movem do pino de saída de um filtro para o pino de entrada de outro filtro. A maneira mais comum para o pino de saída entregar os dados é chamar o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) na entrada, embora alguns outros mecanismos também existam.

Dependendo do filtro, a memória para os dados de mídia pode ser alocada de várias maneiras: no heap, em uma superfície do DirectDraw, usando a memória GDI compartilhada ou usando algum outro mecanismo de alocação. O objeto responsável pela alocação da memória é chamado de *alocador*, que é um objeto com que expõe a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Quando dois Pins se conectam, um dos Pins deve fornecer um alocador. O DirectShow define uma sequência de chamadas de método que é usada para estabelecer qual PIN fornece o alocador. Os Pins também concordam com o número de buffers que o alocador criará e o tamanho dos buffers.

Antes de o streaming começar, o alocador cria um pool de buffers. Durante o streaming, o filtro upstream preenche os buffers com os dados e os entrega para o filtro downstream. Mas o filtro upstream não fornece os ponteiros brutos do filtro downstream para os buffers. Em vez disso, ele usa objetos COM chamados *amostras de mídia*, que o alocador cria para gerenciar os buffers. Amostras de mídia expõem a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Um exemplo de mídia contém:

-   um ponteiro para o buffer subjacente
-   um carimbo de data/hora
-   vários sinalizadores
-   Opcionalmente, um tipo de mídia

O carimbo de data/hora define o tempo de apresentação, que o filtro de processador usa para agendar a renderização. Os sinalizadores indicam coisas como se houvesse uma interrupção nos dados desde o exemplo anterior. O tipo de mídia fornece uma maneira de filtros para alterar os formatos intermediários. Normalmente, o exemplo não tem nenhum tipo de mídia, o que indica que o formato não foi alterado desde o exemplo anterior.

Embora um filtro esteja usando um buffer, ele mantém a contagem de referência no exemplo. O alocador usa a contagem de referência para determinar quando ele pode usar novamente o buffer. Isso impede que um filtro substitua um buffer que outro filtro ainda está usando. Um exemplo não retorna ao pool de exemplos disponíveis do alocador até que todos os filtros o tenham liberado.

Para mais informações, consulte os seguintes tópicos:

-   O tópico [exemplos e alocadores](samples-and-allocators.md) fornece uma descrição mais detalhada de como os alocadores funcionam.
-   O tópico [fluxo de dados no gráfico de filtro](data-flow-in-the-filter-graph.md) fornece uma visão geral do fluxo de dados no DirectShow.

Os tópicos a seguir destinam-se a desenvolvedores que estão escrevendo seus próprios filtros personalizados:

-   [Fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md)
-   [Threads e seções críticas](threads-and-critical-sections.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O gráfico de filtro e seus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



