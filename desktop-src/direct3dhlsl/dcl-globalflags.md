---
title: dcl_globalFlags (sm4-ASM)
description: DCL \_ globalFlags (sm4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365297"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="9993f-103">DCL \_ globalFlags (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9993f-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="9993f-104">Declara os sinalizadores globais do sombreador.</span><span class="sxs-lookup"><span data-stu-id="9993f-104">Declares shader global flags.</span></span>



| <span data-ttu-id="9993f-105">\_ *sinalizadores* de globalFlags de DCL</span><span class="sxs-lookup"><span data-stu-id="9993f-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="9993f-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span><span class="sxs-lookup"><span data-stu-id="9993f-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="9993f-107">\[em \] um sinalizador de sombreador global.</span><span class="sxs-lookup"><span data-stu-id="9993f-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="9993f-108">Atualmente, há um sinalizador definido.</span><span class="sxs-lookup"><span data-stu-id="9993f-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="9993f-109">Refatoração \_ permitida – permite que o driver reordene operações aritméticas para otimização, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="9993f-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="9993f-110">Reordenar operações aritméticas pode gerar resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="9993f-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9993f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9993f-111">Remarks</span></span>

<span data-ttu-id="9993f-112">Essa instrução opcional se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9993f-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9993f-113">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="9993f-113">Vertex Shader</span></span> | <span data-ttu-id="9993f-114">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="9993f-114">Geometry Shader</span></span> | <span data-ttu-id="9993f-115">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9993f-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9993f-116">x</span><span class="sxs-lookup"><span data-stu-id="9993f-116">x</span></span>             | <span data-ttu-id="9993f-117">x</span><span class="sxs-lookup"><span data-stu-id="9993f-117">x</span></span>               | <span data-ttu-id="9993f-118">x</span><span class="sxs-lookup"><span data-stu-id="9993f-118">x</span></span>            |



 

<span data-ttu-id="9993f-119">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="9993f-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9993f-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9993f-120">Minimum Shader Model</span></span>

<span data-ttu-id="9993f-121">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9993f-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9993f-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9993f-122">Shader Model</span></span>                                              | <span data-ttu-id="9993f-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9993f-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9993f-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9993f-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9993f-125">sim</span><span class="sxs-lookup"><span data-stu-id="9993f-125">yes</span></span>       |
| [<span data-ttu-id="9993f-126">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9993f-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9993f-127">sim</span><span class="sxs-lookup"><span data-stu-id="9993f-127">yes</span></span>       |
| [<span data-ttu-id="9993f-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9993f-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9993f-129">sim</span><span class="sxs-lookup"><span data-stu-id="9993f-129">yes</span></span>       |
| [<span data-ttu-id="9993f-130">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9993f-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9993f-131">não</span><span class="sxs-lookup"><span data-stu-id="9993f-131">no</span></span>        |
| [<span data-ttu-id="9993f-132">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9993f-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9993f-133">não</span><span class="sxs-lookup"><span data-stu-id="9993f-133">no</span></span>        |
| [<span data-ttu-id="9993f-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9993f-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9993f-135">não</span><span class="sxs-lookup"><span data-stu-id="9993f-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9993f-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9993f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9993f-137">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9993f-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




