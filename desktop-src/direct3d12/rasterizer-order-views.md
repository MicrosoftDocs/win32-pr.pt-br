---
title: Exibições ordenadas pelo Rasterizer
description: As ROVs (exibições ordenadas pelo rasterizador) permitem que o código do sombreador de pixel marque as vinculações de exibição de acesso não ordenadas com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214098f70608d5f20d24edb1312593c6215abea12efecfc6eea97148e8855cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300977"
---
# <a name="rasterizer-ordered-views"></a>Exibições ordenadas pelo Rasterizer

Os ROVs (exibições ordenadas pelo Rasterizer) permitem que o código do sombreador de pixel marque as vinculações UAV (exibição de acesso não ordenada) com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs. Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que dá resultados de renderização muito melhores quando vários objetos transparentes estão alinhados entre si em uma exibição.

-   [Visão geral](#overview)
-   [Detalhes de implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Os pipelines de elementos gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência. Objetos como cercas de transmissão, incêndio, incêndio, transparência e vidro colorido usam transparência para obter o efeito desejado. Surgem problemas quando várias texturas que contêm transparência estão alinhadas umas com as outras (smoke na frente de uma cerca na frente de um prédio de vidro que contém a fachada, como um exemplo). Os ROVs (exibições ordenadas pelo Rasterizer) permitem que os algoritmos OIT subjacentes usem recursos do hardware para tentar resolver a ordem de transparência corretamente. A transparência é tratada pelo sombreador de pixel.

Os ROVs (exibições ordenadas pelo rasterizador) permitem que o código do sombreador de pixel marque as vinculações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs.

Os ROVs garantem a ordem de acessos UAV para qualquer par de invocações de sombreador de pixel sobreposto. Nesse caso, "sobreposição" significa que as invocações são geradas pelas mesmas chamadas de desenho e compartilham a mesma coordenada de pixel quando no modo de execução de frequência de pixel e a mesma coordenada de pixel e amostra no modo de frequência de exemplo.

A ordem na qual os acessos ROV sobrepostos de invocações de sombreador de pixel são executados é idêntica à ordem na qual a geometria é enviada. Isso significa que, para invocações de sombreador de pixel sobrepostos, as gravações ROV executadas por uma invocação de sombreador de pixel devem estar disponíveis para serem lidas por uma invocação subsequente e não devem afetar as leituras por uma invocação anterior. As leituras de ROV executadas por uma invocação de sombreador de pixel devem refletir gravações por uma invocação anterior e não devem refletir gravações por uma invocação subsequente. Isso é importante para os UAVs porque eles são explicitamente omitidos das garantias de invariância de saída normalmente definidas pela ordem fixa dos resultados do pipeline de gráficos.

## <a name="implementation-details"></a>Detalhes de implementação

Os ROVs (exibições ordenadas pelo rasterizador) são declarados com os seguintes novos objetos HLSL (High Level Shader Language) e só estão disponíveis para o sombreador de pixel:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Use esses objetos da mesma maneira que outros objetos UAV (como `RWBuffer` etc.).

## <a name="api-summary"></a>Resumo da API

ROVs são um constructo somente HLSL que aplica semântica de comportamento diferente a UAVs. Todas as APIs relevantes para os UAVs também são relevantes para ROVs. Observe que o método, as estruturas e a classe auxiliar a seguir referenciam o rasterizador:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) estrutura que mantém a descrição do rasterizador.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) estrutura que mantém um booliana, indicando o suporte.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) método para acessar os recursos com suporte.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) classe auxiliar para criar descrições do rasterizador.
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) estrutura que mantém o estado do pipeline.

## <a name="related-topics"></a>Tópicos relacionados

* [Rasterização conservativa](conservative-rasterization.md)
* [Renderização](rendering.md)
* [Associação de recursos no HLSL](resource-binding-in-hlsl.md)
* [Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)