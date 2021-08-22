---
title: Carregamentos de exibição de acesso não organizado digitado
description: Saiba mais sobre a carga com tipo UAV (Exibição de Acesso Não Organizado) no Direct3D 11. A carga com tipo UAV é a capacidade de um sombreador ler de um UAV com uma DXGI_FORMAT.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7389ba850c68129509ca6b6a835f949dd92f5541382d9fdc2243611d409ca2a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124054"
---
# <a name="typed-unordered-access-view-loads"></a>Carregamentos de exibição de acesso não organizado digitado

A carga com tipo UAV (Exibição de Acesso Não Organizado) é a capacidade de um sombreador ler de um UAV com um FORMATO DXGI \_ específico.

-   [Visão geral](#overview)
-   [Formatos e chamadas à API com suporte](#supported-formats-and-api-calls)
-   [Usando cargas UAV com tipo de HLSL](#using-typed-uav-loads-from-hlsl)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Uma UAV (exibição de acesso não organizado) é uma exibição de um recurso de acesso não organizado (que pode incluir buffers, texturas e matrizes de textura, embora sem várias amostragem). Um UAV permite acesso de leitura/gravação temporalmente não organizado de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória. Esse acesso simultâneo é tratado por meio do uso de [Funções Atômicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 e D3D11.3 se expandem na lista de formatos que podem ser usados com cargas UAV digitados.

## <a name="supported-formats-and-api-calls"></a>Formatos e chamadas à API com suporte

Anteriormente, os três formatos a seguir tinham suporte para cargas UAV com tipo e eram necessários para hardware D3D11.0. Há suporte para todos os hardwares D3D11.3 e D3D12.

-   R32 \_ FLOAT
-   R32 \_ UINT
-   R32 \_ SINT

Os formatos a seguir têm suporte como um conjunto no hardware D3D12 ou D3D11.3, portanto, se qualquer um tiver suporte, todos serão suportados.

-   R32G32B32A32 \_ FLOAT
-   R32G32B32A32 \_ UINT
-   R32G32B32A32 \_ SINT
-   R16G16B16A16 \_ FLOAT
-   R16G16B16A16 \_ UINT
-   R16G16B16A16 \_ SINT
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ UINT
-   R8G8B8A8 \_ SINT
-   R16 \_ FLOAT
-   R16 \_ UINT
-   R16 \_ SINT
-   R8 \_ UNORM
-   R8 \_ UINT
-   R8 \_ SINT

Os formatos a seguir têm suporte opcional e individual no hardware D3D12 e D3D11.3, portanto, uma única consulta precisaria ser feita em cada formato para testar o suporte.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ FLOAT
-   R32G32 \_ UINT
-   R32G32 \_ SINT
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ UINT
-   R11G11B10 \_ FLOAT
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ FLOAT
-   R16G16 \_ UNORM
-   R16G16 \_ UINT
-   R16G16 \_ SNORM
-   R16G16 \_ SINT
-   R8G8 \_ UNORM
-   R8G8 \_ UINT
-   R8G8 \_ SNORM
-   8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Para determinar o suporte para quaisquer formatos adicionais, chame [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com a estrutura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como o primeiro parâmetro. O `TypedUAVLoadAdditionalFormats` bit será definido se a lista "com suporte como um conjunto" acima tiver suporte. Faça uma segunda chamada para **CheckFeatureSupport** usando uma estrutura [**D3D11 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (verificando a estrutura retornada em relação ao membro D3D12 \_ FORMAT \_ SUPPORT2 \_ UAV TYPED LOAD da \_ \_ enum [**D3D11 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) para determinar o suporte na lista de formatos com suporte opcional acima, por exemplo:

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

## <a name="using-typed-uav-loads-from-hlsl"></a>Usando cargas UAV com tipo de HLSL

Para UAVs digitados, o sinalizador HLSL é SOMBREADOR D3D REQUER FORMATOS ADICIONAIS DE CARGA \_ \_ \_ \_ UAV \_ \_ \_ DIGITADO.

Aqui está um código de sombreador de exemplo para processar uma carga UAV digitada:

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

[Recursos do Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 