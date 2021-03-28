---
title: dcl_sampler (sm4-ASM)
description: '\_amostra de DCL (sm4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104366812"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="cc971-103">\_amostra de DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cc971-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="cc971-104">Declara um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="cc971-104">Declares a sampler register.</span></span>



| <span data-ttu-id="cc971-105">a \_ amostra de DCL SN, modo</span><span class="sxs-lookup"><span data-stu-id="cc971-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc971-106">Item</span><span class="sxs-lookup"><span data-stu-id="cc971-106">Item</span></span></th>
<th><span data-ttu-id="cc971-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc971-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc971-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="cc971-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="cc971-109">no Um registro de amostra, em que <em>N</em> é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="cc971-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc971-110"><span id="mode"></span><span id="MODE"></span><em>moda</em></span><span class="sxs-lookup"><span data-stu-id="cc971-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="cc971-111">no Um modo de amostra, que restringe quais Estados de amostra (listados nos membros de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) são respeitados.</span><span class="sxs-lookup"><span data-stu-id="cc971-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="cc971-112">Os modos e os Estados são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc971-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc971-113">Mode</span><span class="sxs-lookup"><span data-stu-id="cc971-113">Mode</span></span></th>
<th><span data-ttu-id="cc971-114">Estados de amostra respeitados</span><span class="sxs-lookup"><span data-stu-id="cc971-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc971-115">padrão</span><span class="sxs-lookup"><span data-stu-id="cc971-115">default</span></span></td>
<td><span data-ttu-id="cc971-116"><em>Filter</em> (não pode usar os valores _COMPARISON ou _TEXT), <em>addressfield/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="cc971-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc971-117">comparação</span><span class="sxs-lookup"><span data-stu-id="cc971-117">comparison</span></span></td>
<td><span data-ttu-id="cc971-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>endereçou/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="cc971-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc971-119">mixagem</span><span class="sxs-lookup"><span data-stu-id="cc971-119">mono</span></span></td>
<td><span data-ttu-id="cc971-120"><em>Filter</em> (deve ser um dos _TEXT valores), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (esses dois Estados são estado global do dispositivo), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="cc971-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cc971-121">O modo restringe as instruções de exemplo que podem ser usadas; Esta tabela lista os métodos de objeto de textura que têm suporte para cada modo.</span><span class="sxs-lookup"><span data-stu-id="cc971-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="cc971-122">Um sistema operacional operando neste modo</span><span class="sxs-lookup"><span data-stu-id="cc971-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="cc971-123">Pode usar estes Texture-Object métodos</span><span class="sxs-lookup"><span data-stu-id="cc971-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc971-124">padrão</span><span class="sxs-lookup"><span data-stu-id="cc971-124">default</span></span>                          | <span data-ttu-id="cc971-125">[Exemplo](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="cc971-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="cc971-126">comparação</span><span class="sxs-lookup"><span data-stu-id="cc971-126">comparison</span></span>                       | <span data-ttu-id="cc971-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="cc971-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="cc971-128">mixagem</span><span class="sxs-lookup"><span data-stu-id="cc971-128">mono</span></span>                             | [<span data-ttu-id="cc971-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="cc971-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="cc971-130">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cc971-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cc971-131">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cc971-131">Vertex Shader</span></span> | <span data-ttu-id="cc971-132">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="cc971-132">Geometry Shader</span></span> | <span data-ttu-id="cc971-133">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="cc971-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cc971-134">x</span><span class="sxs-lookup"><span data-stu-id="cc971-134">x</span></span>             | <span data-ttu-id="cc971-135">x</span><span class="sxs-lookup"><span data-stu-id="cc971-135">x</span></span>               | <span data-ttu-id="cc971-136">x\*</span><span class="sxs-lookup"><span data-stu-id="cc971-136">x\*</span></span>          |



 

<span data-ttu-id="cc971-137">\* -O uso de uma amostra no modo mono tem suporte apenas em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="cc971-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="cc971-138">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="cc971-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="cc971-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cc971-139">Example</span></span>

<span data-ttu-id="cc971-140">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="cc971-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="cc971-141">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="cc971-141">Minimum Shader Model</span></span>

<span data-ttu-id="cc971-142">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cc971-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cc971-143">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cc971-143">Shader Model</span></span>                                              | <span data-ttu-id="cc971-144">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cc971-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cc971-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cc971-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cc971-146">sim</span><span class="sxs-lookup"><span data-stu-id="cc971-146">yes</span></span>       |
| [<span data-ttu-id="cc971-147">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cc971-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cc971-148">sim</span><span class="sxs-lookup"><span data-stu-id="cc971-148">yes</span></span>       |
| [<span data-ttu-id="cc971-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cc971-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cc971-150">sim</span><span class="sxs-lookup"><span data-stu-id="cc971-150">yes</span></span>       |
| [<span data-ttu-id="cc971-151">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc971-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cc971-152">não</span><span class="sxs-lookup"><span data-stu-id="cc971-152">no</span></span>        |
| [<span data-ttu-id="cc971-153">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc971-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cc971-154">não</span><span class="sxs-lookup"><span data-stu-id="cc971-154">no</span></span>        |
| [<span data-ttu-id="cc971-155">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc971-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cc971-156">não</span><span class="sxs-lookup"><span data-stu-id="cc971-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cc971-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc971-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc971-158">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc971-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

