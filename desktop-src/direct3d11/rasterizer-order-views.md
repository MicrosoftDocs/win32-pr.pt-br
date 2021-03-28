---
title: Exibições de ordem do rasterizador
description: As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084764"
---
# <a name="rasterizer-order-views"></a>Exibições de ordem do rasterizador

As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs. Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição.

-   [Visão geral](#overview)
-   [Detalhes da implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Pipelines gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência. Objetos como isolamentos de fio, fumaça, fogo, vegetação e transparência de uso de vidro colorido para obter o efeito desejado. Os problemas surgem quando várias texturas que contêm transparência estão alinhadas umas com as outras (fumaça na frente de uma cerca na frente de um prédio contendo vegetação, como um exemplo). As exibições ordenadas do rasterizador (ROVs) permitem que os algoritmos subjacentes do OIT usem recursos do hardware para tentar resolver a ordem de transparência corretamente. A transparência é manipulada pelo sombreador de pixel.

As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.

ROVs garante a ordem dos acessos UAV para qualquer par de invocações de sombreador de pixel sobrepostas. Nesse caso, "sobreposto" significa que as invocações são geradas pelas mesmas chamadas de desenho e compartilham a mesma coordenada de pixel quando no modo de execução de frequência de pixels e o mesmo pixel e coordenada de exemplo no modo de frequência de amostra.

A ordem em que a sobreposição de acessos ROV de invocações de sombreador de pixel são executadas é idêntica à ordem em que a geometria é enviada. Isso significa que, para a sobreposição de invocações de sombreador de pixel, as gravações ROV executadas por uma invocação de sombreador de pixel devem estar disponíveis para serem lidas por uma invocação subsequente e não devem afetar as leituras por uma invocação anterior. As leituras de ROV executadas por uma invocação de sombreador de pixel devem refletir as gravações por uma invocação anterior e não devem refletir as gravações por uma invocação subsequente. Isso é importante para UAVs porque eles são explicitamente omitidos das garantias de invariação de saída normalmente definidas pela ordem fixa de resultados de pipeline de gráficos.

## <a name="implementation-details"></a>Detalhes de implementação

As exibições ordenadas do rasterizador (ROVs) são declaradas com os novos objetos de HLSL (linguagem de sombreamento de alto nível) e estão disponíveis somente para o sombreador de pixel:

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

-   [**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estrutura que mantém a descrição do rasterizador, observando a \_ classe auxiliar do CD3D12 rasterizador \_ DESC2 para criar descrições do rasterizador.
-   [**D3D11 \_ Dados de recurso \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estrutura que contém o booliano `ROVsSupported` , indicando o suporte.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para acessar os recursos com suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 