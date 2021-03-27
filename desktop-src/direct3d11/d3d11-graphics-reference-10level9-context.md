---
title: Métodos 10Level9 ID3D11DeviceContext
description: Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005054"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="30a3f-103">Métodos 10Level9 ID3D11DeviceContext</span><span class="sxs-lookup"><span data-stu-id="30a3f-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="30a3f-104">Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="30a3f-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="30a3f-105">ID3D11DeviceContext::CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="30a3f-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="30a3f-106">ID3D11DeviceContext::CopyResource</span><span class="sxs-lookup"><span data-stu-id="30a3f-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="30a3f-107">ID3D11DeviceContext::CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="30a3f-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="30a3f-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="30a3f-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="30a3f-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="30a3f-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="30a3f-110">ID3D11DeviceContext::ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="30a3f-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="30a3f-111">ID3D11DeviceContext::CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="30a3f-112">ID3D11DeviceContext::CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="30a3f-113">ID3D11DeviceContext::CSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="30a3f-114">ID3D11DeviceContext::CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="30a3f-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="30a3f-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="30a3f-116">ID3D11DeviceContext::D ispatch</span><span class="sxs-lookup"><span data-stu-id="30a3f-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="30a3f-117">ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="30a3f-118">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="30a3f-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="30a3f-119">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="30a3f-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="30a3f-120">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="30a3f-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="30a3f-121">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="30a3f-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="30a3f-122">ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="30a3f-123">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="30a3f-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="30a3f-124">ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="30a3f-125">ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="30a3f-126">ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="30a3f-127">ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="30a3f-128">ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="30a3f-129">ID3D11DeviceContext::GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="30a3f-130">ID3D11DeviceContext::GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="30a3f-131">ID3D11DeviceContext::GSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="30a3f-132">ID3D11DeviceContext::GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="30a3f-133">ID3D11DeviceContext::HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="30a3f-134">ID3D11DeviceContext::HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="30a3f-135">ID3D11DeviceContext::HSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="30a3f-136">ID3D11DeviceContext::HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="30a3f-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="30a3f-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="30a3f-138">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="30a3f-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="30a3f-139">ID3D11DeviceContext::OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="30a3f-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="30a3f-140">ID3D11DeviceContext::OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="30a3f-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="30a3f-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="30a3f-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="30a3f-142">ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="30a3f-143">ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="30a3f-144">ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="30a3f-145">ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="30a3f-146">ID3D11DeviceContext::RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="30a3f-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="30a3f-147">ID3D11DeviceContext::RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="30a3f-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="30a3f-148">ID3D11DeviceContext::SetPredication</span><span class="sxs-lookup"><span data-stu-id="30a3f-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="30a3f-149">ID3D11DeviceContext::SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="30a3f-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="30a3f-150">ID3D11DeviceContext::VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="30a3f-151">ID3D11DeviceContext::VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="30a3f-152">ID3D11DeviceContext::VSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="30a3f-153">ID3D11DeviceContext::VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="30a3f-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30a3f-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="30a3f-155">ID3D11DeviceContext::CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="30a3f-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-156">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-156">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-157">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="30a3f-159">Somente Texture2D e buffers podem ser copiados na memória acessível por GPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-160">Texture3D não pode ser copiado da memória acessível por GPU para a memória acessível pela CPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-161">Qualquer recurso que tenha apenas D3D10_BIND_SHADER_RESOURCE não pode ser copiado da memória acessível por GPU para memória acessível por CPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-162">Não é possível copiar as texturas do volume mipmapped.</span><span class="sxs-lookup"><span data-stu-id="30a3f-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="30a3f-163">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="30a3f-166">ID3D11DeviceContext::CopyResource</span><span class="sxs-lookup"><span data-stu-id="30a3f-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-167">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-167">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-168">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="30a3f-170">Somente Texture2D e buffers podem ser copiados na memória acessível por GPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-171">Texture3D não pode ser copiado da memória acessível por GPU para a memória acessível pela CPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-172">Qualquer recurso que tenha apenas D3D10_BIND_SHADER_RESOURCE não pode ser copiado da memória acessível por GPU para memória acessível por CPU.</span><span class="sxs-lookup"><span data-stu-id="30a3f-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="30a3f-173">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="30a3f-176">ID3D11DeviceContext::CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="30a3f-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-177">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-177">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-178">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-180">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="30a3f-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="30a3f-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-184">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-184">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-185">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-187">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="30a3f-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="30a3f-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-191">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-191">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-192">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-194">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="30a3f-197">ID3D11DeviceContext::ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="30a3f-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-198">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-198">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-199">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-201">Somente a primeira fatia da matriz será apagada.</span><span class="sxs-lookup"><span data-stu-id="30a3f-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="30a3f-202">Os aplicativos devem criar uma exibição de destino de renderização para cada fatia de face ou matriz e, em seguida, limpar cada exibição individualmente. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="30a3f-205">ID3D11DeviceContext::CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-206">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-206">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-207">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-209">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="30a3f-212">ID3D11DeviceContext::CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-213">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-213">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-214">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-216">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="30a3f-219">ID3D11DeviceContext::CSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-220">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-220">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-221">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-223">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="30a3f-226">ID3D11DeviceContext::CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-227">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-227">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-228">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-230">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="30a3f-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="30a3f-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-234">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-234">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-235">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-237">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="30a3f-240">ID3D11DeviceContext::D ispatch</span><span class="sxs-lookup"><span data-stu-id="30a3f-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-241">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-241">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-242">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-244">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="30a3f-247">ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-248">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-248">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-249">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-251">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="30a3f-254">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="30a3f-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="30a3f-255">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-255">Feature Level</span></span>             | <span data-ttu-id="30a3f-256">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a3f-257">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="30a3f-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="30a3f-258">O número de primitivos não pode exceder 65535.</span><span class="sxs-lookup"><span data-stu-id="30a3f-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="30a3f-259">As texturas não podem se repetir em um primitivo mais de 128 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="30a3f-260">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="30a3f-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="30a3f-261">O número de primitivos não pode exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-262">As texturas não podem se repetir em um primitivo mais de 2048 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="30a3f-263">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="30a3f-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="30a3f-264">O número de primitivos não pode exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-265">As texturas não podem se repetir em um primitivo mais de 8192 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="30a3f-266">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="30a3f-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-267">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-267">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-268">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-270">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="30a3f-273">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="30a3f-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="30a3f-274">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-274">Feature Level</span></span>             | <span data-ttu-id="30a3f-275">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a3f-276">Nível de recurso do D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="30a3f-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="30a3f-277">O número de primitivos não pode exceder 65535.</span><span class="sxs-lookup"><span data-stu-id="30a3f-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="30a3f-278">As texturas não podem se repetir em um primitivo mais de 128 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="30a3f-279">Os valores de índice não podem exceder 65534.</span><span class="sxs-lookup"><span data-stu-id="30a3f-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="30a3f-280">Não há suporte para listas de pontos indexados.</span><span class="sxs-lookup"><span data-stu-id="30a3f-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="30a3f-281">Nível de recurso do D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="30a3f-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="30a3f-282">O número de primitivos não pode exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-283">As texturas não podem se repetir em um primitivo mais de 2048 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="30a3f-284">Os valores de índice não podem exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-285">Não há suporte para listas de pontos indexados.</span><span class="sxs-lookup"><span data-stu-id="30a3f-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="30a3f-286">Nível de recurso do D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="30a3f-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="30a3f-287">O número de primitivos não pode exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-288">As texturas não podem se repetir em um primitivo mais de 8192 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="30a3f-289">Os valores de índice não podem exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-290">Não há suporte para listas de pontos indexados.</span><span class="sxs-lookup"><span data-stu-id="30a3f-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="30a3f-291">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="30a3f-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-292">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-292">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-293">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="30a3f-295">Sem suporte $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="30a3f-298">O número de primitivos não pode exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="30a3f-299">As texturas não podem se repetir em um primitivo mais de 8192 vezes.</span><span class="sxs-lookup"><span data-stu-id="30a3f-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="30a3f-300">Os valores de índice não podem exceder 1048575.</span><span class="sxs-lookup"><span data-stu-id="30a3f-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30a3f-301">Quando você chama o método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> com um sombreador de vértice que está associado ao pipeline e que não importa nenhum dado por instância, alguns hardwares de gráficos do Direct3D 9 podem não desenhar nada.</span><span class="sxs-lookup"><span data-stu-id="30a3f-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="30a3f-302">Em particular, se o sombreador de vértice não usar nenhum dado por instância, chamar <strong>DrawIndexedInstanced</strong> com 1 instância não será equivalente a chamar <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>draw</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="30a3f-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="30a3f-303">ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-304">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-304">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-305">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-307">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="30a3f-312">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="30a3f-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-313">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-313">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-314">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-316">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="30a3f-319">ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="30a3f-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-320">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-320">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-321">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-323">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="30a3f-328">ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-329">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-329">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-330">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-332">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="30a3f-337">ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-338">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-338">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-339">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-341">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="30a3f-346">ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-347">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-347">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-348">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-350">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="30a3f-355">ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-356">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-356">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-357">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-359">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="30a3f-364">ID3D11DeviceContext::GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-365">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-365">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-366">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-368">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="30a3f-371">ID3D11DeviceContext::GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-372">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-372">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-373">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-375">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="30a3f-378">ID3D11DeviceContext::GSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-379">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-379">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-380">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-382">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="30a3f-385">ID3D11DeviceContext::GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-386">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-386">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-387">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-389">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="30a3f-392">ID3D11DeviceContext::HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-393">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-393">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-394">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-396">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="30a3f-401">ID3D11DeviceContext::HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-402">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-402">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-403">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-405">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="30a3f-410">ID3D11DeviceContext::HSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-411">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-411">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-412">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-414">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="30a3f-419">ID3D11DeviceContext::HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-420">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-420">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-421">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="30a3f-423">Sem suporte em qualquer nível de recurso 9. \* ou 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="30a3f-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="30a3f-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="30a3f-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-429">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-429">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-430">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="30a3f-432">O formato pode ser diferente daquele especificado na criação do buffer, mas uma tradução cara será incorrida.</span><span class="sxs-lookup"><span data-stu-id="30a3f-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="30a3f-433">Permite apenas buffers de índice com o formato DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="30a3f-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="30a3f-435">O formato pode ser diferente daquele especificado na criação do buffer, mas uma tradução cara será incorrida.</span><span class="sxs-lookup"><span data-stu-id="30a3f-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="30a3f-436">Permite buffers de índice com os formatos DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 e superior.</span><span class="sxs-lookup"><span data-stu-id="30a3f-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="30a3f-437">$ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="30a3f-439">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="30a3f-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-440">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-440">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-441">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-443">Não há suporte para topologias primitivas com adjacência $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="30a3f-446">ID3D11DeviceContext::OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="30a3f-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-447">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-447">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-448">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-450">SampleMask não pode ser zero $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="30a3f-453">ID3D11DeviceContext::OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="30a3f-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-454">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-454">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-455">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="30a3f-457">Somente um destino de renderização tem suporte para $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="30a3f-460">Somente quatro destinos de renderização têm suporte e todos os recursos associados devem ter a mesma profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="30a3f-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="30a3f-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="30a3f-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-462">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-462">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-463">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-465">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="30a3f-468">ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-469">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-469">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-470">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-472">Consulte nível de recurso 10,0, mas o número total de constantes usadas pelo sombreador não pode exceder 32 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="30a3f-475">ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-476">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-476">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-477">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-479">No máximo 16 amostras podem ser associadas $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="30a3f-482">ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-483">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-483">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-484">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="30a3f-486">Somente ps_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="30a3f-489">Somente ps_4_0_level_9_3 ou ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="30a3f-490">ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-491">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-491">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-492">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-494">Não mais que 8 recursos de sombreador vinculados simultaneamente $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="30a3f-497">ID3D11DeviceContext::RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="30a3f-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-498">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-498">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-499">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-501">Somente o Rect inicial de tesoura está disponível $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="30a3f-504">ID3D11DeviceContext::RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="30a3f-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-505">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-505">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-506">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-508">Somente o visor inicial está disponível $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="30a3f-511">Embora você especifique valores float para os membros da estrutura do [**\_ visor D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) para a matriz *pViewports* em uma chamada para [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [os níveis de recursos](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** usa DWORDs internamente.</span><span class="sxs-lookup"><span data-stu-id="30a3f-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="30a3f-512">Devido a esse comportamento, quando você usa um canto superior esquerdo negativo para o visor, a chamada para **RSSetViewports** para os níveis de recursos 9 \_ x falha.</span><span class="sxs-lookup"><span data-stu-id="30a3f-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="30a3f-513">Essa falha ocorre porque o **RSSetViewports** para 9 \_ x converte os valores de ponto flutuante em inteiros não assinados sem validação, o que resulta em um estouro de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="30a3f-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="30a3f-514">A chamada para [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [os níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x e 11 \_ x funciona como esperado mesmo quando você usa um canto superior esquerdo negativo para o visor.</span><span class="sxs-lookup"><span data-stu-id="30a3f-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="30a3f-515">ID3D11DeviceContext::SetPredication</span><span class="sxs-lookup"><span data-stu-id="30a3f-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-516">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-516">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-517">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-519">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="30a3f-522">ID3D11DeviceContext::SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="30a3f-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-523">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-523">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-524">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-526">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="30a3f-529">ID3D11DeviceContext::VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="30a3f-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-530">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-530">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-531">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-533">Consulte nível de recurso 10,0, mas o número total de constantes usadas pelo sombreador não pode exceder 255 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="30a3f-536">ID3D11DeviceContext::VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="30a3f-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-537">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-537">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-538">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-540">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="30a3f-543">ID3D11DeviceContext::VSSetShader</span><span class="sxs-lookup"><span data-stu-id="30a3f-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-544">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-544">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-545">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="30a3f-547">Somente vs_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="30a3f-550">Somente vs_4_0_level_9_3 ou vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="30a3f-551">ID3D11DeviceContext::VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="30a3f-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30a3f-552">Nível de recursos</span><span class="sxs-lookup"><span data-stu-id="30a3f-552">Feature Level</span></span></th>
<th><span data-ttu-id="30a3f-553">Diferenças de comportamento</span><span class="sxs-lookup"><span data-stu-id="30a3f-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30a3f-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="30a3f-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="30a3f-555">Sem suporte em nenhum nível de recurso de 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="30a3f-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="30a3f-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="30a3f-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30a3f-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="30a3f-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="30a3f-558">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30a3f-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a3f-559">Referência de 10Level9</span><span class="sxs-lookup"><span data-stu-id="30a3f-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





