---
title: Alias de memória e herança de dados
description: O recurso colocado e reservado pode alias de memória física em um heap. Os recursos inseridos permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103683"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Alias de memória e herança de dados

O recurso colocado e reservado pode alias de memória física em um heap. Os recursos inseridos permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos.

-   [Atribuição de alias](#memory-aliasing-and-data-inheritance)
-   [Herança de dados](#data-inheritance)
-   [Tópicos relacionados](#related-topics)

## <a name="aliasing"></a>Atribuição de alias

Uma barreira de alias deve ser emitida entre o uso de dois recursos que compartilham a mesma memória física, mesmo se a herança de dados não for desejada. Modelos de uso simples devem indicar, pelo menos, o recurso de destino envolvido em tal operação. Consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) para obter mais detalhes e modelos de uso avançados.

Depois que um recurso é acessado, todos os recursos que compartilham memória física com esse recurso se tornam invalidados, a menos que a herança de dados tenha permissão para ocorrer. As leituras de recursos invalidados resultam em conteúdos indefinidos de recursos. Gravações em recursos invalidados também resultam em conteúdos indefinidos de recursos, a menos que duas condições ocorram:

-   O recurso não tem o \_ sinalizador de recurso D3D12 \_ \_ permitir destino de \_ renderização \_ ou \_ sinalizador de recurso D3D12 \_ \_ permitir estêncil de \_ profundidade \_ .
-   A gravação é uma operação de cópia ou limpeza em um subrecurso ou bloco inteiro. Bloco-a inicialização só está disponível para recursos com SWIZZLE de blocos de 64 KB \_ \_ indefinidos \_ e SWIZZLE padrão de bloco de 64 KB \_ \_ \_ .

As invalidações sobrepostas são delimitadas a granularidades menores, quando os layouts fornecem informações sobre o local no local dos dados do Texel e quando os recursos estão em determinados Estados de barreira de transição. No entanto, invalidações não podem passar por granularidades de alinhamento de recursos menores do que.

Uma granularidade de alinhamento de buffer é 64 KB, e A granularidade de alinhamento maior tem precedência. Isso é importante ao considerar texturas de 4 KB, pois várias texturas de 4 KB podem residir em uma região de 64 KB sem sobreposição. Mas, um alias de buffer da mesma região de 64 KB não pode ser usado em conjunto com nenhuma dessas texturas de 4 KB. O aplicativo não pode manter o acesso ao buffer de forma confiável, interseccionando as texturas de 4 KB, pois as GPUs são permitidas para dados de textura de 4 KB swizzle na região de 64 KB em um padrão indefinido.

\_ \_ SWIZZLE de blocos indefinidos de 64 KB \_ , SWIZZLE padrão de bloco de 64 KB \_ \_ \_ e \_ layouts de textura de linha principal informam o aplicativo que a granularidade de alinhamento de sobreposição se tornou inválida. Por exemplo: um aplicativo pode criar uma matriz de textura de destino de renderização 2D com duas fatias de matriz, um único nível de MIP e o layout de SWIZZLE de bloco de 64 KB \_ \_ indefinido \_ . Suponha que o aplicativo entenda que cada fatia de matriz ocupa 100 blocos de 64 KB. O aplicativo pode abrem mão usando a fatia de matriz 0 e reutilizar essa memória para um buffer de ~ 6MB, uma textura de ~ 6 MB com layout indefinido, etc. Indo além, suponha que o aplicativo não reprecise mais do primeiro bloco da fatia de matriz 1. Em seguida, o aplicativo também pode localizar um buffer de 64 KB até que o processamento exija novamente o primeiro bloco da fatia de matriz 1. O aplicativo precisaria fazer um bloco inteiro claro ou copiar para reutilizar o primeiro bloco com a matriz de textura novamente.

No entanto, até mesmo texturas com layouts definidos ainda têm casos problemáticos. Os tamanhos de recursos de textura podem ser significativamente diferentes do que o aplicativo pode calcular, pois algumas arquiteturas de adaptador alocam memória extra para texturas a fim de reduzir a largura de banda efetiva durante cenários de renderização comuns. Todas as invalidações nessa região de memória extra fazem com que o recurso inteiro se torne invalidado. Consulte [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) para obter mais detalhes.

## <a name="data-inheritance"></a>Herança de dados

Os recursos colocados permitem a herança de mais dados para texturas, mesmo com layouts de memória indefinidos. Os aplicativos podem imitar os recursos de herança de dados que compartilharam os recursos confirmados, localizando duas texturas com propriedades de recurso idênticas no mesmo deslocamento em um heap compartilhado. A descrição completa do recurso deve ser idêntica, incluindo o valor claro otimizado e o tipo de método de criação de recurso (colocado ou reservado). Porém, os dois recursos podem ter tido Estados de barreira de transição inicial diferentes.

Os recursos reservados habilitam a herança de dados por bloco; Mas as restrições normalmente existem para Estados de barreira de transição de recursos.

Para herdar dados, ambos os recursos devem estar em um estado de barreira de transição de recurso compatível:

-   Para buffers, texturas de acesso simultâneas e texturas de adaptador cruzado, o estado de transição de recurso não é importante e todos os Estados são "compatíveis".
-   Para texturas reservadas sem as propriedades anteriores ou outra herança de dados por bloco por meio de 64 KB de bloco \_ \_ indefinido \_ SWIZZLE ou 64 KB \_ \_ Standard \_ SWIZZLE, o estado de barreira de transição de recursos, incluindo o bloco, deve estar no estado comum.
-   Para todas as outras texturas, em que as descrições de recursos correspondem exatamente, o estado de barreira de transição de recursos para cada par de subrecursos correspondente deve:
    -   Estar no estado comum.
    -   Seja igual quando o estado tiver o mesmo sinalizador de gravação de GPU neles.

Quando a GPU dá suporte a swizzle padrão, os buffers e as texturas swizzle padrão podem ter um alias para a mesma memória e herdar dados entre eles. O aplicativo pode manipular texels da representação de buffer, pois o padrão swizzle padrão descreve como os texels são dispostos na memória. O padrão swizzle visível da CPU é equivalente ao padrão swizzle visível da GPU visto em buffers.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subalocação dentro de heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




