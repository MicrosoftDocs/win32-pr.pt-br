---
title: As otimizações de uma CPU, texturas acessíveis e swizzle padrão
description: As GPUs da arquitetura de memória universal (a) oferecem algumas vantagens de eficiência em relação a GPUs discretas, especialmente ao otimizar para dispositivos móveis.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2624a300811b4d4a1eef70873a31af89b0546224fd9b4f3ba06ecb1fbd2fac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894666"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Otimizações de UMA: texturas acessíveis por CPU e swizzling padrão

As GPUs da arquitetura de memória universal (a) oferecem algumas vantagens de eficiência em relação a GPUs discretas, especialmente ao otimizar para dispositivos móveis. Conceder acesso à CPU de recursos quando a GPU é uma pode reduzir a quantidade de cópia que ocorre entre a CPU e a GPU. Embora não recomendemos que os aplicativos ofereçam acesso cego à CPU a todos os recursos em designs de uma, há oportunidades de melhorar a eficiência fornecendo o acesso à CPU dos recursos corretos. Ao contrário de GPUs discretas, a CPU pode tecnicamente ter um ponteiro para todos os recursos que a GPU pode acessar.

-   [Visão geral das texturas acessíveis à CPU](#overview-of-cpu-accessible-textures)
-   [Visão geral do swizzle padrão](#overview-of-standard-swizzle)
-   [APIs](#apis)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Visão geral das texturas acessíveis à CPU

As texturas acessíveis à CPU, no pipeline de gráficos, são um recurso de arquitetura de uma, permitindo acesso de leitura e gravação de CPUs a texturas. Nas GPUs discretas mais comuns, a CPU não tem acesso a texturas no pipeline de gráficos.

O Conselho geral de práticas recomendadas para texturas é acomodar GPUs discretas, que geralmente envolvem os processos no [carregamento de dados de textura por meio de buffers](upload-and-readback-of-texture-data.md), resumidos como:

-   Não ter nenhum acesso de CPU para a maioria das texturas.
-   Definindo o layout de textura para o \_ layout de textura D3D12 \_ \_ desconhecido.
-   Carregando as texturas na GPU com [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

No entanto, para determinados casos, a CPU e a GPU podem interagir com tanta frequência nos mesmos dados, que o mapeamento de texturas se torna útil para economizar energia ou para acelerar um design específico em determinados adaptadores ou arquiteturas. Os aplicativos devem detectar esses casos e otimizar as cópias desnecessárias. Nesse caso, para obter o melhor desempenho, considere o seguinte:

-   Só comece a se divertido o melhor desempenho do mapeamento de texturas quando a arquitetura de dados de recursos do D3D12:: a é verdadeira. [**\_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) Em seguida, preste atenção ao *CacheCoherentUMA* se decidir quais propriedades de cache de CPU escolher no heap.

-   Aproveitar o acesso de CPU para texturas é mais complicado do que para buffers. Os layouts de textura mais eficientes para GPUs são raramente a linha \_ principal. Na verdade, algumas GPUs só podem dar suporte a \_ texturas principais de linha ao copiar dados de textura.

-   As GPUs de uma devem se beneficiar universalmente de uma otimização simples para reduzir os tempos de carregamento de nível. Depois de reconhecer uma, o aplicativo pode otimizar o [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) inicial para popular as texturas que a GPU não modificará. Em vez de criar a textura em um heap com o \_ tipo de heap D3D12 \_ \_ padrão e empacotar os dados de textura por meio do, o aplicativo pode usar o [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) para evitar entender o layout de textura real.

-   No D3D12, as texturas criadas com o \_ layout de textura D3D12 \_ \_ são desconhecidas e nenhum acesso de CPU é o mais eficiente para a renderização e a amostragem de GPU frequentes. Quando o teste de desempenho, essas texturas devem ser comparadas \_ com o layout de textura D3D12 \_ \_ desconhecido com acesso à CPU, e o \_ layout de textura D3D12 \_ \_ padrão \_ SWIZZLE com acesso à CPU e a \_ \_ \_ linha de layout de textura D3D12 \_ principal para suporte entre adaptadores.

-   O uso \_ \_ do layout \_ de textura D3D12 desconhecido com acesso à CPU permite que os métodos [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**mapeie**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (impedindo o acesso do aplicativo ao ponteiro) e o [**cancelem**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap), mas possam sacrificar a eficiência do acesso à GPU.

-   Usando \_ \_ o layout de textura D3D12 \_ Standard \_ SWIZZLE com acesso à CPU habilita [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (que retorna um ponteiro válido para o aplicativo) e o [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap). Ele também pode sacrificar a eficiência de acesso GPU mais do que o \_ layout de textura D3D12 \_ \_ desconhecido com acesso à CPU.

## <a name="overview-of-standard-swizzle"></a>Visão geral do swizzle padrão

D3D12 (e D3D 11.3) introduz um layout de dados multidimensional padrão. Isso é feito para permitir que várias unidades de processamento operem nos mesmos dados sem copiar os dados ou swizzling os dados entre vários layouts. Um layout padronizado permite ganhos de eficiência por meio de efeitos de rede e permite que os algoritmos façam pequenos cortes, supondo um padrão específico.

Para obter uma descrição detalhada dos layouts de textura, consulte [**\_ \_ layout de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

No entanto, observe que esse swizzle padrão é um recurso de hardware e pode não ter suporte de todas as GPUs.

Para obter informações básicas sobre swizzling, consulte a [curva de ordem Z](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>APIs

Ao contrário do D3D 11.3, o D3D12 dá suporte ao mapeamento de textura por padrão, portanto, não há necessidade de consultar [**\_ \_ \_ \_ as opções de D3D12 de dados de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). No entanto, D3D12 nem sempre dá suporte a swizzle padrão. esse recurso precisará ser consultado com uma chamada para [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) e marcando o campo *StandardSwizzle64KBSupported* de **D3D12 \_ recurso \_ D3D12 de dados de \_ \_ Opções**.

As seguintes APIs referenciam o mapeamento de textura:

Enumerações

-   [**D3D12 \_ \_Layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) : controla o padrão swizzle de texturas padrão e habilita o suporte de mapa em texturas acessíveis à CPU.

Estruturas

-   [**D3D12 \_ RECURSO \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) : descreve um recurso, como uma textura, que é uma estrutura amplamente usada.
-   [**D3D12 \_ HEAP \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) : descreve um heap.

Métodos

-   [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) : cria um único recurso e heap de backup do tamanho e alinhamento corretos.
-   [**ID3D12Device:: createheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : cria um heap para um buffer ou uma textura.
-   [**ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : cria um recurso que é colocado em um heap específico, geralmente um método mais rápido de criar um recurso do que o [**createheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) : cria um recurso que é reservado, mas ainda não foi confirmado ou colocado em um heap.
-   [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : atualiza os mapeamentos de locais de bloco em recursos de blocos gráficos para locais de memória em um heap de recursos.
-   [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : Obtém um ponteiro para os dados especificados no recurso e nega o acesso GPU ao subrecurso.
-   [**ID3D12Resource:: GetDesc**](id3d12resource-getdesc.md) : Obtém as propriedades do recurso.
-   [**ID3D12Heap:: GetDesc**](id3d12heap-getdesc.md) Obtém as propriedades de heap.
-   [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : Copia dados de uma textura que foi mapeada usando [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : Copia dados em uma textura que foi mapeada usando [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Os recursos e os heaps pai têm requisitos de alinhamento:

-   D3D12 \_ o \_ \_ \_ \_ alinhamento de posicionamento de recursos de MSAA padrão (4MB) para texturas com várias amostras.
-   D3D12 \_ o \_ \_ \_ alinhamento de posicionamento de recursos padrão (64 KB) para texturas e buffers de amostra única.
-   A cópia linear de subrecurso deve estar alinhada ao \_ alinhamento de posicionamento de dados de textura D3D12 \_ \_ \_ (512 bytes), com densidade de linha alinhada ao \_ alinhamento de densidade de dados de textura D3D12 \_ \_ \_ (256 bytes).
-   As exibições de buffer de constantes devem estar alinhadas ao \_ \_ alinhamento de posicionamento de dados do buffer de constante D3D12 \_ \_ \_ (256 bytes).

As texturas menores que 64 KB devem ser processadas por meio de [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Com texturas dinâmicas (texturas que alteram cada quadro), a CPU gravará linearmente no heap de carregamento, seguida por uma operação de cópia de GPU.

Normalmente, para criar recursos dinâmicos, crie um buffer grande em um heap de carregamento (consulte [subalocação em buffers](large-buffers.md)). Para criar recursos de preparo, crie um buffer grande em um heap readback. Para criar recursos estáticos padrão, crie recursos adjacentes em um heap padrão. Para criar recursos com alias padrão, crie recursos sobrepostos em um heap padrão.

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) reorganizam dados de textura entre um layout de linha-principal e um layout de recurso indefinido. A operação é síncrona, portanto, o aplicativo deve manter o agendamento da CPU em mente. O aplicativo sempre pode dividir a cópia em regiões menores ou agendar essa operação em outra tarefa. Recursos de MSAA e recursos de estêncil de profundidade com layouts de recursos opacos não são suportados por essas operações de cópia de CPU e causarão uma falha. Os formatos que não têm um tamanho de elemento de energia de dois também não têm suporte e também causarão uma falha. Podem ocorrer códigos de retorno de memória insuficiente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Principais constantes**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 




