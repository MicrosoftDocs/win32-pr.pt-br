---
title: Consulta de funcionalidade
description: 'Seu aplicativo pode descobrir o nível de suporte para associação de recursos e muitos outros recursos, com uma chamada para ID3D12Device \: \: CheckFeatureSupport.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: a99174515883f8995167a7b866ab1ef8b77b56f7a0be2bb83f960abd06e47713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851396"
---
# <a name="capability-querying"></a>Consulta de funcionalidade

Seu aplicativo pode descobrir o nível de suporte para associação de recursos (bem como o nível de suporte para muitos outros recursos), com uma chamada para [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

## <a name="how-to-query-for-the-resource-binding-tier"></a>Como consultar a camada de associação de recursos

Este primeiro exemplo se concentra na associação de recursos. Cada camada de associação de recursos é um superconjunto de camadas inferiores na funcionalidade, portanto, o código que funciona em uma determinada camada funciona inalterado em qualquer camada superior.

As camadas de associação de recursos são constantes na [**enumeração D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) dados.

Para consultar a camada de associação de recursos, use um código como este. Este exemplo de código demonstra o padrão geral para consultar qualquer um dos vários tipos de suporte a recursos.

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

Observe que qualquer constante enumerada que você passar ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), nesse caso) tem uma estrutura de dados correspondente que recebe informações sobre esse recurso ou conjunto de recursos ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), nesse caso). Sempre passe um ponteiro para a estrutura que corresponde à constante enumerada que você passa.

## <a name="how-to-query-for-any-feature-level"></a>Como consultar qualquer nível de recurso

Além da camada de associação de recursos, há muitos outros recursos cujo nível de suporte você pode consultar para usar o mesmo padrão mostrado no exemplo de código acima. Basta passar uma constante diferente da enumeração [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) para [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (para dizer à API em qual recurso solicitar informações de suporte) e passar um ponteiro para uma instância da estrutura correspondente (na qual receber as informações solicitadas).

- Passe **D3D12_FEATURE_ARCHITECTURE** e [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Passe **D3D12_FEATURE_ARCHITECTURE1** e [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Passe **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** e [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Passe **D3D12_FEATURE_CROSS_NODE** e [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Passe **D3D12_FEATURE_D3D12_OPTIONS** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Passe **D3D12_FEATURE_D3D12_OPTIONS1** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Passe **D3D12_FEATURE_D3D12_OPTIONS2** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Passe **D3D12_FEATURE_D3D12_OPTIONS3** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Passe **D3D12_FEATURE_D3D12_OPTIONS4** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Passe **D3D12_FEATURE_D3D12_OPTIONS5** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Passe **D3D12_FEATURE_EXISTING_HEAPS** e [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Passe **D3D12_FEATURE_FEATURE_LEVELS** e [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Passe **D3D12_FEATURE_FORMAT_INFO** e [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Passe **D3D12_FEATURE_FORMAT_SUPPORT** e [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Passe **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** e [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Passe **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** e [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Passe **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** e [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Passe **D3D12_FEATURE_ROOT_SIGNATURE** e [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Passe **D3D12_FEATURE_SERIALIZATION** e [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Passe **D3D12_FEATURE_SHADER_CACHE** e [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Passe **D3D12_FEATURE_SHADER_MODEL** e [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Suporte de hardware para formatos DXGI

Para exibir tabelas de formatos DXGI e recursos de hardware, consulte estes tópicos.

- [Suporte ao formato DXGI para hardware de nível de recurso 12.1 do Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Suporte ao formato DXGI para hardware de nível de recurso 12.0 do Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Suporte ao formato DXGI para hardware de nível de recurso 11.1 do Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Suporte ao formato DXGI para hardware de nível de recurso 11.0 do Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
- [Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

* [Associação de recursos no Direct3D 12](resource-binding.md)
* [Níveis de recursos de hardware](hardware-feature-levels.md)
* [Assinaturas raiz](root-signatures.md)