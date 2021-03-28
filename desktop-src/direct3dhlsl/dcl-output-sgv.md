---
title: dcl_output_sgv (sm4-ASM)
description: '\_ \_ SGV de saída DCL (sm4-ASM)'
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365289"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="8489f-103">\_ \_ SGV de saída DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8489f-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="8489f-104">Declara um registro de saída que contém um parâmetro [de valor do sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="8489f-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="8489f-105">\_ \_ SGV de saída de DCL em *\[ \] . Mask*, *sistema*</span><span class="sxs-lookup"><span data-stu-id="8489f-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="8489f-106">Item</span><span class="sxs-lookup"><span data-stu-id="8489f-106">Item</span></span>                                                                                                                               | <span data-ttu-id="8489f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8489f-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8489f-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="8489f-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="8489f-109">\[em \] um registro de dados de saída; *N* é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="8489f-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="8489f-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="8489f-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="8489f-111">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="8489f-111">\[in\] Optional.</span></span> <span data-ttu-id="8489f-112">Uma máscara de componente (. xyzw) que especifica qual dos componentes de registro usar.</span><span class="sxs-lookup"><span data-stu-id="8489f-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="8489f-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="8489f-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="8489f-114">\[no \] nome do valor do sistema, que é uma cadeia de caracteres (consulte a [semântica do valor do sistema](dx-graphics-hlsl-semantics.md)) sem o prefixo "VA \_ ".</span><span class="sxs-lookup"><span data-stu-id="8489f-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="8489f-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8489f-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8489f-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8489f-116">Vertex Shader</span></span> | <span data-ttu-id="8489f-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8489f-117">Geometry Shader</span></span> | <span data-ttu-id="8489f-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8489f-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="8489f-119">x</span><span class="sxs-lookup"><span data-stu-id="8489f-119">x</span></span>               |              |



 

<span data-ttu-id="8489f-120">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="8489f-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="8489f-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8489f-121">Example</span></span>

<span data-ttu-id="8489f-122">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="8489f-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8489f-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8489f-123">Minimum Shader Model</span></span>

<span data-ttu-id="8489f-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8489f-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8489f-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8489f-125">Shader Model</span></span>                                              | <span data-ttu-id="8489f-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8489f-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8489f-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8489f-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8489f-128">sim</span><span class="sxs-lookup"><span data-stu-id="8489f-128">yes</span></span>       |
| [<span data-ttu-id="8489f-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8489f-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8489f-130">sim</span><span class="sxs-lookup"><span data-stu-id="8489f-130">yes</span></span>       |
| [<span data-ttu-id="8489f-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8489f-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8489f-132">sim</span><span class="sxs-lookup"><span data-stu-id="8489f-132">yes</span></span>       |
| [<span data-ttu-id="8489f-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8489f-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8489f-134">não</span><span class="sxs-lookup"><span data-stu-id="8489f-134">no</span></span>        |
| [<span data-ttu-id="8489f-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8489f-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8489f-136">não</span><span class="sxs-lookup"><span data-stu-id="8489f-136">no</span></span>        |
| [<span data-ttu-id="8489f-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8489f-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8489f-138">não</span><span class="sxs-lookup"><span data-stu-id="8489f-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8489f-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8489f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8489f-140">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8489f-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





