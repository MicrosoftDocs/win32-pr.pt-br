---
title: Exibições ordenadas pelo rasterizador
description: Os ROVs (exibições ordenadas pelo rasterizador) permitem que o código do sombreador de pixel marque associações de exibição de acesso não ordenadas com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19988d3f3eec39e8fc298a2fc13031ecc29e3e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548292"
---
# <a name="rasterizer-ordered-views"></a>Exibições ordenadas pelo rasterizador

Os ROVs (exibições ordenadas pelo rasterizador) permitem que o código do sombreador de pixel marque associações de UAV (exibição de acesso não ordenado) com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs. Isso permite que os algoritmos de transparência independente de ordem (OIT) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição.

-   [Visão geral](#overview)
-   [Detalhes da implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Pipelines gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência. Objetos como isolamentos de fio, fumaça, fogo, vegetação e transparência de uso de vidro colorido para obter o efeito desejado. Os problemas surgem quando várias texturas que contêm transparência estão alinhadas umas com as outras (fumaça na frente de uma cerca na frente de um prédio contendo vegetação, como um exemplo). Os ROVs (exibições ordenadas pelo rasterizador) permitem que os algoritmos subjacentes do OIT usem recursos do hardware para tentar resolver a ordem de transparência corretamente. A transparência é manipulada pelo sombreador de pixel.

As exibições ordenadas pelo rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.

ROVs garante a ordem dos acessos UAV para qualquer par de invocações de sombreador de pixel sobrepostas. Nesse caso, "sobreposto" significa que as invocações são geradas pelas mesmas chamadas de desenho e compartilham a mesma coordenada de pixel quando no modo de execução de frequência de pixels e o mesmo pixel e coordenada de exemplo no modo de frequência de amostra.

A ordem em que a sobreposição de acessos ROV de invocações de sombreador de pixel são executadas é idêntica à ordem em que a geometria é enviada. Isso significa que, para a sobreposição de invocações de sombreador de pixel, as gravações ROV executadas por uma invocação de sombreador de pixel devem estar disponíveis para serem lidas por uma invocação subsequente e não devem afetar as leituras por uma invocação anterior. As leituras de ROV executadas por uma invocação de sombreador de pixel devem refletir as gravações por uma invocação anterior e não devem refletir as gravações por uma invocação subsequente. Isso é importante para UAVs porque eles são explicitamente omitidos das garantias de invariação de saída normalmente definidas pela ordem fixa de resultados de pipeline de gráficos.

## <a name="implementation-details"></a>Detalhes de implementação

Os ROVs (exibições ordenadas pelo rasterizador) são declarados com os novos objetos de HLSL (linguagem de sombreamento de alto nível) e estão disponíveis somente para o sombreador de pixel:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Use esses objetos da mesma maneira que outros objetos UAV (como, `RWBuffer` etc.).

## <a name="api-summary"></a>Resumo da API

ROVs são uma construção somente HLSL que aplica semântica de comportamento diferente ao UAVs. Todas as APIs relevantes para UAVs também são relevantes para ROVs. Observe que o seguinte método, estruturas e classe auxiliar fazem referência ao rasterizador:

-   [**D3D12 \_ Rerasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : estrutura que contém a descrição do rasterizador.
-   [**D3D12 \_ \_Opções de \_ D3D12 \_ de dados de recurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estrutura que contém um booliano, indicando o suporte.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : método para acessar os recursos com suporte.
-   [**CD3DX12 \_ Classe do RASTERIZAdor \_ desc**](cd3dx12-rasterizer-desc.md) : Helper para criar descrições do rasterizador.
-   [**D3D12 \_ Estado do pipeline de gráficos \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : estrutura que contém o estado do pipeline.

## <a name="related-topics"></a>Tópicos relacionados

* [Rasterização conservadora](conservative-rasterization.md)
* [Renderização](rendering.md)
* [Associação de recursos em HLSL](resource-binding-in-hlsl.md)
* [Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)