---
title: dcl_indexableTemp (sm4-ASM)
description: DCL \_ indexableTemp (sm4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988623"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="c97d5-103">DCL \_ indexableTemp (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c97d5-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="c97d5-104">Declara um registro temporário indexável.</span><span class="sxs-lookup"><span data-stu-id="c97d5-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="c97d5-105">DCL \_ indexableTemp x *N \[ tamanho \] , ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="c97d5-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="c97d5-106">Item</span><span class="sxs-lookup"><span data-stu-id="c97d5-106">Item</span></span>                                                                                                                           | <span data-ttu-id="c97d5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c97d5-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d5-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="c97d5-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="c97d5-109">\[em \] um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="c97d5-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="c97d5-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[tamanho\]*</span><span class="sxs-lookup"><span data-stu-id="c97d5-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="c97d5-111">\[em \] um valor inteiro opcional.</span><span class="sxs-lookup"><span data-stu-id="c97d5-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="c97d5-112">O número de elementos na matriz de registro.</span><span class="sxs-lookup"><span data-stu-id="c97d5-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="c97d5-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="c97d5-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="c97d5-114">\[em \] um valor inteiro opcional. O número de componentes na matriz de registro.</span><span class="sxs-lookup"><span data-stu-id="c97d5-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="c97d5-115">Um registro contém espaço suficiente para um valor de quatro componentes de 32 bits; o número de elementos na matriz de registros temporários (indexável e [não indexável](dcl-temps.md)) não pode exceder 4096.</span><span class="sxs-lookup"><span data-stu-id="c97d5-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="c97d5-116">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c97d5-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c97d5-117">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c97d5-117">Vertex Shader</span></span> | <span data-ttu-id="c97d5-118">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c97d5-118">Geometry Shader</span></span> | <span data-ttu-id="c97d5-119">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c97d5-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c97d5-120">x</span><span class="sxs-lookup"><span data-stu-id="c97d5-120">x</span></span>             | <span data-ttu-id="c97d5-121">x</span><span class="sxs-lookup"><span data-stu-id="c97d5-121">x</span></span>               | <span data-ttu-id="c97d5-122">x</span><span class="sxs-lookup"><span data-stu-id="c97d5-122">x</span></span>            |



 

<span data-ttu-id="c97d5-123">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="c97d5-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c97d5-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c97d5-124">Example</span></span>

<span data-ttu-id="c97d5-125">Aqui estão alguns exemplos do código gerado para registros indexáveis.</span><span class="sxs-lookup"><span data-stu-id="c97d5-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c97d5-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c97d5-126">Minimum Shader Model</span></span>

<span data-ttu-id="c97d5-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c97d5-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c97d5-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c97d5-128">Shader Model</span></span>                                              | <span data-ttu-id="c97d5-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c97d5-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c97d5-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c97d5-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c97d5-131">sim</span><span class="sxs-lookup"><span data-stu-id="c97d5-131">yes</span></span>       |
| [<span data-ttu-id="c97d5-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c97d5-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c97d5-133">sim</span><span class="sxs-lookup"><span data-stu-id="c97d5-133">yes</span></span>       |
| [<span data-ttu-id="c97d5-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c97d5-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c97d5-135">sim</span><span class="sxs-lookup"><span data-stu-id="c97d5-135">yes</span></span>       |
| [<span data-ttu-id="c97d5-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97d5-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c97d5-137">não</span><span class="sxs-lookup"><span data-stu-id="c97d5-137">no</span></span>        |
| [<span data-ttu-id="c97d5-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97d5-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c97d5-139">não</span><span class="sxs-lookup"><span data-stu-id="c97d5-139">no</span></span>        |
| [<span data-ttu-id="c97d5-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97d5-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c97d5-141">não</span><span class="sxs-lookup"><span data-stu-id="c97d5-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c97d5-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c97d5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c97d5-143">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97d5-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





