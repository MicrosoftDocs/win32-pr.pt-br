---
title: Especificando destinos do compilador
description: Aqui, listamos os destinos de vários perfis que o D3DCompile \ Functions e o compilador HLSL suportam.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366649"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="0496a-103">Especificando destinos do compilador</span><span class="sxs-lookup"><span data-stu-id="0496a-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="0496a-104">Você precisa especificar o destino do sombreador — conjunto de recursos do sombreador — para compilar ao chamar a função [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)ou [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="0496a-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="0496a-105">Aqui, listamos os destinos de vários perfis que as funções **D3DCompile \*** e o compilador HLSL suportam.</span><span class="sxs-lookup"><span data-stu-id="0496a-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="0496a-106">Níveis de recurso do Direct3D 11,0 e 11,1</span><span class="sxs-lookup"><span data-stu-id="0496a-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="0496a-107">Nível de recurso do Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="0496a-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="0496a-108">Nível de recurso do Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="0496a-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="0496a-109">Níveis de recurso do Direct3D 9,1, 9,2 e 9,3</span><span class="sxs-lookup"><span data-stu-id="0496a-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="0496a-110">Modelo de sombreador Direct3D 9 herdado 3,0</span><span class="sxs-lookup"><span data-stu-id="0496a-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="0496a-111">Modelo de sombreador Direct3D 9 herdado 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="0496a-112">Modelo de sombreador do Direct3D 9 herdado 1. x</span><span class="sxs-lookup"><span data-stu-id="0496a-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="0496a-113">Efeitos herdados</span><span class="sxs-lookup"><span data-stu-id="0496a-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="0496a-114">Observações</span><span class="sxs-lookup"><span data-stu-id="0496a-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="0496a-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0496a-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="0496a-116">Níveis de recurso do Direct3D 11,0 e 11,1</span><span class="sxs-lookup"><span data-stu-id="0496a-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="0496a-117">Aqui estão os destinos do sombreador para os quais [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 11,0 e 11,1 dão suporte.</span><span class="sxs-lookup"><span data-stu-id="0496a-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="0496a-118">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-118">Target</span></span>   | <span data-ttu-id="0496a-119">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-120">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-120">cs\_5\_0</span></span> | <span data-ttu-id="0496a-121">DirectCompute 5,0 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="0496a-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="0496a-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-122">ds\_5\_0</span></span> | [<span data-ttu-id="0496a-123">Sombreador de domínio</span><span class="sxs-lookup"><span data-stu-id="0496a-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="0496a-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-124">gs\_5\_0</span></span> | <span data-ttu-id="0496a-125">[Sombreador de geometria](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="0496a-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-126">hs\_5\_0</span></span> | [<span data-ttu-id="0496a-127">Sombreador envoltória</span><span class="sxs-lookup"><span data-stu-id="0496a-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="0496a-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-128">ps\_5\_0</span></span> | <span data-ttu-id="0496a-129">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="0496a-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-130">vs\_5\_0</span></span> | <span data-ttu-id="0496a-131">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="0496a-132">Nível de recurso do Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="0496a-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="0496a-133">Aqui estão os destinos de sombreador para os quais o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 10,1 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0496a-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="0496a-134">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-134">Target</span></span>   | <span data-ttu-id="0496a-135">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-136">cs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-136">cs\_4\_1</span></span> | <span data-ttu-id="0496a-137">DirectCompute 4,1 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="0496a-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="0496a-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-138">gs\_4\_1</span></span> | <span data-ttu-id="0496a-139">[Sombreador de geometria](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="0496a-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-140">ps\_4\_1</span></span> | <span data-ttu-id="0496a-141">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="0496a-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-142">vs\_4\_1</span></span> | <span data-ttu-id="0496a-143">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="0496a-144">Nível de recurso do Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="0496a-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="0496a-145">Aqui estão os destinos de sombreador para os quais o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 10,0 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0496a-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="0496a-146">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-146">Target</span></span>   | <span data-ttu-id="0496a-147">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-148">cs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-148">cs\_4\_0</span></span> | <span data-ttu-id="0496a-149">DirectCompute 4,0 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="0496a-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="0496a-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-150">gs\_4\_0</span></span> | <span data-ttu-id="0496a-151">[Sombreador de geometria](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="0496a-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-152">ps\_4\_0</span></span> | <span data-ttu-id="0496a-153">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="0496a-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-154">vs\_4\_0</span></span> | <span data-ttu-id="0496a-155">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0496a-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="0496a-156">Níveis de recurso do Direct3D 9,1, 9,2 e 9,3</span><span class="sxs-lookup"><span data-stu-id="0496a-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="0496a-157">Aqui estão os destinos do sombreador que [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 9,1, 9,2 e 9,3 dão suporte.</span><span class="sxs-lookup"><span data-stu-id="0496a-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="0496a-158">Ao usar os \* \_ perfis de \_ sombreador HLSL de 4% do \_ nível \_ 9 \_ x, você usa implicitamente os perfis do [Shader Model 2. x](dx-graphics-hlsl-sm2.md) para dar suporte ao hardware compatível com Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0496a-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="0496a-159">Os perfis do modelo de sombreador 2. x dão suporte a um comportamento de controle de fluxo mais limitado que o [sombreador modelo 4. x](dx-graphics-hlsl-sm4.md) e perfis posteriores.</span><span class="sxs-lookup"><span data-stu-id="0496a-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0496a-160">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-160">Target</span></span></th>
<th><span data-ttu-id="0496a-161">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0496a-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="0496a-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="0496a-163">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) para 9,1 e 9,2 (limites semelhantes a PS_2_0)</span><span class="sxs-lookup"><span data-stu-id="0496a-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="0496a-164">64 instruções de textura aritméticas e 32</span><span class="sxs-lookup"><span data-stu-id="0496a-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="0496a-165">12 registros temporários</span><span class="sxs-lookup"><span data-stu-id="0496a-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="0496a-166">4 níveis de leituras dependentes</span><span class="sxs-lookup"><span data-stu-id="0496a-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0496a-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="0496a-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="0496a-168"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de pixel</a> para 9,3 (limites semelhantes a ps_2_x ² com recursos adicionais do sombreador)</span><span class="sxs-lookup"><span data-stu-id="0496a-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="0496a-169">512 instruções</span><span class="sxs-lookup"><span data-stu-id="0496a-169">512 instructions</span></span></li>
<li><span data-ttu-id="0496a-170">registros temporários de 32</span><span class="sxs-lookup"><span data-stu-id="0496a-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="0496a-171">Controle de fluxo estático (profundidade máxima de 4)</span><span class="sxs-lookup"><span data-stu-id="0496a-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="0496a-172">Controle de fluxo dinâmico (profundidade máxima de 24)</span><span class="sxs-lookup"><span data-stu-id="0496a-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="0496a-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="0496a-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="0496a-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="0496a-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="0496a-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="0496a-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="0496a-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="0496a-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="0496a-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="0496a-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0496a-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="0496a-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="0496a-179"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértice</a> para 9,1 e 9,2 (semelhante a VS_2_0)</span><span class="sxs-lookup"><span data-stu-id="0496a-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="0496a-180">256 instruções</span><span class="sxs-lookup"><span data-stu-id="0496a-180">256 instructions</span></span></li>
<li><span data-ttu-id="0496a-181">12 registros temporários</span><span class="sxs-lookup"><span data-stu-id="0496a-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="0496a-182">Controle de fluxo estático (profundidade máxima de 1)</span><span class="sxs-lookup"><span data-stu-id="0496a-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0496a-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="0496a-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="0496a-184"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértice</a> para 9,3 (semelhante a vs_2_a ² com recursos e instanciação adicionais do sombreador)</span><span class="sxs-lookup"><span data-stu-id="0496a-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="0496a-185">256 instruções</span><span class="sxs-lookup"><span data-stu-id="0496a-185">256 instructions</span></span></li>
<li><span data-ttu-id="0496a-186">registros temporários de 32</span><span class="sxs-lookup"><span data-stu-id="0496a-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="0496a-187">Controle de fluxo estático (profundidade máxima de 4)</span><span class="sxs-lookup"><span data-stu-id="0496a-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="0496a-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="0496a-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="0496a-189">Modelo de sombreador Direct3D 9 herdado 3,0</span><span class="sxs-lookup"><span data-stu-id="0496a-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="0496a-190">Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="0496a-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="0496a-191">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-191">Target</span></span>    | <span data-ttu-id="0496a-192">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-193">ps\_3\_0</span></span>  | <span data-ttu-id="0496a-194">[Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="0496a-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="0496a-195">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0496a-195">ps\_3\_sw</span></span> | <span data-ttu-id="0496a-196">[Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="0496a-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="0496a-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-197">vs\_3\_0</span></span>  | <span data-ttu-id="0496a-198">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="0496a-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="0496a-199">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0496a-199">vs\_3\_sw</span></span> | <span data-ttu-id="0496a-200">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="0496a-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="0496a-201">Modelo de sombreador Direct3D 9 herdado 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="0496a-202">Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="0496a-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="0496a-203">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-203">Target</span></span>    | <span data-ttu-id="0496a-204">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-205">ps\_2\_0</span></span>  | <span data-ttu-id="0496a-206">[Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="0496a-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="0496a-207">ps\_2\_a</span></span>  | <span data-ttu-id="0496a-208">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="0496a-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="0496a-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="0496a-209">ps\_2\_b</span></span>  | <span data-ttu-id="0496a-210">[Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) 2B</span><span class="sxs-lookup"><span data-stu-id="0496a-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="0496a-211">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0496a-211">ps\_2\_sw</span></span> | <span data-ttu-id="0496a-212">Software do [pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="0496a-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-213">vs\_2\_0</span></span>  | <span data-ttu-id="0496a-214">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="0496a-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="0496a-215">vs\_2\_a</span></span>  | <span data-ttu-id="0496a-216">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="0496a-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="0496a-217">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0496a-217">vs\_2\_sw</span></span> | <span data-ttu-id="0496a-218">Software de [sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="0496a-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="0496a-219">Modelo de sombreador do Direct3D 9 herdado 1. x</span><span class="sxs-lookup"><span data-stu-id="0496a-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="0496a-220">Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 1. x ⁴.</span><span class="sxs-lookup"><span data-stu-id="0496a-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="0496a-221">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-221">Target</span></span>   | <span data-ttu-id="0496a-222">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0496a-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-223">tx\_1\_0</span></span> | <span data-ttu-id="0496a-224">Perfil de sombreador de textura que herdado D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) e [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span><span class="sxs-lookup"><span data-stu-id="0496a-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="0496a-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-225">vs\_1\_1</span></span> | <span data-ttu-id="0496a-226">[Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="0496a-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="0496a-227">Efeitos herdados</span><span class="sxs-lookup"><span data-stu-id="0496a-227">Legacy Effects</span></span>

<span data-ttu-id="0496a-228">Aqui estão os alvos de efeito para efeitos herdados.</span><span class="sxs-lookup"><span data-stu-id="0496a-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="0496a-229">Destino</span><span class="sxs-lookup"><span data-stu-id="0496a-229">Target</span></span>   | <span data-ttu-id="0496a-230">Description</span><span class="sxs-lookup"><span data-stu-id="0496a-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="0496a-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-231">fx\_2\_0</span></span> | <span data-ttu-id="0496a-232">Effects (FX) para o Direct3D 9 em D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="0496a-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="0496a-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-233">fx\_4\_0</span></span> | <span data-ttu-id="0496a-234">Effects (FX) para Direct3D 10,0 em D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="0496a-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="0496a-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0496a-235">fx\_4\_1</span></span> | <span data-ttu-id="0496a-236">Effects (FX) para Direct3D 10,1 em D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="0496a-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="0496a-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0496a-237">fx\_5\_0</span></span> | <span data-ttu-id="0496a-238">Effects (FX) para o Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="0496a-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="0496a-239">Observações</span><span class="sxs-lookup"><span data-stu-id="0496a-239">Notes</span></span>

<span data-ttu-id="0496a-240">Aqui estão algumas observações que as seções anteriores se referem a:</span><span class="sxs-lookup"><span data-stu-id="0496a-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="0496a-241">os dispositivos 10,0 e 10,1 de [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) podem, opcionalmente, dar suporte a DirectCompute.</span><span class="sxs-lookup"><span data-stu-id="0496a-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="0496a-242">Para verificar o suporte, use [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com o [**\_ recurso D3D11 \_ d3d10 \_ X \_ \_ Opções de hardware**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="0496a-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="0496a-243">o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requer efetivamente hardware que esteja em conformidade com os requisitos para o modelo de [sombreador do Direct3D 9 herdado 3,0](#legacy-direct3d-9-shader-model-30), mas esse nível de recurso não usa destinos vs \_ 3 \_ 0 ou PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="0496a-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="0496a-244">Use apenas modelos de sombreador Direct3D 9 herdados com a API do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0496a-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="0496a-245">Em vez disso, use os perfis 9. x com a API Direct3D 10. x e 11. x.</span><span class="sxs-lookup"><span data-stu-id="0496a-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="0496a-246">As funções **D3DCompile \*** do sombreador HLSL atuais não dão suporte a sombreadores de pixel herdados 1. x.</span><span class="sxs-lookup"><span data-stu-id="0496a-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="0496a-247">A última versão do HLSL para dar suporte a esses destinos foi D3DX9 na versão de outubro de 2006 do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="0496a-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="0496a-248">Todas as versões do D3DX e do SDK do DirectX foram preteridas.</span><span class="sxs-lookup"><span data-stu-id="0496a-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="0496a-249">Para obter mais informações, consulte [onde está o SDK do DirectX?](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="0496a-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0496a-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0496a-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0496a-251">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="0496a-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 