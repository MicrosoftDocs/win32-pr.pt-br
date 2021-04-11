---
description: Sinalizadores de recurso primitivos de driver diversos.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164115"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="14190-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="14190-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="14190-104">Sinalizadores de recurso primitivos de driver diversos.</span><span class="sxs-lookup"><span data-stu-id="14190-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14190-105">#definir</span><span class="sxs-lookup"><span data-stu-id="14190-105">#define</span></span></td>
<td><span data-ttu-id="14190-106">Valor</span><span class="sxs-lookup"><span data-stu-id="14190-106">Value</span></span></td>
<td><span data-ttu-id="14190-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="14190-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="14190-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="14190-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="14190-109">0x00000002L</span></span></td>
<td><span data-ttu-id="14190-110">O dispositivo pode habilitar e desabilitar a modificação do buffer de profundidade em operações de pixel.</span><span class="sxs-lookup"><span data-stu-id="14190-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="14190-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="14190-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="14190-112">0x00000010L</span></span></td>
<td><span data-ttu-id="14190-113">O driver não executa a remoção de triângulo.</span><span class="sxs-lookup"><span data-stu-id="14190-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="14190-114">Isso corresponde ao membro de D3DCULL_NONE do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="14190-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="14190-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="14190-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="14190-116">0x00000020L</span></span></td>
<td><span data-ttu-id="14190-117">O driver dá suporte à seleção de triângulo no sentido horário por meio do estado de D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="14190-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="14190-118">(Isso se aplica somente a primitivas de triângulo.) Esse sinalizador corresponde ao membro de D3DCULL_CW do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="14190-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="14190-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="14190-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="14190-120">0x00000040L</span></span></td>
<td><span data-ttu-id="14190-121">O driver dá suporte à seleção no sentido anti-horário por meio do estado de D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="14190-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="14190-122">(Isso se aplica somente a primitivas de triângulo.) Esse sinalizador corresponde ao membro de D3DCULL_CCW do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="14190-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="14190-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="14190-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="14190-124">0x00000100L</span></span></td>
<td><span data-ttu-id="14190-125">O dispositivo dá suporte a gravações por canal para o buffer de cores de destino de renderização por meio do estado de D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="14190-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="14190-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="14190-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="14190-127">0x00000200L</span></span></td>
<td><span data-ttu-id="14190-128">O dispositivo corta corretamente os pontos dimensionados de tamanho maior que 1,0 para os planos de recorte definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="14190-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="14190-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="14190-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="14190-130">0x00000200L</span></span></td>
<td><span data-ttu-id="14190-131">Os clipes de dispositivo transformam primitivas de vértice.</span><span class="sxs-lookup"><span data-stu-id="14190-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="14190-132">Especifique D3DUSAGE_DONOTCLIP quando o pipeline não deve fazer recorte.</span><span class="sxs-lookup"><span data-stu-id="14190-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="14190-133">Nesse caso, pode ser necessário recortar o software adicional no momento do desenho, exigindo que o buffer de vértice esteja na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="14190-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="14190-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="14190-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="14190-135">0x00000400L</span></span></td>
<td><span data-ttu-id="14190-136">O dispositivo dá suporte a <a href="d3dta.md">D3DTA</a> para registro temporário.</span><span class="sxs-lookup"><span data-stu-id="14190-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="14190-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="14190-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="14190-138">0x00000800L</span></span></td>
<td><span data-ttu-id="14190-139">O dispositivo dá suporte a operações de mesclagem alfa diferentes de D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="14190-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="14190-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="14190-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="14190-141">0x00000100L</span></span></td>
<td><span data-ttu-id="14190-142">Um dispositivo de referência que não é renderizado.</span><span class="sxs-lookup"><span data-stu-id="14190-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="14190-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="14190-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="14190-144">0x00004000L</span></span></td>
<td><span data-ttu-id="14190-145">O dispositivo dá suporte a máscaras de gravação independentes para várias texturas de elementos ou vários destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="14190-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="14190-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="14190-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="14190-147">0x00008000L</span></span></td>
<td><span data-ttu-id="14190-148">O dispositivo dá suporte a constantes por estágio.</span><span class="sxs-lookup"><span data-stu-id="14190-148">Device supports per-stage constants.</span></span> <span data-ttu-id="14190-149">Consulte D3DTSS_CONSTANT em <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="14190-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="14190-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="14190-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="14190-151">0x00200000L</span></span></td>
<td><span data-ttu-id="14190-152">O dispositivo dá suporte à conversão para sRGB após a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="14190-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14190-153">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="14190-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="14190-154">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="14190-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="14190-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="14190-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="14190-156">0x00010000L</span></span></td>
<td><span data-ttu-id="14190-157">O dispositivo dá suporte a sombra separada e alfa especular Alpha.</span><span class="sxs-lookup"><span data-stu-id="14190-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="14190-158">Muitos dispositivos usam o canal alfa especular para armazenar o fator de neblina.</span><span class="sxs-lookup"><span data-stu-id="14190-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="14190-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="14190-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="14190-160">0x00020000L</span></span></td>
<td><span data-ttu-id="14190-161">O dispositivo dá suporte a configurações de mesclagem separadas para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="14190-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="14190-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="14190-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="14190-163">0x00040000L</span></span></td>
<td><span data-ttu-id="14190-164">O dispositivo dá suporte a diferentes profundidades de bits para vários destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="14190-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14190-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="14190-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="14190-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="14190-166">0x00080000L</span></span></td>
<td><span data-ttu-id="14190-167">O dispositivo dá suporte a operações de sombreador pós-pixel para vários destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="14190-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14190-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="14190-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="14190-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="14190-169">0x00100000L</span></span></td>
<td><span data-ttu-id="14190-170">Fator de mistura de dispositivo coloca de neblina por vértice.</span><span class="sxs-lookup"><span data-stu-id="14190-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="14190-171">Essas constantes são usadas pelo membro PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="14190-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="14190-172">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="14190-172">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="14190-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14190-173">Header</span></span>                   | <span data-ttu-id="14190-174">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="14190-174">d3d9caps.h</span></span> |
| <span data-ttu-id="14190-175">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="14190-175">Minimum operating system</span></span> | <span data-ttu-id="14190-176">Windows 98</span><span class="sxs-lookup"><span data-stu-id="14190-176">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="14190-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14190-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14190-178">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="14190-178">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
