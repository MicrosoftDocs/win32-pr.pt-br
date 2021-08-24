---
title: Consultas
description: No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta. Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usadas com esse heap.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241946"
---
# <a name="queries"></a>Consultas

No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta. Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usadas com esse heap.

-   [Diferenças nas consultas do Direct3D 11 ao Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Heaps de consulta](#query-heaps)
-   [Criando heaps de consulta](#creating-query-heaps)
-   [Extraindo dados de uma consulta](#extracting-data-from-a-query)
-   [Tópicos relacionados](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Diferenças nas consultas do Direct3D 11 ao Direct3D 12

Os tipos de consulta a seguir não estão mais presentes no Direct3D 12, sua funcionalidade que está sendo incorporada a outros processos:

-   **Consultas de evento** -a funcionalidade de evento agora é manipulada por limites.
-   **Consultas de carimbo de data/hora não contíguos** -os relógios de GPU podem ser definidos para um estado estável no Direct3D 12 (consulte a seção de [tempo](timing.md) ). As comparações de relógio de GPU não são significativas se a GPU estiver ociosa entre os carimbos de data/hora (conhecido como uma consulta não-junção). Com uma potência estável, as consultas de carimbo de data/hora são emitidas de diferentes listas de comandos com confiança. Dois carimbos de data/hora dentro da mesma lista de comandos são sempre comparáveis com confiança.
-   **Consultas de estatísticas de saída de fluxo** – no Direct3D 12, não há uma consulta de estouro de saída de fluxo único (SO) para todos os fluxos de saída. Os aplicativos precisam emitir várias consultas de fluxo único e, em seguida, correlacionar os resultados.
-   As consultas de predicado de **Estatísticas de saída de fluxo e oclusão** -consultas (que gravam na memória) e [predicação](predication.md) (que lê da memória) não são mais acopladas e, portanto, esses tipos de consulta não são necessários.

Um novo tipo de consulta oclusão binária foi adicionado ao Direct3D 12. Isso permite estratégias de predicação que se preocupam apenas com um objeto totalmente obstruído ou não (em vez de quantos pixels foram obstruído) para indicar isso ao dispositivo, o que pode ser capaz de executar as consultas com mais eficiência.

## <a name="query-heaps"></a>Heaps de consulta

As consultas podem ser um de vários tipos ([**tipo de \_ \_ heap de \_ consulta D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) e agrupadas em heaps de consulta antes de serem enviadas para a GPU.

Um novo tipo de consulta D3D12 tipo de consulta \_ \_ \_ Binary \_ oclusão está disponível e atua como D3D12 \_ tipo de consulta \_ \_ oclusão, exceto pelo fato de que ele retorna um resultado binário 0/1:0 indica que nenhum exemplo passou no teste de profundidade e de estêncil, 1 indica que pelo menos uma amostra passou por profundidade e teste de estêncil. Isso permite que as consultas do oclusão não interfiram com nenhuma otimização de desempenho de GPU associada a testes de profundidade/estêncil.

## <a name="creating-query-heaps"></a>Criando heaps de consulta

As APIs relevantes para a criação de heaps de consulta são o [**tipo de \_ \_ heap \_ de consulta D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)de enumeração, a [**D3D12 de \_ heap de consulta \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)de struct e o método [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

O tempo de execução principal validará que o tipo de heap de consulta é um membro válido da enumeração de [**\_ \_ tipo de heap D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) e que a contagem é maior que 0.

Cada elemento de consulta individual dentro de um heap de consulta pode ser iniciado e interrompido separadamente.

As APIs para usar os heaps de consulta são o [**\_ \_ tipo de consulta enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)e os métodos [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

\_ \_ Tipo de consulta D3D12 \_ carimbo de data/hora é a única consulta que dá suporte somente [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) . Todos os outros tipos de consulta exigem [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e **endquery**.

A camada de depuração validará o seguinte:

-   É ilegal iniciar uma consulta de carimbo de data/hora &mdash; que só pode ser encerrada
-   É ilegal iniciar uma consulta duas vezes sem terminá-la (para um determinado elemento). Para consultas que exigem início e término, é ilegal encerrar uma consulta antes do início correspondente (para um determinado elemento).
-   O tipo de consulta passado para [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) deve corresponder ao tipo de consulta passado para [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

O tempo de execução principal validará o seguinte:

-   [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) não pode ser chamado em uma consulta de carimbo de data/hora.
-   Para os tipos de consulta que dão suporte a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (todos, exceto para carimbo de data/hora), uma consulta para um determinado elemento não deve abranger limites de lista de comandos.
-   *ElementIndex* deve estar dentro do intervalo.
-   O tipo de consulta é um membro válido da enumeração de [**\_ \_ tipo de consulta D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) .
-   O tipo de consulta deve ser compatível com o heap de consulta. A tabela a seguir mostra o tipo de heap de consulta necessário para cada tipo de consulta:

    

    | Tipo de consulta                                  | Tipo de heap de consulta                                |
    |---------------------------------------------|------------------------------------------------|
    | \_Tipo de consulta D3D12 \_ \_ oclusão               | D3D12 \_ tipo de heap de consulta \_ \_ \_ oclusão            |
    | \_Tipo de consulta D3D12 \_ \_ Binary \_ oclusão       | D3D12 \_ tipo de heap de consulta \_ \_ \_ oclusão            |
    | \_Tipo de consulta D3D12 carimbo de \_ \_ data/hora               | \_Carimbo de \_ \_ \_ data/hora do tipo heap de consulta D3D12            |
    | \_Tipo de consulta D3D12 \_ \_ Estatísticas de pipeline \_    | \_Estatísticas de \_ pipeline do tipo de heap de consulta D3D12 \_ \_ \_ |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM0 | \_Tipo de heap de consulta D3D12 \_ \_ \_ para \_ estatísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM1 | \_Tipo de heap de consulta D3D12 \_ \_ \_ para \_ estatísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM2 | \_Tipo de heap de consulta D3D12 \_ \_ \_ para \_ estatísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM3 | \_Tipo de heap de consulta D3D12 \_ \_ \_ para \_ estatísticas       |

    

     

-   O tipo de consulta é suportado pelo tipo de lista de comandos. A tabela a seguir mostra quais consultas têm suporte em quais tipos de lista de comandos.

    

    | Tipo de consulta                                  | Tipos de lista de comandos com suporte         |
    |---------------------------------------------|--------------------------------------|
    | \_Tipo de consulta D3D12 \_ \_ oclusão               | Direto                               |
    | \_Tipo de consulta D3D12 \_ \_ Binary \_ oclusão       | Direto                               |
    | \_Tipo de consulta D3D12 carimbo de \_ \_ data/hora               | Cópia direta, de computação e opcional |
    | \_Tipo de consulta D3D12 \_ \_ Estatísticas de pipeline \_    | Direto                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM0 | Direto                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM1 | Direto                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM2 | Direto                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estatísticas \_ STREAM3 | Direto                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extraindo dados de uma consulta

A maneira de extrair dados de uma consulta é usar o método [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) . O **ResolveQueryData** funciona com todos os tipos de memória (se eles são memória do sistema ou memória local do dispositivo), mas requer que o recurso de destino esteja em [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). 

## <a name="related-topics"></a>Tópicos relacionados

* [Contadores e consultas](counters-and-queries.md)
* [Passo a passo de consultas do predicação](predication-queries.md)
