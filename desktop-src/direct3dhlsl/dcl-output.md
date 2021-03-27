---
title: dcl_output (sm4-ASM)
description: '\_saída de DCL (sm4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967135"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="4ad91-103">\_saída de DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4ad91-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="4ad91-104">Declara um registro de sombreador-saída.</span><span class="sxs-lookup"><span data-stu-id="4ad91-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="4ad91-105">DCL \_ saída o *N \[ . Mask \]*</span><span class="sxs-lookup"><span data-stu-id="4ad91-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="4ad91-106">Item</span><span class="sxs-lookup"><span data-stu-id="4ad91-106">Item</span></span>                                                                           | <span data-ttu-id="4ad91-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ad91-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad91-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="4ad91-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="4ad91-109">\[em \] um registro de dados de saída; *N* é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="4ad91-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="4ad91-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="4ad91-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="4ad91-111">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="4ad91-111">\[in\] Optional.</span></span> <span data-ttu-id="4ad91-112">Uma máscara de componente (. xyzw) que especifica qual dos componentes de registro usar.</span><span class="sxs-lookup"><span data-stu-id="4ad91-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="4ad91-113">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4ad91-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4ad91-114">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4ad91-114">Vertex Shader</span></span> | <span data-ttu-id="4ad91-115">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="4ad91-115">Geometry Shader</span></span> | <span data-ttu-id="4ad91-116">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4ad91-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4ad91-117">x</span><span class="sxs-lookup"><span data-stu-id="4ad91-117">x</span></span>             | <span data-ttu-id="4ad91-118">x</span><span class="sxs-lookup"><span data-stu-id="4ad91-118">x</span></span>               | <span data-ttu-id="4ad91-119">x</span><span class="sxs-lookup"><span data-stu-id="4ad91-119">x</span></span>            |



 

<span data-ttu-id="4ad91-120">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4ad91-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4ad91-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4ad91-121">Example</span></span>

<span data-ttu-id="4ad91-122">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="4ad91-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4ad91-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4ad91-123">Minimum Shader Model</span></span>

<span data-ttu-id="4ad91-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4ad91-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4ad91-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4ad91-125">Shader Model</span></span>                                              | <span data-ttu-id="4ad91-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4ad91-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4ad91-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4ad91-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4ad91-128">sim</span><span class="sxs-lookup"><span data-stu-id="4ad91-128">yes</span></span>       |
| [<span data-ttu-id="4ad91-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4ad91-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4ad91-130">sim</span><span class="sxs-lookup"><span data-stu-id="4ad91-130">yes</span></span>       |
| [<span data-ttu-id="4ad91-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4ad91-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4ad91-132">sim</span><span class="sxs-lookup"><span data-stu-id="4ad91-132">yes</span></span>       |
| [<span data-ttu-id="4ad91-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ad91-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4ad91-134">não</span><span class="sxs-lookup"><span data-stu-id="4ad91-134">no</span></span>        |
| [<span data-ttu-id="4ad91-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ad91-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4ad91-136">não</span><span class="sxs-lookup"><span data-stu-id="4ad91-136">no</span></span>        |
| [<span data-ttu-id="4ad91-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ad91-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4ad91-138">não</span><span class="sxs-lookup"><span data-stu-id="4ad91-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4ad91-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ad91-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ad91-140">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ad91-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





