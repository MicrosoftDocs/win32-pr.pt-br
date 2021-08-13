---
title: Geração de alias de memória e herança de dados
description: O recurso colocado e reservado pode ser um alias de memória física dentro de um heap. Os recursos colocados permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b584ef95f4ee89bc98940c8407427203a19f55046134e1d3c15cb672fef8fef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460916"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Geração de alias de memória e herança de dados

O recurso colocado e reservado pode ser um alias de memória física dentro de um heap. Os recursos colocados permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos.

-   [Atribuição de alias](#memory-aliasing-and-data-inheritance)
-   [Herança de dados](#data-inheritance)
-   [Tópicos relacionados](#related-topics)

## <a name="aliasing"></a>Atribuição de alias

Uma barreira de alias deve ser emitida entre o uso de dois recursos que compartilham a mesma memória física, mesmo que a herança de dados não seja desejada. Modelos de uso simples devem indicar, pelo menos, o recurso de destino envolvido em tal operação. Consulte [**CreatePlacedResource para**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) obter mais detalhes e modelos de uso avançados.

Depois que um recurso é acessado, todos os recursos que compartilham memória física com esse recurso são invalidados, a menos que a herança de dados tenha permissão para ocorrer. Leituras de recursos invalidados resultam em conteúdo de recurso indefinido. Gravações em recursos invalidados também resultam em conteúdo de recurso indefinido, a menos que duas condições ocorram:

-   O recurso não tem o SINALIZADOR DE RECURSO D3D12 ALLOW RENDER TARGET ou O SINALIZADOR DE RECURSO \_ \_ \_ \_ \_ D3D12 \_ \_ ALLOW DEPTH \_ \_ \_ STENCIL.
-   A gravação é uma operação de cópia ou de limpar para uma sub-fonte ou um grupo inteiro. A inicialização deile só está disponível para recursos com SWIZZLE INDEFINIDO DE 64KB E SWIZZLE PADRÃO DE \_ \_ \_ 64KB. \_ \_ \_

As invalidações sobrepostas têm como escopo granularidades menores, quando os layouts fornecem informações sobre a localização do local dos dados de texel e quando os recursos estão em determinados estados de barreira de transição. No entanto, as invalidações não podem ser menores do que as granularidades de alinhamento de recursos.

Uma granularidade de alinhamento de buffer é de 64KB e a granularidade de alinhamento maior tem precedência. Isso é importante ao considerar texturas de 4KB, pois várias texturas de 4KB podem residir em uma região de 64KB sem sobreposição umas às outras. Porém, um buffer com alias da mesma região de 64KB não pode ser usado em conjunto com qualquer uma dessas texturas de 4KB. O aplicativo não pode impedir de forma confiável o acesso ao buffer de intersecção das texturas de 4KB, pois as GPUs têm permissão para fazer swizzle de dados de textura de 4KB dentro da região de 64KB em um padrão indefinido.

Os layouts de textura \_ \_ SWIZZLE INDEFINIDO DE \_ 64KB, SWIZZLE PADRÃO DE 64KB e TEXTURA PRINCIPAL DE LINHA informam ao aplicativo quais granularidades de alinhamento sobrepostas se tornaram \_ \_ \_ \_ inválidas. Por exemplo: um aplicativo pode criar uma matriz de textura de destino de renderização 2D com duas fatias de matriz, um único nível de mip e o \_ layout SWIZZLE INDEFINIDO de 64KB \_ \_ TILE. Suponha que o aplicativo entenda que cada fatia de matriz ocupa blocos de 100 64KB. O aplicativo pode forgo usando a fatia de matriz 0 e re-usar essa memória para um buffer de ~6 MB, uma textura de ~6 MB com layout indefinido etc. Além disso, suponha que o aplicativo não exigia mais o primeiro pacote da fatia 1 da matriz. Em seguida, o aplicativo também pode localizar um buffer de 64KB lá até que a renderização exigir novamente o primeiro pacote da fatia 1 da matriz. O aplicativo teria que limpar ou copiar um peça completo para usar novamente o primeiro peça com a matriz de textura.

No entanto, até mesmo texturas com layouts definidos ainda têm casos problemáticos. Os tamanhos de recursos de textura podem diferir significativamente do que o aplicativo pode calcular a si mesmo, porque algumas arquiteturas de adaptador alocam memória extra para texturas a fim de reduzir a largura de banda efetiva durante cenários comuns de renderização. Quaisquer invalidações nessa região de memória extra causam a invalidação de todo o recurso. Consulte [**GetResourceAllocationInfo para**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) obter mais detalhes.

## <a name="data-inheritance"></a>Herança de dados

Os recursos colocados permitem a maior herança de dados para texturas, mesmo com layouts de memória indefinido. Os aplicativos podem imitar os recursos de herança de dados que os recursos confirmados compartilhados permitem localizando duas texturas com propriedades de recurso idênticas no mesmo deslocamento em um heap compartilhado. Toda a descrição do recurso deve ser idêntica, incluindo o valor claro otimizado e o tipo de método de criação de recurso (colocado ou reservado). No entanto, ambos os recursos podem ter estados de barreira de transição iniciais diferentes.

Os recursos reservados habilitam a herança de dados por parte do ; mas normalmente existem restrições para estados de barreira de transição de recursos.

Para herdar dados, ambos os recursos devem estar em um estado de barreira de transição de recurso compatível:

-   Para buffers, texturas de acesso simultâneo e texturas entre adaptadores, o estado de transição de recurso não é importante e todos os estados são "compatíveis".
-   Para texturas reservadas sem as propriedades anteriores ou outra herança de dados por lado por meio de SWIZZLE INDEFINIDO DE 64KB ou SWIZZLE PADRÃO DE \_ \_ \_ 64KB, o estado de barreira de transição de recurso, incluindo o lado, deve estar no \_ \_ estado \_ comum.
-   Para todas as outras texturas, em que as descrições do recurso correspondem exatamente, o estado da barreira de transição de recursos para cada par correspondente de sub-fontes deve:
    -   Estar no estado comum.
    -   Ser igual quando o estado tiver o mesmo sinalizador de gravação de GPU.

Quando a GPU dá suporte ao swizzle padrão, buffers e texturas swizzle padrão podem ter um alias para a mesma memória e herdar dados entre eles. O aplicativo pode manipular os texels da representação de buffer, porque o padrão swizzle padrão descreve como os texels são colocados na memória. O padrão swizzle visível na CPU é equivalente ao padrão de swizzle visível para GPU visto em buffers.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subalocação em heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




