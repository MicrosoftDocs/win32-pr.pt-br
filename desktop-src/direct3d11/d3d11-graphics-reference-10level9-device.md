---
title: Métodos 10Level9 ID3D11Device
description: Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366455"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="77438-103">Métodos 10Level9 ID3D11Device</span><span class="sxs-lookup"><span data-stu-id="77438-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="77438-104">Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="77438-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="77438-105">ID3D11Device::CheckCounter</span><span class="sxs-lookup"><span data-stu-id="77438-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="77438-106">ID3D11Device::CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="77438-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="77438-107">ID3D11Device::CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="77438-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="77438-108">ID3D11Device:: createblendstate</span><span class="sxs-lookup"><span data-stu-id="77438-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="77438-109">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="77438-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="77438-110">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="77438-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="77438-111">ID3D11Device:: createcounterer</span><span class="sxs-lookup"><span data-stu-id="77438-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="77438-112">ID3D11Device::CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="77438-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="77438-113">ID3D11Device::CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="77438-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="77438-114">ID3D11Device::CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="77438-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="77438-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="77438-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="77438-116">ID3D11Device::CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="77438-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="77438-117">ID3D11Device::CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="77438-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="77438-118">ID3D11Device::CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="77438-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="77438-119">ID3D11Device:: predicado</span><span class="sxs-lookup"><span data-stu-id="77438-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="77438-120">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="77438-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="77438-121">ID3D11Device::CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="77438-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="77438-122">ID3D11Device::CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="77438-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="77438-123">ID3D11Device:: createsamplestate</span><span class="sxs-lookup"><span data-stu-id="77438-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="77438-124">ID3D11Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="77438-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="77438-125">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="77438-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="77438-126">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="77438-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="77438-127">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="77438-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="77438-128">ID3D11Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="77438-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="77438-129">ID3D11Device::CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="77438-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="77438-130">ID3D11Device::OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="77438-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="77438-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77438-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="77438-132">ID3D11Device::CheckCounter</span><span class="sxs-lookup"><span data-stu-id="77438-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-133">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-133">Feature Level</span></span></th>
<th><span data-ttu-id="77438-134">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-136">Os contadores dependentes do dispositivo têm suporte opcional.</span><span class="sxs-lookup"><span data-stu-id="77438-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="77438-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> para determinar o suporte. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="77438-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="77438-140">ID3D11Device::CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="77438-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-141">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-141">Feature Level</span></span></th>
<th><span data-ttu-id="77438-142">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-144">Consulte suporte de formato por <a href="overviews-direct3d-11-devices-downlevel-intro.md">nível de recurso</a>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="77438-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="77438-147">ID3D11Device::CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="77438-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-148">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-148">Feature Level</span></span></th>
<th><span data-ttu-id="77438-149">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-151">Os níveis de recurso não oferecem nenhuma garantia relativa ao suporte a MSAA. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="77438-154">ID3D11Device:: createblendstate</span><span class="sxs-lookup"><span data-stu-id="77438-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="77438-155">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-155">Feature Level</span></span>              | <span data-ttu-id="77438-156">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77438-157">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="77438-158">AlphaToCoverageEnable deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="77438-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="77438-159">Os primeiros quatro BlendEnables devem ter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="77438-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="77438-160">D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="77438-161">Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)</span><span class="sxs-lookup"><span data-stu-id="77438-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="77438-162">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="77438-163">AlphaToCoverageEnable deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="77438-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="77438-164">Os primeiros quatro BlendEnables devem ter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="77438-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="77438-165">Os primeiros quatro RenderTargetWriteMasks devem ter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="77438-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="77438-166">D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="77438-167">Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)</span><span class="sxs-lookup"><span data-stu-id="77438-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="77438-168">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="77438-169">AlphaToCoverageEnable deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="77438-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="77438-170">Os primeiros quatro BlendEnables devem ter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="77438-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="77438-171">D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="77438-172">Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)</span><span class="sxs-lookup"><span data-stu-id="77438-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="77438-173">Nível de recurso do D3D \_ \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77438-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="77438-174">Adiciona alfa para cobertura</span><span class="sxs-lookup"><span data-stu-id="77438-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="77438-175">ID3D11Device::CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="77438-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="77438-176">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-176">Feature Level</span></span>              | <span data-ttu-id="77438-177">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77438-178">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="77438-179">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="77438-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="77438-180">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="77438-181">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="77438-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="77438-182">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="77438-183">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="77438-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="77438-184">Nível de recurso do D3D \_ \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77438-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="77438-185">O membro *OutputMergerLogicOp* foi adicionado às opções de D3D11 de dados de recurso do D3D11, para determinar o suporte para operações lógicas (operações lógicas de bits de saída entre o sombreador de pixel e o conteúdo de destino de renderização, consulte [**D3D11 \_ renderizar \_ \_ \_ DESC1 Blend de destino**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). [**\_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)</span><span class="sxs-lookup"><span data-stu-id="77438-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="77438-186">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="77438-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-187">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-187">Feature Level</span></span></th>
<th><span data-ttu-id="77438-188">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="77438-190">Buffers não podem ter exibições de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="77438-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="77438-191">Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="77438-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="77438-192">Permite apenas buffers de índice com o formato DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="77438-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="77438-194">Buffers não podem ter exibições de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="77438-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="77438-195">Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="77438-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="77438-196">Permite buffers de índice com os formatos DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 e superior.</span><span class="sxs-lookup"><span data-stu-id="77438-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="77438-197">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="77438-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77438-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="77438-199">ID3D11Device:: createcounterer</span><span class="sxs-lookup"><span data-stu-id="77438-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-200">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-200">Feature Level</span></span></th>
<th><span data-ttu-id="77438-201">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-203">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="77438-206">ID3D11Device::CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="77438-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-207">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-207">Feature Level</span></span></th>
<th><span data-ttu-id="77438-208">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-210">Não dá suporte a estêncil de dois lados. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="77438-213">ID3D11Device::CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="77438-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-214">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-214">Feature Level</span></span></th>
<th><span data-ttu-id="77438-215">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77438-217">Sem suporte em nenhum nível de recurso 9. \* ou 10. \*.</span><span class="sxs-lookup"><span data-stu-id="77438-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="77438-218">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="77438-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77438-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77438-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77438-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="77438-223">ID3D11Device::CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="77438-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-224">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-224">Feature Level</span></span></th>
<th><span data-ttu-id="77438-225">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-227">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="77438-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="77438-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-231">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-231">Feature Level</span></span></th>
<th><span data-ttu-id="77438-232">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-234">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="77438-237">ID3D11Device::CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="77438-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-238">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-238">Feature Level</span></span></th>
<th><span data-ttu-id="77438-239">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77438-241">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77438-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77438-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77438-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="77438-246">ID3D11Device::CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="77438-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="77438-247">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-247">Feature Level</span></span>             | <span data-ttu-id="77438-248">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77438-249">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-250">Não dá suporte à \_ entrada \_ D3D11 \_ por \_ dados de instância</span><span class="sxs-lookup"><span data-stu-id="77438-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="77438-251">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-252">Não dá suporte à \_ entrada \_ D3D11 \_ por \_ dados de instância</span><span class="sxs-lookup"><span data-stu-id="77438-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="77438-253">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-254">O fluxo de vértice zero deve ter \_ entrada D3D11 \_ por \_ \_ dados de vértice, se qualquer fluxo tiver \_ dados de entrada D3D11 \_ por \_ vértice \_</span><span class="sxs-lookup"><span data-stu-id="77438-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="77438-255">Consulte o gráfico suporte de formato por [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) para obter detalhes sobre quais formatos podem ser usados para dados de vértice em cada nível de recurso.</span><span class="sxs-lookup"><span data-stu-id="77438-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="77438-256">ID3D11Device::CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="77438-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="77438-257">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-257">Feature Level</span></span>             | <span data-ttu-id="77438-258">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="77438-259">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-260">Deve usar o PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="77438-261">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-262">Deve usar o PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="77438-263">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-264">Deve usar PS \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="77438-265">ID3D11Device:: predicado</span><span class="sxs-lookup"><span data-stu-id="77438-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-266">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-266">Feature Level</span></span></th>
<th><span data-ttu-id="77438-267">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-269">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="77438-272">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="77438-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="77438-273">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-273">Feature Level</span></span>             | <span data-ttu-id="77438-274">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77438-275">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-276">Há suporte para consultas de evento.</span><span class="sxs-lookup"><span data-stu-id="77438-276">Event queries are supported.</span></span> <span data-ttu-id="77438-277">As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="77438-278">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-279">Há suporte para consultas de evento e oclusão.</span><span class="sxs-lookup"><span data-stu-id="77438-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="77438-280">As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="77438-281">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-282">Há suporte para consultas de evento e oclusão.</span><span class="sxs-lookup"><span data-stu-id="77438-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="77438-283">As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte.</span><span class="sxs-lookup"><span data-stu-id="77438-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="77438-284">ID3D11Device::CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="77438-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-285">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-285">Feature Level</span></span></th>
<th><span data-ttu-id="77438-286">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-288">DepthClipEnable deve ser <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="77438-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="77438-289">DepthBiasClamp deve ser definido como 0. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="77438-292">ID3D11Device::CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="77438-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-293">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-293">Feature Level</span></span></th>
<th><span data-ttu-id="77438-294">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-296">Só pode dar suporte a exibições de destino de renderização de objetos Texture2D. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="77438-299">ID3D11Device:: createsamplestate</span><span class="sxs-lookup"><span data-stu-id="77438-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-300">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-300">Feature Level</span></span></th>
<th><span data-ttu-id="77438-301">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="77438-303">Não há suporte para o filtro de comparação.</span><span class="sxs-lookup"><span data-stu-id="77438-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="77438-304">A cor da borda deve estar entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="77438-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="77438-305">Min LOD não pode ser fracionário</span><span class="sxs-lookup"><span data-stu-id="77438-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="77438-306">O LOD máximo deve ser FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="77438-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="77438-307">O máximo de anisotropy é 2.</span><span class="sxs-lookup"><span data-stu-id="77438-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="77438-308">Não há suporte para D3D11_TEXTURE_ADDRESS_MIRRORONCE.</span><span class="sxs-lookup"><span data-stu-id="77438-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="77438-310">Não há suporte para o filtro de comparação.</span><span class="sxs-lookup"><span data-stu-id="77438-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="77438-311">A cor da borda deve estar entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="77438-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="77438-312">Min LOD não pode ser fracionário</span><span class="sxs-lookup"><span data-stu-id="77438-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="77438-313">O LOD máximo deve ser FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="77438-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="77438-314">O máximo de anisotropy é 16.</span><span class="sxs-lookup"><span data-stu-id="77438-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="77438-315">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="77438-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77438-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="77438-317">ID3D11Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="77438-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="77438-318">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-318">Feature Level</span></span>             | <span data-ttu-id="77438-319">MostDetailedMip Plus MipLevels deve incluir o menor LOD (menor subrecurso</span><span class="sxs-lookup"><span data-stu-id="77438-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="77438-320">A exibição deve incluir todos os elementos da matriz de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="77438-321">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-322">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-322">Yes</span></span>                                                                          | <span data-ttu-id="77438-323">sim</span><span class="sxs-lookup"><span data-stu-id="77438-323">yes</span></span>                                           |
| <span data-ttu-id="77438-324">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-325">Sim</span><span class="sxs-lookup"><span data-stu-id="77438-325">Yes</span></span>                                                                          | <span data-ttu-id="77438-326">Sim</span><span class="sxs-lookup"><span data-stu-id="77438-326">Yes</span></span>                                           |
| <span data-ttu-id="77438-327">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-328">Sim</span><span class="sxs-lookup"><span data-stu-id="77438-328">Yes</span></span>                                                                          | <span data-ttu-id="77438-329">Sim</span><span class="sxs-lookup"><span data-stu-id="77438-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="77438-330">ID3D11Device::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="77438-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-331">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-331">Feature Level</span></span></th>
<th><span data-ttu-id="77438-332">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-334">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="77438-337">ID3D11Device::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="77438-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="77438-338">Os recursos Texture2D têm limites de largura e altura que diferem nos [níveis de recursos](overviews-direct3d-11-devices-downlevel-intro.md).</span><span class="sxs-lookup"><span data-stu-id="77438-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="77438-339">Nos níveis de recurso 9 \_ 3, os seguintes são mínimo garantidos, e implementações individuais podem exceder os requisitos.</span><span class="sxs-lookup"><span data-stu-id="77438-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="77438-340">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-340">Feature Level</span></span>             | <span data-ttu-id="77438-341">Se MipCount > 1, as dimensões devem ser uma potência integral de dois</span><span class="sxs-lookup"><span data-stu-id="77438-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="77438-342">Dimensão de textura mínima com suporte</span><span class="sxs-lookup"><span data-stu-id="77438-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="77438-343">As dimensões de texturas de cubo devem ser a potência de dois</span><span class="sxs-lookup"><span data-stu-id="77438-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="77438-344">Se \_ TEXTURECUBE for definido, as matrizes serão:</span><span class="sxs-lookup"><span data-stu-id="77438-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="77438-345">Se MISC \_ TEXTURECUBE não for definido, o arrays será.</span><span class="sxs-lookup"><span data-stu-id="77438-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="77438-346">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-347">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-347">Yes</span></span>                                                          | <span data-ttu-id="77438-348">2.048</span><span class="sxs-lookup"><span data-stu-id="77438-348">2048</span></span>                                | <span data-ttu-id="77438-349">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-349">Yes</span></span>                                           | <span data-ttu-id="77438-350">6</span><span class="sxs-lookup"><span data-stu-id="77438-350">6</span></span>                                              | <span data-ttu-id="77438-351">1</span><span class="sxs-lookup"><span data-stu-id="77438-351">1</span></span>                                                  |
| <span data-ttu-id="77438-352">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-353">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-353">Yes</span></span>                                                          | <span data-ttu-id="77438-354">2.048</span><span class="sxs-lookup"><span data-stu-id="77438-354">2048</span></span>                                | <span data-ttu-id="77438-355">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-355">Yes</span></span>                                           | <span data-ttu-id="77438-356">6</span><span class="sxs-lookup"><span data-stu-id="77438-356">6</span></span>                                              | <span data-ttu-id="77438-357">1</span><span class="sxs-lookup"><span data-stu-id="77438-357">1</span></span>                                                  |
| <span data-ttu-id="77438-358">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-359">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-359">Yes</span></span>                                                          | <span data-ttu-id="77438-360">4096</span><span class="sxs-lookup"><span data-stu-id="77438-360">4096</span></span>                                | <span data-ttu-id="77438-361">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-361">Yes</span></span>                                           | <span data-ttu-id="77438-362">6</span><span class="sxs-lookup"><span data-stu-id="77438-362">6</span></span>                                              | <span data-ttu-id="77438-363">1</span><span class="sxs-lookup"><span data-stu-id="77438-363">1</span></span>                                                  |



 

<span data-ttu-id="77438-364">Na tabela anterior, o nome completo de **misc \_ TEXTURECUBE** é [**D3D11 do \_ recurso \_ misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="77438-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="77438-365">Os itens a seguir são verdadeiros para todos os 9 \_ \* [níveis de recursos](overviews-direct3d-11-devices-downlevel-intro.md):</span><span class="sxs-lookup"><span data-stu-id="77438-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="77438-366">Ao usar o \_ \_ padrão de uso D3D11 ou o uso de D3D11 \_ \_ imutável, BindFlags não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="77438-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="77438-367">Ao usar o \_ \_ \_ estêncil de profundidade de D3D11 BIND, MipLevels deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="77438-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="77438-368">Ao usar o \_ recurso D3D11 BIND \_ Shader \_ , o SampleDesc. Count deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="77438-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="77438-369">Ao usar a \_ Associação D3D11 \_ presente, o recurso não pode ter o \_ recurso D3D11 BIND \_ Shader \_ .</span><span class="sxs-lookup"><span data-stu-id="77438-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="77438-370">Ao usar o \_ \_ recurso de DDI d3d10 \_ misc \_ compartilhado, o formato não pode ser o \_ formato dxgi \_ R8G8B8A8 \_ UNORM ou o \_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="77438-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="77438-371">ID3D11Device::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="77438-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="77438-372">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-372">Feature Level</span></span>             | <span data-ttu-id="77438-373">Dimensão máxima (qualquer eixo)</span><span class="sxs-lookup"><span data-stu-id="77438-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="77438-374">As dimensões devem ser forçadas de dois</span><span class="sxs-lookup"><span data-stu-id="77438-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="77438-375">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-376">256</span><span class="sxs-lookup"><span data-stu-id="77438-376">256</span></span>                          | <span data-ttu-id="77438-377">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-377">Yes</span></span>                             |
| <span data-ttu-id="77438-378">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-379">512</span><span class="sxs-lookup"><span data-stu-id="77438-379">512</span></span>                          | <span data-ttu-id="77438-380">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-380">Yes</span></span>                             |
| <span data-ttu-id="77438-381">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-382">512</span><span class="sxs-lookup"><span data-stu-id="77438-382">512</span></span>                          | <span data-ttu-id="77438-383">Yes</span><span class="sxs-lookup"><span data-stu-id="77438-383">Yes</span></span>                             |



 

<span data-ttu-id="77438-384">Se o recurso for D3D11 \_ uso \_ padrão ou o uso de D3D11 \_ \_ imutável, BindFlags não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="77438-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="77438-385">ID3D11Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="77438-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-386">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-386">Feature Level</span></span></th>
<th><span data-ttu-id="77438-387">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77438-389">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77438-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="77438-392">ID3D11Device::CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="77438-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="77438-393">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-393">Feature Level</span></span>             | <span data-ttu-id="77438-394">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="77438-395">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77438-396">Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="77438-397">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77438-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77438-398">Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="77438-399">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77438-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77438-400">Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77438-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="77438-401">ID3D11Device::OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="77438-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77438-402">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="77438-402">Feature Level</span></span></th>
<th><span data-ttu-id="77438-403">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="77438-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77438-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77438-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="77438-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> com o valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e a estrutura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> para determinar se um formato pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="77438-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="77438-406">Se o formato puder ser compartilhado, <strong>CheckFeatureSupport</strong> retornará o sinalizador <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="77438-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="77438-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca podem ser compartilhados ao usar o nível de recurso 9, mesmo que o dispositivo indique suporte a recursos opcionais para <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span><span class="sxs-lookup"><span data-stu-id="77438-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="77438-408">A tentativa de criar recursos compartilhados com formatos DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> sempre falhará, a menos que o nível de recurso seja 10_0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="77438-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="77438-409">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="77438-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77438-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77438-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77438-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77438-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="77438-412">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77438-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77438-413">Referência de 10Level9</span><span class="sxs-lookup"><span data-stu-id="77438-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

