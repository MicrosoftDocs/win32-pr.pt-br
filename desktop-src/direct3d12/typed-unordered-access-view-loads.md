---
title: Carregamentos de UAV (exibição de acesso não ordenado) digitados
description: A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um formato DXGI específico \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548242"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Carregamentos de UAV (exibição de acesso não ordenado) digitados

A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico.

-   [Visão geral](#overview)
-   [Formatos e chamadas de API com suporte](#supported-formats-and-api-calls)
-   [Usando cargas UAV tipadas de HLSL](#using-typed-uav-loads-from-hlsl)
-   [Usando UNORM e SNORM tipado UAV cargas de HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Um UAV (modo de exibição de acesso não ordenado) é uma exibição de um recurso de acesso não ordenado (que pode incluir buffers, texturas e matrizes de textura, embora sem várias amostras). Um UAV permite acesso de leitura/gravação não ordenado de forma temporal de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória. Esse acesso simultâneo é tratado por meio do uso de [funções atômicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (e D3D 11.3) expande na lista de formatos que podem ser usados com cargas UAV tipadas.

## <a name="supported-formats-and-api-calls"></a>Formatos e chamadas de API com suporte

Anteriormente, os três formatos a seguir suportavam cargas de UAV tipadas e eram necessárias para o hardware do D3D 11.0. Eles têm suporte para todos os hardwares do D3D 11.3 e D3D12.

-   R32 \_ float
-   R32 \_ uint
-   R32 \_ Santo

Os formatos a seguir têm suporte como um conjunto no hardware D3D12 ou D3D 11.3, portanto, se houver suporte para qualquer um, todos têm suporte.

-   R32G32B32A32 \_ float
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Santo
-   R16G16B16A16 \_ float
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Santo
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Santo
-   R16 \_ float
-   R16 \_ uint
-   R16 \_ Santo
-   UNORM de R8 \_
-   R8 \_ uint
-   R8, \_ Santo

Os seguintes formatos são opcionalmente e individualmente suportados em hardware D3D12 e D3D 11.3, portanto, uma única consulta precisaria ser feita em cada formato para testar o suporte.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ float
-   R32G32 \_ uint
-   R32G32 \_ Santo
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ uint
-   R11G11B10 \_ float
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ float
-   R16G16 \_ UNORM
-   R16G16 \_ uint
-   R16G16 \_ SNORM
-   R16G16 \_ Santo
-   R8G8 \_ UNORM
-   R8G8 \_ uint
-   R8G8 \_ SNORM
-   R8G8 \_ Santo
-   R16 \_ UNORM
-   R16 \_ SNORM
-   SNORM de R8 \_
-   \_UNORM a8
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar o suporte para todos os formatos adicionais, chame [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) com a estrutura de opções de [**D3D12 de \_ dados de recurso \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como o primeiro parâmetro (consulte a [consulta de funcionalidade](capability-querying.md)). O campo *TypedUAVLoadAdditionalFormats* será definido se a lista "com suporte como um conjunto" acima for suportada. Faça uma segunda chamada para **CheckFeatureSupport**, usando uma estrutura de [**suporte de formato de \_ dados de recurso \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (verificando a estrutura retornada no \_ formato D3D12 \_ SUPPORT2 \_ UAV \_ \_ de carregamento digitado do [**\_ formato D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) SUPPORT2 enum) para determinar o suporte na lista de formatos com suporte opcional listados acima, por exemplo:

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Usando cargas UAV tipadas de HLSL

Para UAVs tipados, o sinalizador HLSL é o \_ sombreador do D3D \_ requer \_ \_ \_ formatos adicionais de carga UAV \_ \_ .

Aqui está um código de sombreador de exemplo para processar uma carga de UAV tipada:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Usando UNORM e SNORM tipado UAV cargas de HLSL

Ao usar carregamentos UAV tipados para ler de um recurso UNORM ou SNORM, você deve declarar corretamente o tipo de elemento do objeto HLSL como `unorm` ou `snorm` . Ele é especificado como um comportamento indefinido para incompatibilidade do tipo de elemento declarado em HLSL com o tipo de dados de recurso subjacente. Por exemplo, se você estiver usando cargas UAV tipadas em um recurso de buffer com dados de R8 \_ UNORM, deverá declarar o tipo de elemento como `unorm float` :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização](rendering.md)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> <dt>

[Associação de recursos em HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Especificando assinaturas raiz em HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 