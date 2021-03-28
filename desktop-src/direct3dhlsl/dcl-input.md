---
title: dcl_input (sm4-ASM)
description: '\_entrada DCL (sm4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988620"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="4d014-103">\_entrada DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4d014-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="4d014-104">Declara um inregistrador de entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4d014-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="4d014-105">\_entrada DCL v *N \[ . Mask \] \[ , interpolação \]*</span><span class="sxs-lookup"><span data-stu-id="4d014-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d014-106">Item</span><span class="sxs-lookup"><span data-stu-id="4d014-106">Item</span></span></th>
<th><span data-ttu-id="4d014-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d014-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d014-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em></span><span class="sxs-lookup"><span data-stu-id="4d014-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="4d014-109">no Um registro de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="4d014-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="4d014-110"><em>N</em> é um inteiro que identifica o número do registro.</span><span class="sxs-lookup"><span data-stu-id="4d014-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="4d014-111"><em>[. Mask]</em> é uma máscara de componente opcional (. xyzw) que especifica qual dos componentes de registro usar.</span><span class="sxs-lookup"><span data-stu-id="4d014-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d014-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolação</em></span><span class="sxs-lookup"><span data-stu-id="4d014-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="4d014-113">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="4d014-113">[in] Optional.</span></span> <span data-ttu-id="4d014-114">O modo de interpolação, que é respeitado apenas em registros de entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="4d014-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="4d014-115">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4d014-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="4d014-116">constante-não interpolar entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="4d014-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="4d014-117">interpolar linearmente entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="4d014-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="4d014-118">linearCentroid-o mesmo que linear, mas de centróide clamped quando há multiamostragens.</span><span class="sxs-lookup"><span data-stu-id="4d014-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="4d014-119">linearNoperspective-igual à linear, mas sem correção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4d014-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="4d014-120">linearNoperspectiveCentroid-igual à linear, centróide clamped quando há multiamostragens, sem correção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4d014-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="4d014-121">Notas de interpolação</span><span class="sxs-lookup"><span data-stu-id="4d014-121">Interpolation Notes</span></span>

<span data-ttu-id="4d014-122">Por padrão, os atributos de vértice são interpolados de um centro de pixels ao executar a suavização de multiamostras.</span><span class="sxs-lookup"><span data-stu-id="4d014-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="4d014-123">Se um pixel Center não for coberto, um atributo será extrapolado para um pixel Center antes da interpolação.</span><span class="sxs-lookup"><span data-stu-id="4d014-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="4d014-124">Para um pixel que não está totalmente coberto ou um atributo que não cobre um pixel Center, você pode especificar a amostragem de centróide que força a amostragem a ocorrer em algum lugar dentro da área coberta do pixel.</span><span class="sxs-lookup"><span data-stu-id="4d014-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="4d014-125">Como uma máscara de exemplo (se usada) é aplicada antes de o centróide ser computado, qualquer local de exemplo mascarado pela máscara de exemplo não pode ser escolhido como um local de centróide.</span><span class="sxs-lookup"><span data-stu-id="4d014-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="4d014-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4d014-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d014-127">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4d014-127">Vertex Shader</span></span> | <span data-ttu-id="4d014-128">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="4d014-128">Geometry Shader</span></span> | <span data-ttu-id="4d014-129">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4d014-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4d014-130">x</span><span class="sxs-lookup"><span data-stu-id="4d014-130">x</span></span>             | <span data-ttu-id="4d014-131">x</span><span class="sxs-lookup"><span data-stu-id="4d014-131">x</span></span>               | <span data-ttu-id="4d014-132">x</span><span class="sxs-lookup"><span data-stu-id="4d014-132">x</span></span>            |



 

<span data-ttu-id="4d014-133">Para identificar a entrada como um valor do sistema, [use \_ a entrada DCL \_ VA (sm4-ASM)](dcl-input-sv.md).</span><span class="sxs-lookup"><span data-stu-id="4d014-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="4d014-134">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4d014-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4d014-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4d014-135">Example</span></span>

<span data-ttu-id="4d014-136">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="4d014-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4d014-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4d014-137">Minimum Shader Model</span></span>

<span data-ttu-id="4d014-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4d014-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d014-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4d014-139">Shader Model</span></span>                                              | <span data-ttu-id="4d014-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4d014-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d014-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4d014-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d014-142">sim</span><span class="sxs-lookup"><span data-stu-id="4d014-142">yes</span></span>       |
| [<span data-ttu-id="4d014-143">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4d014-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d014-144">sim</span><span class="sxs-lookup"><span data-stu-id="4d014-144">yes</span></span>       |
| [<span data-ttu-id="4d014-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4d014-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d014-146">sim</span><span class="sxs-lookup"><span data-stu-id="4d014-146">yes</span></span>       |
| [<span data-ttu-id="4d014-147">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d014-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d014-148">não</span><span class="sxs-lookup"><span data-stu-id="4d014-148">no</span></span>        |
| [<span data-ttu-id="4d014-149">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d014-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d014-150">não</span><span class="sxs-lookup"><span data-stu-id="4d014-150">no</span></span>        |
| [<span data-ttu-id="4d014-151">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d014-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d014-152">não</span><span class="sxs-lookup"><span data-stu-id="4d014-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d014-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d014-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d014-154">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d014-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





