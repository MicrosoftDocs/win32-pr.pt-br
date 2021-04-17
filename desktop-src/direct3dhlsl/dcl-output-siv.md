---
title: dcl_output_siv (sm4-ASM)
description: '\_ \_ SIV de saída DCL (sm4-ASM)'
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988617"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="1b02d-103">\_ \_ SIV de saída DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b02d-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="1b02d-104">Declara um registro de saída que contém um parâmetro [de valor do sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="1b02d-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="1b02d-105">DCL \_ \_ de saída SIV em \[ *. máscaras* \] , *systemvalue*</span><span class="sxs-lookup"><span data-stu-id="1b02d-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="1b02d-106">Item</span><span class="sxs-lookup"><span data-stu-id="1b02d-106">Item</span></span>                                                                                                                               | <span data-ttu-id="1b02d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b02d-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b02d-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="1b02d-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="1b02d-109">\[em \] um registro de dados de saída; *N* é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="1b02d-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="1b02d-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="1b02d-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="1b02d-111">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="1b02d-111">\[in\] Optional.</span></span> <span data-ttu-id="1b02d-112">Uma máscara de componente (. xyzw) que especifica qual dos componentes de registro usar.</span><span class="sxs-lookup"><span data-stu-id="1b02d-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="1b02d-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="1b02d-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="1b02d-114">\[no \] nome do valor do sistema, que é uma cadeia de caracteres (consulte a [semântica do valor do sistema](dx-graphics-hlsl-semantics.md)) sem o prefixo "VA \_ ".</span><span class="sxs-lookup"><span data-stu-id="1b02d-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="1b02d-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1b02d-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b02d-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1b02d-116">Vertex Shader</span></span> | <span data-ttu-id="1b02d-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1b02d-117">Geometry Shader</span></span> | <span data-ttu-id="1b02d-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1b02d-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1b02d-119">x</span><span class="sxs-lookup"><span data-stu-id="1b02d-119">x</span></span>             | <span data-ttu-id="1b02d-120">x</span><span class="sxs-lookup"><span data-stu-id="1b02d-120">x</span></span>               |              |



 

<span data-ttu-id="1b02d-121">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="1b02d-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="1b02d-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1b02d-122">Example</span></span>

<span data-ttu-id="1b02d-123">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="1b02d-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="1b02d-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1b02d-124">Minimum Shader Model</span></span>

<span data-ttu-id="1b02d-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1b02d-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1b02d-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1b02d-126">Shader Model</span></span>                                              | <span data-ttu-id="1b02d-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1b02d-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b02d-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1b02d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b02d-129">sim</span><span class="sxs-lookup"><span data-stu-id="1b02d-129">yes</span></span>       |
| [<span data-ttu-id="1b02d-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1b02d-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b02d-131">sim</span><span class="sxs-lookup"><span data-stu-id="1b02d-131">yes</span></span>       |
| [<span data-ttu-id="1b02d-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1b02d-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b02d-133">sim</span><span class="sxs-lookup"><span data-stu-id="1b02d-133">yes</span></span>       |
| [<span data-ttu-id="1b02d-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b02d-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b02d-135">não</span><span class="sxs-lookup"><span data-stu-id="1b02d-135">no</span></span>        |
| [<span data-ttu-id="1b02d-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b02d-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b02d-137">não</span><span class="sxs-lookup"><span data-stu-id="1b02d-137">no</span></span>        |
| [<span data-ttu-id="1b02d-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b02d-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b02d-139">não</span><span class="sxs-lookup"><span data-stu-id="1b02d-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b02d-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b02d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b02d-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b02d-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





