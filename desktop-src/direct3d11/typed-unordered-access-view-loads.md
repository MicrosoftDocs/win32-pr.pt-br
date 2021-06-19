---
title: Cargas de exibição de acesso não ordenado digitado
description: Saiba mais sobre a carga digitada de UAV (exibição de acesso não ordenado) no Direct3D 11. A carga digitada UAV é a capacidade de um sombreador ler de um UAV com um DXGI_FORMAT específico.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396281"
---
# <a name="typed-unordered-access-view-loads"></a>Cargas de exibição de acesso não ordenado digitado

A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um formato DXGI específico \_ .

-   [Visão geral](#overview)
-   [Formatos e chamadas de API com suporte](#supported-formats-and-api-calls)
-   [Usando cargas UAV tipadas de HLSL](#using-typed-uav-loads-from-hlsl)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Um UAV (modo de exibição de acesso não ordenado) é uma exibição de um recurso de acesso não ordenado (que pode incluir buffers, texturas e matrizes de textura, embora sem várias amostras). Um UAV permite acesso de leitura/gravação não ordenado de forma temporal de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória. Esse acesso simultâneo é tratado por meio do uso de [funções atômicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 e D3D 11.3 expande a lista de formatos que podem ser usados com cargas UAV tipadas.

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
-   8G8 \_ Santo
-   R16 \_ UNORM
-   R16 \_ SNORM
-   SNORM de R8 \_
-   \_UNORM a8
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar o suporte para todos os formatos adicionais, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com a estrutura de [**dados do \_ recurso D3D11 \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como o primeiro parâmetro. O `TypedUAVLoadAdditionalFormats` bit será definido se a lista "com suporte como um conjunto" acima for suportada. Faça uma segunda chamada para **CheckFeatureSupport**, usando uma [**estrutura \_ \_ SUPPORT2 de \_ formato \_ de dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (verificando a estrutura retornada em relação ao D3D12 formato SUPPORT2 \_ \_ \_ \_ \_ membro de carregamento digitado do [**\_ formato UAV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) D3D11 enum) para determinar o suporte na lista de formatos opcionalmente suportados acima, por exemplo:

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 