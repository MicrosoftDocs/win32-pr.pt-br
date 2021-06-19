---
title: Carregamentos de UAV (exibição de acesso não ordenado) digitados
description: Saiba mais sobre a carga digitada de UAV (exibição de acesso não ordenado) no Direct3D 12. A carga digitada UAV é a capacidade de um sombreador ler de um UAV com um DXGI_FORMAT específico.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394761"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="0494e-104">Carregamentos de UAV (exibição de acesso não ordenado) digitados</span><span class="sxs-lookup"><span data-stu-id="0494e-104">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="0494e-105">A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)específico.</span><span class="sxs-lookup"><span data-stu-id="0494e-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="0494e-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0494e-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="0494e-107">Formatos e chamadas de API com suporte</span><span class="sxs-lookup"><span data-stu-id="0494e-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="0494e-108">Usando cargas UAV tipadas de HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0494e-109">Usando UNORM e SNORM tipado UAV cargas de HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-109">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0494e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0494e-110">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="0494e-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0494e-111">Overview</span></span>

<span data-ttu-id="0494e-112">Um UAV (modo de exibição de acesso não ordenado) é uma exibição de um recurso de acesso não ordenado (que pode incluir buffers, texturas e matrizes de textura, embora sem várias amostras).</span><span class="sxs-lookup"><span data-stu-id="0494e-112">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="0494e-113">Um UAV permite acesso de leitura/gravação não ordenado de forma temporal de vários threads.</span><span class="sxs-lookup"><span data-stu-id="0494e-113">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="0494e-114">Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória.</span><span class="sxs-lookup"><span data-stu-id="0494e-114">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="0494e-115">Esse acesso simultâneo é tratado por meio do uso de [funções atômicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="0494e-115">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="0494e-116">D3D12 (e D3D 11.3) expande na lista de formatos que podem ser usados com cargas UAV tipadas.</span><span class="sxs-lookup"><span data-stu-id="0494e-116">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="0494e-117">Formatos e chamadas de API com suporte</span><span class="sxs-lookup"><span data-stu-id="0494e-117">Supported formats and API calls</span></span>

<span data-ttu-id="0494e-118">Anteriormente, os três formatos a seguir suportavam cargas de UAV tipadas e eram necessárias para o hardware do D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="0494e-118">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="0494e-119">Eles têm suporte para todos os hardwares do D3D 11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="0494e-119">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="0494e-120">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-120">R32\_FLOAT</span></span>
-   <span data-ttu-id="0494e-121">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-121">R32\_UINT</span></span>
-   <span data-ttu-id="0494e-122">R32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-122">R32\_SINT</span></span>

<span data-ttu-id="0494e-123">Os formatos a seguir têm suporte como um conjunto no hardware D3D12 ou D3D 11.3, portanto, se houver suporte para qualquer um, todos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0494e-123">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="0494e-124">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-124">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="0494e-125">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-125">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="0494e-126">R32G32B32A32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-126">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="0494e-127">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-127">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="0494e-128">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-128">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="0494e-129">R16G16B16A16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-129">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="0494e-130">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-130">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="0494e-131">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-131">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="0494e-132">R8G8B8A8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-132">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="0494e-133">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-133">R16\_FLOAT</span></span>
-   <span data-ttu-id="0494e-134">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-134">R16\_UINT</span></span>
-   <span data-ttu-id="0494e-135">R16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-135">R16\_SINT</span></span>
-   <span data-ttu-id="0494e-136">UNORM de R8 \_</span><span class="sxs-lookup"><span data-stu-id="0494e-136">R8\_UNORM</span></span>
-   <span data-ttu-id="0494e-137">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-137">R8\_UINT</span></span>
-   <span data-ttu-id="0494e-138">R8, \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-138">R8\_SINT</span></span>

<span data-ttu-id="0494e-139">Os seguintes formatos são opcionalmente e individualmente suportados em hardware D3D12 e D3D 11.3, portanto, uma única consulta precisaria ser feita em cada formato para testar o suporte.</span><span class="sxs-lookup"><span data-stu-id="0494e-139">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="0494e-140">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-140">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="0494e-141">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-141">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="0494e-142">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-142">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="0494e-143">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-143">R32G32\_UINT</span></span>
-   <span data-ttu-id="0494e-144">R32G32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-144">R32G32\_SINT</span></span>
-   <span data-ttu-id="0494e-145">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-145">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="0494e-146">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-146">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="0494e-147">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-147">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="0494e-148">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-148">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="0494e-149">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0494e-149">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="0494e-150">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-150">R16G16\_UNORM</span></span>
-   <span data-ttu-id="0494e-151">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-151">R16G16\_UINT</span></span>
-   <span data-ttu-id="0494e-152">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-152">R16G16\_SNORM</span></span>
-   <span data-ttu-id="0494e-153">R16G16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-153">R16G16\_SINT</span></span>
-   <span data-ttu-id="0494e-154">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-154">R8G8\_UNORM</span></span>
-   <span data-ttu-id="0494e-155">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0494e-155">R8G8\_UINT</span></span>
-   <span data-ttu-id="0494e-156">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-156">R8G8\_SNORM</span></span>
-   <span data-ttu-id="0494e-157">R8G8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="0494e-157">R8G8\_SINT</span></span>
-   <span data-ttu-id="0494e-158">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-158">R16\_UNORM</span></span>
-   <span data-ttu-id="0494e-159">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-159">R16\_SNORM</span></span>
-   <span data-ttu-id="0494e-160">SNORM de R8 \_</span><span class="sxs-lookup"><span data-stu-id="0494e-160">R8\_SNORM</span></span>
-   <span data-ttu-id="0494e-161">\_UNORM a8</span><span class="sxs-lookup"><span data-stu-id="0494e-161">A8\_UNORM</span></span>
-   <span data-ttu-id="0494e-162">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-162">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="0494e-163">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-163">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="0494e-164">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0494e-164">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="0494e-165">Para determinar o suporte para todos os formatos adicionais, chame [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) com a estrutura de opções de [**D3D12 de \_ dados de recurso \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) como o primeiro parâmetro (consulte a [consulta de funcionalidade](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="0494e-165">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="0494e-166">O campo *TypedUAVLoadAdditionalFormats* será definido se a lista "com suporte como um conjunto" acima for suportada.</span><span class="sxs-lookup"><span data-stu-id="0494e-166">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="0494e-167">Faça uma segunda chamada para **CheckFeatureSupport**, usando uma estrutura de [**suporte de formato de \_ dados de recurso \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (verificando a estrutura retornada no \_ formato D3D12 \_ SUPPORT2 \_ UAV \_ \_ de carregamento digitado do [**\_ formato D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) SUPPORT2 enum) para determinar o suporte na lista de formatos com suporte opcional listados acima, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0494e-167">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0494e-168">Usando cargas UAV tipadas de HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-168">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="0494e-169">Para UAVs tipados, o sinalizador HLSL é o \_ sombreador do D3D \_ requer \_ \_ \_ formatos adicionais de carga UAV \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0494e-169">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="0494e-170">Aqui está um código de sombreador de exemplo para processar uma carga de UAV tipada:</span><span class="sxs-lookup"><span data-stu-id="0494e-170">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0494e-171">Usando UNORM e SNORM tipado UAV cargas de HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-171">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="0494e-172">Ao usar carregamentos UAV tipados para ler de um recurso UNORM ou SNORM, você deve declarar corretamente o tipo de elemento do objeto HLSL como `unorm` ou `snorm` .</span><span class="sxs-lookup"><span data-stu-id="0494e-172">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="0494e-173">Ele é especificado como um comportamento indefinido para incompatibilidade do tipo de elemento declarado em HLSL com o tipo de dados de recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="0494e-173">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="0494e-174">Por exemplo, se você estiver usando cargas UAV tipadas em um recurso de buffer com dados de R8 \_ UNORM, deverá declarar o tipo de elemento como `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="0494e-174">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="0494e-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0494e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0494e-176">Renderização</span><span class="sxs-lookup"><span data-stu-id="0494e-176">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="0494e-177">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="0494e-177">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="0494e-178">Associação de recursos no HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-178">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="0494e-179">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="0494e-179">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="0494e-180">Como especificar assinaturas raiz no HLSL</span><span class="sxs-lookup"><span data-stu-id="0494e-180">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 