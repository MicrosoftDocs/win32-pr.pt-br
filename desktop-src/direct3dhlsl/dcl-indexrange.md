---
title: dcl_indexRange (sm4-ASM)
description: DCL \_ indexRange (sm4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967137"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="3e085-103">DCL \_ indexRange (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3e085-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="3e085-104">Declara um intervalo de registros que serão acessados pelo índice (um inteiro calculado no sombreador).</span><span class="sxs-lookup"><span data-stu-id="3e085-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="3e085-105">DCL \_ IndexRange *minRegisterM*, *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="3e085-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e085-106">Item</span><span class="sxs-lookup"><span data-stu-id="3e085-106">Item</span></span></th>
<th><span data-ttu-id="3e085-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e085-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e085-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span><span class="sxs-lookup"><span data-stu-id="3e085-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="3e085-109">no O primeiro registro a ser acessado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="3e085-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="3e085-110"><em>minRegister</em> é <strong>v</strong> para um vértice ou registro de entrada de sombreador de pixel ou <strong>o</strong> para um registro de saída de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="3e085-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="3e085-111"><em>M</em> é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="3e085-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e085-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="3e085-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="3e085-113">no O último registro a ser acessado por índice.</span><span class="sxs-lookup"><span data-stu-id="3e085-113">[in] The last register to access by index.</span></span> <span data-ttu-id="3e085-114">A mesma forma que <em>minRegister</em> , exceto <em>N</em> é o número de registrador.</span><span class="sxs-lookup"><span data-stu-id="3e085-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3e085-115">As seguintes restrições se aplicam a todos os registros:</span><span class="sxs-lookup"><span data-stu-id="3e085-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="3e085-116">Os registros mínimo e máximo devem ser do mesmo tipo e ter as mesmas máscaras de componente (se as máscaras forem declaradas).</span><span class="sxs-lookup"><span data-stu-id="3e085-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="3e085-117">Um registro pode ter vários intervalos de índice, desde que não haja sobreposição.</span><span class="sxs-lookup"><span data-stu-id="3e085-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="3e085-118">O número de registro mínimo deve ser menor que o número de registro máximo.</span><span class="sxs-lookup"><span data-stu-id="3e085-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="3e085-119">Um registro de índice não pode conter um [valor de sistema](dx-graphics-hlsl-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="3e085-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="3e085-120">A indexação de um registro fora da declaração de índice máximo produz resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3e085-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="3e085-121">Os registros de entrada do sombreador de pixel devem usar o mesmo modo de interpolação; os registros de saída do sombreador de pixel não podem ser indexados.</span><span class="sxs-lookup"><span data-stu-id="3e085-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="3e085-122">Um registro de entrada do sombreador de geometria tem duas dimensões (eixo de vértice, eixo de atributo); o intervalo de índice aplica-se somente ao eixo de atributo porque o eixo de vértice é sempre totalmente indexável.</span><span class="sxs-lookup"><span data-stu-id="3e085-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="3e085-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="3e085-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3e085-124">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e085-124">Vertex Shader</span></span> | <span data-ttu-id="3e085-125">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="3e085-125">Geometry Shader</span></span> | <span data-ttu-id="3e085-126">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3e085-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3e085-127">x</span><span class="sxs-lookup"><span data-stu-id="3e085-127">x</span></span>             | <span data-ttu-id="3e085-128">x</span><span class="sxs-lookup"><span data-stu-id="3e085-128">x</span></span>               | <span data-ttu-id="3e085-129">x</span><span class="sxs-lookup"><span data-stu-id="3e085-129">x</span></span>            |



 

<span data-ttu-id="3e085-130">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="3e085-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="3e085-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3e085-131">Example</span></span>

<span data-ttu-id="3e085-132">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="3e085-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="3e085-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3e085-133">Minimum Shader Model</span></span>

<span data-ttu-id="3e085-134">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3e085-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3e085-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3e085-135">Shader Model</span></span>                                              | <span data-ttu-id="3e085-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3e085-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3e085-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3e085-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3e085-138">sim</span><span class="sxs-lookup"><span data-stu-id="3e085-138">yes</span></span>       |
| [<span data-ttu-id="3e085-139">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3e085-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3e085-140">sim</span><span class="sxs-lookup"><span data-stu-id="3e085-140">yes</span></span>       |
| [<span data-ttu-id="3e085-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3e085-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3e085-142">sim</span><span class="sxs-lookup"><span data-stu-id="3e085-142">yes</span></span>       |
| [<span data-ttu-id="3e085-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e085-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3e085-144">não</span><span class="sxs-lookup"><span data-stu-id="3e085-144">no</span></span>        |
| [<span data-ttu-id="3e085-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e085-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3e085-146">não</span><span class="sxs-lookup"><span data-stu-id="3e085-146">no</span></span>        |
| [<span data-ttu-id="3e085-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e085-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3e085-148">não</span><span class="sxs-lookup"><span data-stu-id="3e085-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3e085-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e085-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e085-150">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e085-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





