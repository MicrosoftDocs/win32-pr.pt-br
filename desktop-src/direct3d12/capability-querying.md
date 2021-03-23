---
title: Consulta de funcionalidade
description: 'Seu aplicativo pode descobrir o nível de suporte para associação de recursos e muitos outros recursos, com uma chamada para ID3D12Device \: \: CheckFeatureSupport.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548230"
---
# <a name="capability-querying"></a><span data-ttu-id="26732-103">Consulta de funcionalidade</span><span class="sxs-lookup"><span data-stu-id="26732-103">Capability querying</span></span>

<span data-ttu-id="26732-104">Seu aplicativo pode descobrir o nível de suporte para a ligação de recursos (bem como o nível de suporte para muitos outros recursos), com uma chamada para [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="26732-104">Your application can discover the level of support for resource binding (as well as the level of support for many other features), with a call to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

## <a name="how-to-query-for-the-resource-binding-tier"></a><span data-ttu-id="26732-105">Como consultar a camada de associação de recursos</span><span class="sxs-lookup"><span data-stu-id="26732-105">How to query for the resource binding tier</span></span>

<span data-ttu-id="26732-106">Este primeiro exemplo se concentra na associação de recursos.</span><span class="sxs-lookup"><span data-stu-id="26732-106">This first example focuses on resource binding.</span></span> <span data-ttu-id="26732-107">Cada camada de associação de recurso é um superconjunto de camadas inferiores na funcionalidade, de modo que o código que funciona em uma determinada camada funciona inalterado em qualquer camada superior.</span><span class="sxs-lookup"><span data-stu-id="26732-107">Each resource binding tier is a superset of lower tiers in functionality, so code that works on a given tier works unchanged on any higher tier.</span></span>

<span data-ttu-id="26732-108">As camadas de associação de recurso são constantes na enumeração de [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .</span><span class="sxs-lookup"><span data-stu-id="26732-108">The resource binding tiers are constants in the [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) enumeration.</span></span>

<span data-ttu-id="26732-109">Para consultar a camada de associação de recursos, use um código como este.</span><span class="sxs-lookup"><span data-stu-id="26732-109">To query for the resource binding tier, use code such as this.</span></span> <span data-ttu-id="26732-110">Este exemplo de código demonstra o padrão geral para consultar qualquer um dos vários tipos de suporte a recursos.</span><span class="sxs-lookup"><span data-stu-id="26732-110">This code example demonstrates the general pattern for querying for any of the various kinds of feature support.</span></span>

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

<span data-ttu-id="26732-111">Observe que qualquer constante enumerada que você passa ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), nesse caso) tem uma estrutura de dados correspondente que recebe informações sobre esse recurso ou conjunto de recursos ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), nesse caso).</span><span class="sxs-lookup"><span data-stu-id="26732-111">Note that any enumerated constant that you pass ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in this case) has a corresponding data structure that receives info about that feature or set of features ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), in this case).</span></span> <span data-ttu-id="26732-112">Sempre passe um ponteiro para a estrutura que corresponde à constante enumerada que você passa.</span><span class="sxs-lookup"><span data-stu-id="26732-112">Always pass a pointer to the structure that matches the enumerated constant that you pass.</span></span>

## <a name="how-to-query-for-any-feature-level"></a><span data-ttu-id="26732-113">Como consultar qualquer nível de recurso</span><span class="sxs-lookup"><span data-stu-id="26732-113">How to query for any feature level</span></span>

<span data-ttu-id="26732-114">Além da camada de associação de recursos, há muitos outros recursos cujo nível de suporte você pode consultar usando o mesmo padrão mostrado no exemplo de código acima.</span><span class="sxs-lookup"><span data-stu-id="26732-114">As well as the resource binding tier, there are many other features whose level of support you can query for using the same pattern shown in the code example above.</span></span> <span data-ttu-id="26732-115">Basta passar uma constante diferente da enumeração [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) para [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (para informar à API a qual recurso solicitar informações de suporte) e passar um ponteiro para uma instância da estrutura correspondente (na qual as informações solicitadas são recebidas).</span><span class="sxs-lookup"><span data-stu-id="26732-115">You just pass a different constant from the [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) enumeration to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (to tell the API what feature to request support information on), and you pass a pointer to an instance of the matching structure (in which to receive the requested info).</span></span>

- <span data-ttu-id="26732-116">Passe **D3D12_FEATURE_ARCHITECTURE** e [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span><span class="sxs-lookup"><span data-stu-id="26732-116">Pass **D3D12_FEATURE_ARCHITECTURE** and [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span></span>
- <span data-ttu-id="26732-117">Passe **D3D12_FEATURE_ARCHITECTURE1** e [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span><span class="sxs-lookup"><span data-stu-id="26732-117">Pass **D3D12_FEATURE_ARCHITECTURE1** and [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span></span>
- <span data-ttu-id="26732-118">Passe **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** e [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span><span class="sxs-lookup"><span data-stu-id="26732-118">Pass **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** and [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span></span>
- <span data-ttu-id="26732-119">Passe **D3D12_FEATURE_CROSS_NODE** e [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span><span class="sxs-lookup"><span data-stu-id="26732-119">Pass **D3D12_FEATURE_CROSS_NODE** and [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span></span>
- <span data-ttu-id="26732-120">Passe **D3D12_FEATURE_D3D12_OPTIONS** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span><span class="sxs-lookup"><span data-stu-id="26732-120">Pass **D3D12_FEATURE_D3D12_OPTIONS** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span></span>
- <span data-ttu-id="26732-121">Passe **D3D12_FEATURE_D3D12_OPTIONS1** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span><span class="sxs-lookup"><span data-stu-id="26732-121">Pass **D3D12_FEATURE_D3D12_OPTIONS1** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span></span>
- <span data-ttu-id="26732-122">Passe **D3D12_FEATURE_D3D12_OPTIONS2** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span><span class="sxs-lookup"><span data-stu-id="26732-122">Pass **D3D12_FEATURE_D3D12_OPTIONS2** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span></span>
- <span data-ttu-id="26732-123">Passe **D3D12_FEATURE_D3D12_OPTIONS3** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span><span class="sxs-lookup"><span data-stu-id="26732-123">Pass **D3D12_FEATURE_D3D12_OPTIONS3** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span></span>
- <span data-ttu-id="26732-124">Passe **D3D12_FEATURE_D3D12_OPTIONS4** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span><span class="sxs-lookup"><span data-stu-id="26732-124">Pass **D3D12_FEATURE_D3D12_OPTIONS4** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span></span>
- <span data-ttu-id="26732-125">Passe **D3D12_FEATURE_D3D12_OPTIONS5** e [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span><span class="sxs-lookup"><span data-stu-id="26732-125">Pass **D3D12_FEATURE_D3D12_OPTIONS5** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span></span>
- <span data-ttu-id="26732-126">Passe **D3D12_FEATURE_EXISTING_HEAPS** e [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span><span class="sxs-lookup"><span data-stu-id="26732-126">Pass **D3D12_FEATURE_EXISTING_HEAPS** and [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span></span>
- <span data-ttu-id="26732-127">Passe **D3D12_FEATURE_FEATURE_LEVELS** e [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span><span class="sxs-lookup"><span data-stu-id="26732-127">Pass **D3D12_FEATURE_FEATURE_LEVELS** and [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span></span>
- <span data-ttu-id="26732-128">Passe **D3D12_FEATURE_FORMAT_INFO** e [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span><span class="sxs-lookup"><span data-stu-id="26732-128">Pass **D3D12_FEATURE_FORMAT_INFO** and [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span></span>
- <span data-ttu-id="26732-129">Passe **D3D12_FEATURE_FORMAT_SUPPORT** e [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span><span class="sxs-lookup"><span data-stu-id="26732-129">Pass **D3D12_FEATURE_FORMAT_SUPPORT** and [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span></span>
- <span data-ttu-id="26732-130">Passe **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** e [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span><span class="sxs-lookup"><span data-stu-id="26732-130">Pass **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** and [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span></span>
- <span data-ttu-id="26732-131">Passe **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** e [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span><span class="sxs-lookup"><span data-stu-id="26732-131">Pass **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** and [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span></span>
- <span data-ttu-id="26732-132">Passe **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** e [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span><span class="sxs-lookup"><span data-stu-id="26732-132">Pass **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** and [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span></span>
- <span data-ttu-id="26732-133">Passe **D3D12_FEATURE_ROOT_SIGNATURE** e [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span><span class="sxs-lookup"><span data-stu-id="26732-133">Pass **D3D12_FEATURE_ROOT_SIGNATURE** and [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span></span>
- <span data-ttu-id="26732-134">Passe **D3D12_FEATURE_SERIALIZATION** e [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span><span class="sxs-lookup"><span data-stu-id="26732-134">Pass **D3D12_FEATURE_SERIALIZATION** and [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span></span>
- <span data-ttu-id="26732-135">Passe **D3D12_FEATURE_SHADER_CACHE** e [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span><span class="sxs-lookup"><span data-stu-id="26732-135">Pass **D3D12_FEATURE_SHADER_CACHE** and [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span></span>
- <span data-ttu-id="26732-136">Passe **D3D12_FEATURE_SHADER_MODEL** e [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span><span class="sxs-lookup"><span data-stu-id="26732-136">Pass **D3D12_FEATURE_SHADER_MODEL** and [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span></span>

## <a name="hardware-support-for-dxgi-formats"></a><span data-ttu-id="26732-137">Suporte de hardware para formatos DXGI</span><span class="sxs-lookup"><span data-stu-id="26732-137">Hardware support for DXGI Formats</span></span>

<span data-ttu-id="26732-138">Para exibir tabelas de formatos de DXGI e recursos de hardware, consulte estes tópicos.</span><span class="sxs-lookup"><span data-stu-id="26732-138">To view tables of DXGI formats and hardware features, refer to these topics.</span></span>

- [<span data-ttu-id="26732-139">Suporte ao formato DXGI para hardware 12,1 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="26732-139">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [<span data-ttu-id="26732-140">Suporte ao formato DXGI para hardware 12,0 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="26732-140">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [<span data-ttu-id="26732-141">Suporte ao formato DXGI para hardware 11,1 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="26732-141">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [<span data-ttu-id="26732-142">Suporte ao formato DXGI para hardware 11,0 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="26732-142">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- <span data-ttu-id="26732-143">[Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26732-143">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
- <span data-ttu-id="26732-144">[Suporte de hardware para formatos Direct3D 10,1](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26732-144">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
- <span data-ttu-id="26732-145">[Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26732-145">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="26732-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26732-146">Related topics</span></span>

* [<span data-ttu-id="26732-147">Associação de recursos no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="26732-147">Resource binding in Direct3D 12</span></span>](resource-binding.md)
* [<span data-ttu-id="26732-148">Níveis de recursos de hardware</span><span class="sxs-lookup"><span data-stu-id="26732-148">Hardware feature levels</span></span>](hardware-feature-levels.md)
* [<span data-ttu-id="26732-149">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="26732-149">Root signatures</span></span>](root-signatures.md)