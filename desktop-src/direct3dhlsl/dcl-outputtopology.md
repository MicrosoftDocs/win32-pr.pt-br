---
title: dcl_outputTopology (sm4-ASM)
description: DCL \_ outputTopology (sm4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638893"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="c28b6-103">DCL \_ outputTopology (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c28b6-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="c28b6-104">Declara os dados de saída do tipo primitivo Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="c28b6-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="c28b6-105">\_ *tipo* de outputTopology de DCL</span><span class="sxs-lookup"><span data-stu-id="c28b6-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c28b6-106">Item</span><span class="sxs-lookup"><span data-stu-id="c28b6-106">Item</span></span></th>
<th><span data-ttu-id="c28b6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c28b6-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c28b6-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Escreva</em></span><span class="sxs-lookup"><span data-stu-id="c28b6-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="c28b6-109">no Uma topologia primitiva de saída, que é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c28b6-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="c28b6-110"><em>ponto da</em></span><span class="sxs-lookup"><span data-stu-id="c28b6-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="c28b6-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="c28b6-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="c28b6-112"><em>trianglestrip</em></span><span class="sxs-lookup"><span data-stu-id="c28b6-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c28b6-113">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c28b6-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c28b6-114">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c28b6-114">Vertex Shader</span></span> | <span data-ttu-id="c28b6-115">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c28b6-115">Geometry Shader</span></span> | <span data-ttu-id="c28b6-116">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c28b6-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="c28b6-117">x</span><span class="sxs-lookup"><span data-stu-id="c28b6-117">x</span></span>               |              |



 

<span data-ttu-id="c28b6-118">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="c28b6-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c28b6-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c28b6-119">Example</span></span>

<span data-ttu-id="c28b6-120">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="c28b6-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c28b6-121">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c28b6-121">Minimum Shader Model</span></span>

<span data-ttu-id="c28b6-122">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c28b6-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c28b6-123">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c28b6-123">Shader Model</span></span>                                              | <span data-ttu-id="c28b6-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c28b6-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c28b6-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c28b6-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c28b6-126">sim</span><span class="sxs-lookup"><span data-stu-id="c28b6-126">yes</span></span>       |
| [<span data-ttu-id="c28b6-127">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c28b6-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c28b6-128">sim</span><span class="sxs-lookup"><span data-stu-id="c28b6-128">yes</span></span>       |
| [<span data-ttu-id="c28b6-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c28b6-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c28b6-130">sim</span><span class="sxs-lookup"><span data-stu-id="c28b6-130">yes</span></span>       |
| [<span data-ttu-id="c28b6-131">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c28b6-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c28b6-132">não</span><span class="sxs-lookup"><span data-stu-id="c28b6-132">no</span></span>        |
| [<span data-ttu-id="c28b6-133">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c28b6-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c28b6-134">não</span><span class="sxs-lookup"><span data-stu-id="c28b6-134">no</span></span>        |
| [<span data-ttu-id="c28b6-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c28b6-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c28b6-136">não</span><span class="sxs-lookup"><span data-stu-id="c28b6-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c28b6-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c28b6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c28b6-138">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c28b6-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





