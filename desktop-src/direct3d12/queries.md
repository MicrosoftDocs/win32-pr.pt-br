---
title: Consultas
description: No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta. Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usados com esse heap.
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

No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta. Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usados com esse heap.

-   [Diferenças nas consultas do Direct3D 11 para o Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Heaps de consulta](#query-heaps)
-   [Criando heaps de consulta](#creating-query-heaps)
-   [Extraindo dados de uma consulta](#extracting-data-from-a-query)
-   [Tópicos relacionados](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Diferenças nas consultas do Direct3D 11 para o Direct3D 12

Os seguintes tipos de consulta não estão mais presentes no Direct3D 12, sua funcionalidade sendo incorporada em outros processos:

-   **Consultas de evento** – o evento agora é tratado por cercas.
-   **Consultas de data/hora** não adjacentes – os relógios de GPU podem ser definidos como um estado estável no Direct3D 12 (consulte a [seção Tempo).](timing.md) As comparações de relógio de GPU não serão significativas se a GPU estiver ociosa entre osstamps de data/hora (conhecido como uma consulta desconstância). Com potência estável, duas consultas de timestamp emitidas de listas de comandos diferentes são comparáveis de forma confiável. Dois timestamps dentro da mesma lista de comandos são sempre comparáveis de forma confiável.
-   **Consultas de estatísticas de saída** de fluxo – no Direct3D 12, não há nenhuma consulta de estouro de so (saída de fluxo único) para todos os fluxos de saída. Os aplicativos precisam emitir várias consultas de fluxo único e correlacionar os resultados.
-   Consultas de predicado de predicado de **oclusão** e estatísticas de saída de fluxo – consultas (que são escritas na memória) e [Predication](predication.md) (que lê da memória) não são mais alocadas e, portanto, esses tipos de consulta não são necessários.

Um novo tipo de consulta de oclusão binária foi adicionado ao Direct3D 12. Isso permite que estratégias de predicação que se importam apenas se um objeto foi totalmente ocluído ou não (em vez de quantos pixels foram ocluídos) para indicar isso para o dispositivo, que pode ser capaz de executar as consultas com mais eficiência.

## <a name="query-heaps"></a>Heaps de consulta

As consultas podem ser uma de vários tipos ([**D3D12 \_ QUERY \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) e são agrupadas em heaps de consulta antes de serem enviadas para a GPU.

Um novo tipo de consulta D3D12 QUERY TYPE BINARY OCCLUSION está disponível e atua como \_ \_ \_ \_ D3D12 QUERY TYPE OCCLUSION, exceto pelo fato de que ele retorna um resultado binário \_ \_ de \_ 0/1: 0 indica que nenhuma amostra passou de profundidade e teste de estêncil, 1 indica que pelo menos uma amostra passou de profundidade e teste de estêncil. Isso permite que as consultas de oclusão não interfiram em nenhuma otimização de desempenho de GPU associada ao teste de profundidade/estêncil.

## <a name="creating-query-heaps"></a>Criando heaps de consulta

As APIs relevantes para a criação de heaps de consulta são a enum [**D3D12 \_ QUERY \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type), o [**Struct D3D12 \_ QUERY HEAP \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)e o [**método CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

O runtime principal validará se o tipo de heap de consulta é um membro válido da enumeração [**D3D12 \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) e se a contagem é maior que 0.

Cada elemento de consulta individual dentro de um heap de consulta pode ser iniciado e interrompido separadamente.

As APIs para usar os heaps de consulta são a enum [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)e os métodos [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) [**e EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

D3D12 TIPO DE CONSULTA TIMESTAMP é a única consulta que dá \_ \_ suporte apenas a \_ [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) Todos os outros tipos de consulta [**exigem BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) **e EndQuery.**

A camada de depuração validará o seguinte:

-   É ilegal iniciar uma consulta de data/hora que &mdash; você só pode encerrar
-   É ilegal iniciar uma consulta duas vezes sem finalá-la (para um determinado elemento). Para consultas que exigem início e término, é ilegal encerrar uma consulta antes do início correspondente (para um determinado elemento).
-   O tipo de consulta passado para [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) deve corresponder ao tipo de consulta passado para [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)

O runtime principal validará o seguinte:

-   [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) não pode ser chamado em uma consulta de data/hora.
-   Para os tipos de consulta que suportam [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (todos, exceto o timestamp), uma consulta para um determinado elemento não deve abranger limites da lista de comandos.
-   *ElementIndex deve* estar dentro do intervalo.
-   O tipo de consulta é um membro válido da enum [**D3D12 \_ QUERY \_ TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)
-   O tipo de consulta deve ser compatível com o heap de consulta. A tabela a seguir mostra o tipo de heap de consulta necessário para cada tipo de consulta:

    

    | Tipo de consulta                                  | Tipo de heap de consulta                                |
    |---------------------------------------------|------------------------------------------------|
    | OCLUSÃO DE TIPO \_ \_ DE CONSULTA D3D12 \_               | OCLUSÃO DO TIPO HEAP DE CONSULTA D3D12 \_ \_ \_ \_            |
    | OCLUSÃO BINÁRIA DO TIPO DE CONSULTA D3D12 \_ \_ \_ \_       | OCLUSÃO DO TIPO HEAP DE CONSULTA D3D12 \_ \_ \_ \_            |
    | D3D12 \_ TIPO DE CONSULTA \_ \_ TIMESTAMP               | D3D12 \_ TIPO DE HEAP DE CONSULTA \_ \_ \_ TIMESTAMP            |
    | ESTATÍSTICAS DE PIPELINE DO TIPO DE CONSULTA D3D12 \_ \_ \_ \_    | D3D12 \_ QUERY \_ HEAP TYPE \_ PIPELINE \_ \_ STATISTICS (ESTATÍSTICAS DE PIPELINE DO TIPO HEAP DE CONSULTA D3D12) |
    | TIPO DE CONSULTA D3D12 \_ \_ PARA FLUXO DE \_ \_ \_ ESTATÍSTICAS0 | TIPO DE HEAP DE CONSULTA D3D12 \_ \_ PARA \_ \_ \_ ESTATÍSTICAS       |
    | TIPO DE CONSULTA D3D12 \_ \_ PARA FLUXO DE \_ \_ \_ ESTATÍSTICAS1 | TIPO DE HEAP DE CONSULTA D3D12 \_ \_ PARA \_ \_ \_ ESTATÍSTICAS       |
    | D3D12 \_ TIPO DE CONSULTA PARA FLUXO DE \_ \_ \_ \_ ESTATÍSTICAS2 | TIPO DE HEAP DE CONSULTA D3D12 \_ \_ PARA \_ \_ \_ ESTATÍSTICAS       |
    | D3D12 \_ TIPO DE CONSULTA PARA FLUXO DE \_ \_ \_ \_ ESTATÍSTICAS3 | TIPO DE HEAP DE CONSULTA D3D12 \_ \_ PARA \_ \_ \_ ESTATÍSTICAS       |

    

     

-   O tipo de consulta é suportado pelo tipo de lista de comandos. A tabela a seguir mostra quais consultas têm suporte em quais tipos de lista de comandos.

    

    | Tipo de consulta                                  | Tipos de lista de comandos com suporte         |
    |---------------------------------------------|--------------------------------------|
    | OCLUSÃO DE TIPO \_ \_ DE CONSULTA D3D12 \_               | Direto                               |
    | OCLUSÃO BINÁRIA DO TIPO DE CONSULTA D3D12 \_ \_ \_ \_       | Direto                               |
    | D3D12 \_ TIPO DE CONSULTA \_ \_ TIMESTAMP               | Direct, Compute e, opcionalmente, Copiar |
    | ESTATÍSTICAS DE PIPELINE DO TIPO DE CONSULTA D3D12 \_ \_ \_ \_    | Direto                               |
    | TIPO DE CONSULTA D3D12 \_ \_ PARA FLUXO DE \_ \_ \_ ESTATÍSTICAS0 | Direto                               |
    | TIPO DE CONSULTA D3D12 \_ \_ PARA FLUXO DE \_ \_ \_ ESTATÍSTICAS1 | Direto                               |
    | D3D12 \_ TIPO DE CONSULTA PARA FLUXO DE \_ \_ \_ \_ ESTATÍSTICAS2 | Direto                               |
    | D3D12 \_ TIPO DE CONSULTA PARA FLUXO DE \_ \_ \_ \_ ESTATÍSTICAS3 | Direto                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extraindo dados de uma consulta

A maneira de extrair dados de uma consulta é usar o [**método ResolveQueryData.**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) **ResolveQueryData funciona** com todos os tipos de memória (sejam eles memória do sistema ou memória local do dispositivo), mas exige que o recurso de destino seja D3D12_RESOURCE_STATE_COPY_DEST [**.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 

## <a name="related-topics"></a>Tópicos relacionados

* [Contadores e consultas](counters-and-queries.md)
* [Passo a passo de consultas de pré-sindical](predication-queries.md)
