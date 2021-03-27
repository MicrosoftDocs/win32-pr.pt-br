---
title: dcl_constantBuffer (sm4-ASM)
description: DCL \_ constantBuffer (sm4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084269"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="c2dfb-103">DCL \_ constantBuffer (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="c2dfb-104">Declara um buffer de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="c2dfb-105">DCL \_ constantBuffer *cbN \[ tamanho \]*, *AccessPattern*</span><span class="sxs-lookup"><span data-stu-id="c2dfb-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2dfb-106">Item</span><span class="sxs-lookup"><span data-stu-id="c2dfb-106">Item</span></span></th>
<th><span data-ttu-id="c2dfb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2dfb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2dfb-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [tamanho]</em></span><span class="sxs-lookup"><span data-stu-id="c2dfb-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="c2dfb-109">no Um buffer de constante de sombreador em que N é um inteiro que denota que o número e o tamanho do registro de buffer constante é um inteiro que denota o número de elementos no buffer.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dfb-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span><span class="sxs-lookup"><span data-stu-id="c2dfb-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="c2dfb-111">no A maneira como o buffer será acessado pelo código do sombreador, que é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c2dfb-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c2dfb-112">Name</span><span class="sxs-lookup"><span data-stu-id="c2dfb-112">Name</span></span></th>
<th><span data-ttu-id="c2dfb-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2dfb-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2dfb-114">immediateIndexed</span><span class="sxs-lookup"><span data-stu-id="c2dfb-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="c2dfb-115">Indexe o buffer com um valor literal.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dfb-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="c2dfb-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="c2dfb-117">Indexe o buffer com o resultado de uma expressão avaliada.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c2dfb-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c2dfb-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c2dfb-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c2dfb-119">Vertex Shader</span></span> | <span data-ttu-id="c2dfb-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c2dfb-120">Geometry Shader</span></span> | <span data-ttu-id="c2dfb-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c2dfb-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c2dfb-122">x</span><span class="sxs-lookup"><span data-stu-id="c2dfb-122">x</span></span>             | <span data-ttu-id="c2dfb-123">x</span><span class="sxs-lookup"><span data-stu-id="c2dfb-123">x</span></span>               | <span data-ttu-id="c2dfb-124">x</span><span class="sxs-lookup"><span data-stu-id="c2dfb-124">x</span></span>            |



 

<span data-ttu-id="c2dfb-125">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c2dfb-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c2dfb-126">Example</span></span>

<span data-ttu-id="c2dfb-127">Este exemplo declara um buffer constante para registrar cB0, que tem 19 elementos.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="c2dfb-128">Esses elementos são acessados com um índice literal.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c2dfb-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c2dfb-129">Minimum Shader Model</span></span>

<span data-ttu-id="c2dfb-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c2dfb-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c2dfb-131">Shader Model</span></span>                                              | <span data-ttu-id="c2dfb-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c2dfb-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c2dfb-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c2dfb-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c2dfb-134">sim</span><span class="sxs-lookup"><span data-stu-id="c2dfb-134">yes</span></span>       |
| [<span data-ttu-id="c2dfb-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c2dfb-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c2dfb-136">sim</span><span class="sxs-lookup"><span data-stu-id="c2dfb-136">yes</span></span>       |
| [<span data-ttu-id="c2dfb-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c2dfb-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2dfb-138">sim</span><span class="sxs-lookup"><span data-stu-id="c2dfb-138">yes</span></span>       |
| [<span data-ttu-id="c2dfb-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2dfb-140">não</span><span class="sxs-lookup"><span data-stu-id="c2dfb-140">no</span></span>        |
| [<span data-ttu-id="c2dfb-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2dfb-142">não</span><span class="sxs-lookup"><span data-stu-id="c2dfb-142">no</span></span>        |
| [<span data-ttu-id="c2dfb-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2dfb-144">não</span><span class="sxs-lookup"><span data-stu-id="c2dfb-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c2dfb-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2dfb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2dfb-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





