---
title: dcl_inputPrimitive (sm4-ASM)
description: DCL \_ inputPrimitive (sm4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916887"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="f08d1-103">DCL \_ inputPrimitive (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f08d1-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="f08d1-104">Declara o tipo primitivo para entradas Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="f08d1-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="f08d1-105">\_ *tipo* de inputPrimitive de DCL</span><span class="sxs-lookup"><span data-stu-id="f08d1-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f08d1-106">Item</span><span class="sxs-lookup"><span data-stu-id="f08d1-106">Item</span></span></th>
<th><span data-ttu-id="f08d1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f08d1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f08d1-108"><span id="type"></span><span id="TYPE"></span><em>Escreva</em></span><span class="sxs-lookup"><span data-stu-id="f08d1-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="f08d1-109">no Tipo primitivo de dados de entrada, que é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f08d1-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="f08d1-110"><em>ponto</em> - lista de pontos</span><span class="sxs-lookup"><span data-stu-id="f08d1-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="f08d1-111"><em>linha</em> - lista de linhas</span><span class="sxs-lookup"><span data-stu-id="f08d1-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="f08d1-112"><em>triângulo</em> - lista de triângulos</span><span class="sxs-lookup"><span data-stu-id="f08d1-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="f08d1-113"><em>line_adj</em> - lista de linhas com dados de adjacência</span><span class="sxs-lookup"><span data-stu-id="f08d1-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="f08d1-114"><em>triangle_adj</em> - lista de triângulos com dados de adjacência</span><span class="sxs-lookup"><span data-stu-id="f08d1-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f08d1-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f08d1-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f08d1-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="f08d1-116">Vertex Shader</span></span> | <span data-ttu-id="f08d1-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="f08d1-117">Geometry Shader</span></span> | <span data-ttu-id="f08d1-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f08d1-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="f08d1-119">x</span><span class="sxs-lookup"><span data-stu-id="f08d1-119">x</span></span>               |              |



 

<span data-ttu-id="f08d1-120">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="f08d1-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="f08d1-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f08d1-121">Example</span></span>

<span data-ttu-id="f08d1-122">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="f08d1-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f08d1-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f08d1-123">Minimum Shader Model</span></span>

<span data-ttu-id="f08d1-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f08d1-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f08d1-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f08d1-125">Shader Model</span></span>                                              | <span data-ttu-id="f08d1-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f08d1-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f08d1-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f08d1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f08d1-128">sim</span><span class="sxs-lookup"><span data-stu-id="f08d1-128">yes</span></span>       |
| [<span data-ttu-id="f08d1-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f08d1-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f08d1-130">sim</span><span class="sxs-lookup"><span data-stu-id="f08d1-130">yes</span></span>       |
| [<span data-ttu-id="f08d1-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f08d1-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f08d1-132">sim</span><span class="sxs-lookup"><span data-stu-id="f08d1-132">yes</span></span>       |
| [<span data-ttu-id="f08d1-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f08d1-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f08d1-134">não</span><span class="sxs-lookup"><span data-stu-id="f08d1-134">no</span></span>        |
| [<span data-ttu-id="f08d1-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f08d1-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f08d1-136">não</span><span class="sxs-lookup"><span data-stu-id="f08d1-136">no</span></span>        |
| [<span data-ttu-id="f08d1-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f08d1-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f08d1-138">não</span><span class="sxs-lookup"><span data-stu-id="f08d1-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f08d1-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f08d1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f08d1-140">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f08d1-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





