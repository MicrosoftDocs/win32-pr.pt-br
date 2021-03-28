---
title: dcl_temps (sm4-ASM)
description: '\_pretemps DCL (sm4-ASM)'
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988613"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="e2129-103">\_pretemps DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e2129-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="e2129-104">Declara registros temporários.</span><span class="sxs-lookup"><span data-stu-id="e2129-104">Declares temporary registers.</span></span>



| <span data-ttu-id="e2129-105">pretemps de DCL \_ N</span><span class="sxs-lookup"><span data-stu-id="e2129-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="e2129-106">Item</span><span class="sxs-lookup"><span data-stu-id="e2129-106">Item</span></span>                                                   | <span data-ttu-id="e2129-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2129-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2129-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="e2129-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="e2129-109">\[no \] número de registros temporários.</span><span class="sxs-lookup"><span data-stu-id="e2129-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="e2129-110">Cada registrador tem espaço para um valor de quatro componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e2129-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="e2129-111">O número total de registros temporários e [indexáveis](dcl-indexabletemp.md) temporários deve ser menor ou igual a 4096.</span><span class="sxs-lookup"><span data-stu-id="e2129-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="e2129-112">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e2129-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e2129-113">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e2129-113">Vertex Shader</span></span> | <span data-ttu-id="e2129-114">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="e2129-114">Geometry Shader</span></span> | <span data-ttu-id="e2129-115">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e2129-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e2129-116">x</span><span class="sxs-lookup"><span data-stu-id="e2129-116">x</span></span>             | <span data-ttu-id="e2129-117">x</span><span class="sxs-lookup"><span data-stu-id="e2129-117">x</span></span>               | <span data-ttu-id="e2129-118">x</span><span class="sxs-lookup"><span data-stu-id="e2129-118">x</span></span>            |



 

<span data-ttu-id="e2129-119">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="e2129-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="e2129-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e2129-120">Example</span></span>

<span data-ttu-id="e2129-121">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="e2129-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e2129-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e2129-122">Minimum Shader Model</span></span>

<span data-ttu-id="e2129-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e2129-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e2129-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e2129-124">Shader Model</span></span>                                              | <span data-ttu-id="e2129-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e2129-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e2129-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e2129-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e2129-127">sim</span><span class="sxs-lookup"><span data-stu-id="e2129-127">yes</span></span>       |
| [<span data-ttu-id="e2129-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e2129-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e2129-129">sim</span><span class="sxs-lookup"><span data-stu-id="e2129-129">yes</span></span>       |
| [<span data-ttu-id="e2129-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e2129-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e2129-131">sim</span><span class="sxs-lookup"><span data-stu-id="e2129-131">yes</span></span>       |
| [<span data-ttu-id="e2129-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2129-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e2129-133">não</span><span class="sxs-lookup"><span data-stu-id="e2129-133">no</span></span>        |
| [<span data-ttu-id="e2129-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2129-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e2129-135">não</span><span class="sxs-lookup"><span data-stu-id="e2129-135">no</span></span>        |
| [<span data-ttu-id="e2129-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2129-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e2129-137">não</span><span class="sxs-lookup"><span data-stu-id="e2129-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e2129-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2129-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2129-139">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2129-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





