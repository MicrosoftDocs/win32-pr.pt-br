---
title: dcl_input_sv (sm4-ASM)
description: '\_entrada DCL \_ VA (sm4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638897"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="4b919-103">\_entrada DCL \_ VA (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4b919-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="4b919-104">Declara um registro de entrada de sombreador que espera que um [valor de sistema](dx-graphics-hlsl-semantics.md) seja fornecido de um estágio anterior.</span><span class="sxs-lookup"><span data-stu-id="4b919-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="4b919-105">\_entrada DCL \_ VA v *N \[ . Mask \]* *\[ \] , systemValueName, interpolamode*</span><span class="sxs-lookup"><span data-stu-id="4b919-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b919-106">Item</span><span class="sxs-lookup"><span data-stu-id="4b919-106">Item</span></span></th>
<th><span data-ttu-id="4b919-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b919-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b919-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em></span><span class="sxs-lookup"><span data-stu-id="4b919-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="4b919-109">no Um registro de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="4b919-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="4b919-110"><em>N</em> é um inteiro que identifica o número do registro.</span><span class="sxs-lookup"><span data-stu-id="4b919-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="4b919-111"><em>[. Mask]</em> é uma máscara de componente opcional (. xyzw) que especifica qual dos componentes de registro usar.</span><span class="sxs-lookup"><span data-stu-id="4b919-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b919-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span><span class="sxs-lookup"><span data-stu-id="4b919-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="4b919-113">no O nome do valor do sistema que é uma cadeia de caracteres (consulte a <a href="dx-graphics-hlsl-semantics.md">semântica do valor do sistema</a>) sem o prefixo de &quot; SV_ &quot; .</span><span class="sxs-lookup"><span data-stu-id="4b919-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b919-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolação</em></span><span class="sxs-lookup"><span data-stu-id="4b919-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="4b919-115">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="4b919-115">[in] Optional.</span></span> <span data-ttu-id="4b919-116">O modo de interpolação que afeta como os valores são calculados durante a rasterização; o modo é usado apenas por um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="4b919-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="4b919-117">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4b919-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="4b919-118">constante-não interpolar entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="4b919-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="4b919-119">interpolar linearmente entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="4b919-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="4b919-120">linearCentroid-o mesmo que linear, mas de centróide clamped quando há multiamostragens.</span><span class="sxs-lookup"><span data-stu-id="4b919-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="4b919-121">linearNoperspective-igual à linear, mas sem correção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="4b919-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="4b919-122">linearNoperspectiveCentroid – o mesmo que linear, mas sem correção de perspectiva e centróide clamped quando há multiamostragens.</span><span class="sxs-lookup"><span data-stu-id="4b919-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4b919-123">Uma máscara de componente para uma declaração de valor de sistema pode ser qualquer subconjunto apropriado de \[ xyzw \] ; declarações não podem se sobrepor (cada declaração deve seguir a sequência xyzw).</span><span class="sxs-lookup"><span data-stu-id="4b919-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="4b919-124">Ao declarar valores de sistema escalares (distância de corte e distância de busca, por exemplo), você pode declarar vários valores de sistema em um único registro.</span><span class="sxs-lookup"><span data-stu-id="4b919-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="4b919-125">Se você fizer isso, certifique-se de que outros modificadores, como os modos de interpolação coincidam.</span><span class="sxs-lookup"><span data-stu-id="4b919-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="4b919-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4b919-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4b919-127">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4b919-127">Vertex Shader</span></span> | <span data-ttu-id="4b919-128">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="4b919-128">Geometry Shader</span></span> | <span data-ttu-id="4b919-129">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4b919-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4b919-130">x</span><span class="sxs-lookup"><span data-stu-id="4b919-130">x</span></span>             | <span data-ttu-id="4b919-131">x</span><span class="sxs-lookup"><span data-stu-id="4b919-131">x</span></span>               | <span data-ttu-id="4b919-132">x</span><span class="sxs-lookup"><span data-stu-id="4b919-132">x</span></span>            |



 

<span data-ttu-id="4b919-133">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4b919-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4b919-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4b919-134">Example</span></span>

<span data-ttu-id="4b919-135">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="4b919-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4b919-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4b919-136">Minimum Shader Model</span></span>

<span data-ttu-id="4b919-137">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4b919-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4b919-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4b919-138">Shader Model</span></span>                                              | <span data-ttu-id="4b919-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4b919-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4b919-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4b919-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4b919-141">sim</span><span class="sxs-lookup"><span data-stu-id="4b919-141">yes</span></span>       |
| [<span data-ttu-id="4b919-142">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4b919-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4b919-143">sim</span><span class="sxs-lookup"><span data-stu-id="4b919-143">yes</span></span>       |
| [<span data-ttu-id="4b919-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4b919-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4b919-145">sim</span><span class="sxs-lookup"><span data-stu-id="4b919-145">yes</span></span>       |
| [<span data-ttu-id="4b919-146">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b919-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4b919-147">não</span><span class="sxs-lookup"><span data-stu-id="4b919-147">no</span></span>        |
| [<span data-ttu-id="4b919-148">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b919-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4b919-149">não</span><span class="sxs-lookup"><span data-stu-id="4b919-149">no</span></span>        |
| [<span data-ttu-id="4b919-150">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b919-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4b919-151">não</span><span class="sxs-lookup"><span data-stu-id="4b919-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4b919-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b919-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b919-153">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4b919-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





