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
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="c4e6f-104">Cargas de exibição de acesso não ordenado digitado</span><span class="sxs-lookup"><span data-stu-id="c4e6f-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="c4e6f-105">A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um formato DXGI específico \_ .</span><span class="sxs-lookup"><span data-stu-id="c4e6f-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="c4e6f-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c4e6f-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="c4e6f-107">Formatos e chamadas de API com suporte</span><span class="sxs-lookup"><span data-stu-id="c4e6f-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="c4e6f-108">Usando cargas UAV tipadas de HLSL</span><span class="sxs-lookup"><span data-stu-id="c4e6f-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="c4e6f-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4e6f-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="c4e6f-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c4e6f-110">Overview</span></span>

<span data-ttu-id="c4e6f-111">Um UAV (modo de exibição de acesso não ordenado) é uma exibição de um recurso de acesso não ordenado (que pode incluir buffers, texturas e matrizes de textura, embora sem várias amostras).</span><span class="sxs-lookup"><span data-stu-id="c4e6f-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="c4e6f-112">Um UAV permite acesso de leitura/gravação não ordenado de forma temporal de vários threads.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="c4e6f-113">Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="c4e6f-114">Esse acesso simultâneo é tratado por meio do uso de [funções atômicas](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="c4e6f-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="c4e6f-115">D3D12 e D3D 11.3 expande a lista de formatos que podem ser usados com cargas UAV tipadas.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="c4e6f-116">Formatos e chamadas de API com suporte</span><span class="sxs-lookup"><span data-stu-id="c4e6f-116">Supported formats and API calls</span></span>

<span data-ttu-id="c4e6f-117">Anteriormente, os três formatos a seguir suportavam cargas de UAV tipadas e eram necessárias para o hardware do D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="c4e6f-118">Eles têm suporte para todos os hardwares do D3D 11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="c4e6f-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-120">R32\_UINT</span></span>
-   <span data-ttu-id="c4e6f-121">R32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-121">R32\_SINT</span></span>

<span data-ttu-id="c4e6f-122">Os formatos a seguir têm suporte como um conjunto no hardware D3D12 ou D3D 11.3, portanto, se houver suporte para qualquer um, todos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="c4e6f-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="c4e6f-125">R32G32B32A32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="c4e6f-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="c4e6f-128">R16G16B16A16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="c4e6f-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="c4e6f-131">R8G8B8A8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="c4e6f-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-133">R16\_UINT</span></span>
-   <span data-ttu-id="c4e6f-134">R16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-134">R16\_SINT</span></span>
-   <span data-ttu-id="c4e6f-135">UNORM de R8 \_</span><span class="sxs-lookup"><span data-stu-id="c4e6f-135">R8\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-136">R8\_UINT</span></span>
-   <span data-ttu-id="c4e6f-137">R8, \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-137">R8\_SINT</span></span>

<span data-ttu-id="c4e6f-138">Os seguintes formatos são opcionalmente e individualmente suportados em hardware D3D12 e D3D 11.3, portanto, uma única consulta precisaria ser feita em cada formato para testar o suporte.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="c4e6f-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="c4e6f-143">R32G32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="c4e6f-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="c4e6f-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="c4e6f-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="c4e6f-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="c4e6f-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-152">R16G16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="c4e6f-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="c4e6f-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="c4e6f-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-156">8G8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="c4e6f-156">8G8\_SINT</span></span>
-   <span data-ttu-id="c4e6f-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-157">R16\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-158">R16\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-159">SNORM de R8 \_</span><span class="sxs-lookup"><span data-stu-id="c4e6f-159">R8\_SNORM</span></span>
-   <span data-ttu-id="c4e6f-160">\_UNORM a8</span><span class="sxs-lookup"><span data-stu-id="c4e6f-160">A8\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="c4e6f-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="c4e6f-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="c4e6f-164">Para determinar o suporte para todos os formatos adicionais, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com a estrutura de [**dados do \_ recurso D3D11 \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="c4e6f-165">O `TypedUAVLoadAdditionalFormats` bit será definido se a lista "com suporte como um conjunto" acima for suportada.</span><span class="sxs-lookup"><span data-stu-id="c4e6f-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="c4e6f-166">Faça uma segunda chamada para **CheckFeatureSupport**, usando uma [**estrutura \_ \_ SUPPORT2 de \_ formato \_ de dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (verificando a estrutura retornada em relação ao D3D12 formato SUPPORT2 \_ \_ \_ \_ \_ membro de carregamento digitado do [**\_ formato UAV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) D3D11 enum) para determinar o suporte na lista de formatos opcionalmente suportados acima, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c4e6f-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="c4e6f-167">Usando cargas UAV tipadas de HLSL</span><span class="sxs-lookup"><span data-stu-id="c4e6f-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="c4e6f-168">Para UAVs tipados, o sinalizador HLSL é o \_ sombreador do D3D \_ requer \_ \_ \_ formatos adicionais de carga UAV \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c4e6f-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="c4e6f-169">Aqui está um código de sombreador de exemplo para processar uma carga de UAV tipada:</span><span class="sxs-lookup"><span data-stu-id="c4e6f-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="c4e6f-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4e6f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e6f-171">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="c4e6f-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="c4e6f-172">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="c4e6f-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 