---
title: dcl_output oMask (SM5-ASM)
description: Declare um registro de saída para ser gravado pelo sombreador.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365290"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="cb0c0-103">\_oMask de saída DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cb0c0-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="cb0c0-104">Declare um registro de saída para ser gravado pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="cb0c0-105">DCL \_ saída o \# \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="cb0c0-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="cb0c0-106">Item</span><span class="sxs-lookup"><span data-stu-id="cb0c0-106">Item</span></span>                                                   | <span data-ttu-id="cb0c0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb0c0-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="cb0c0-108"><span id="o"></span><span id="O"></span>*minúscula*</span><span class="sxs-lookup"><span data-stu-id="cb0c0-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="cb0c0-109">\[no \] registro de saída.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb0c0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb0c0-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="cb0c0-111">Restrições</span><span class="sxs-lookup"><span data-stu-id="cb0c0-111">Restrictions</span></span>

-   <span data-ttu-id="cb0c0-112">A máscara de componente pode ser qualquer subconjunto de \[ xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="cb0c0-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="cb0c0-113">No entanto, deixar as lacunas entre os componentes desperdiça espaço.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="cb0c0-114">É legal declarar um superconjunto da máscara do componente declarado para entrada pelo próximo estágio.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="cb0c0-115">No entanto, as máscaras mutuamente exclusivas não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="cb0c0-116">O sombreador de vértice gerando O3. XY, significa que o sombreador de pixel inserindo v3. z é inválido, mas inserindo v3. x ou v3. y ou v3. XY é válido.</span><span class="sxs-lookup"><span data-stu-id="cb0c0-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="cb0c0-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cb0c0-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cb0c0-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="cb0c0-118">Vertex</span></span> | <span data-ttu-id="cb0c0-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="cb0c0-119">Hull</span></span> | <span data-ttu-id="cb0c0-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="cb0c0-120">Domain</span></span> | <span data-ttu-id="cb0c0-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="cb0c0-121">Geometry</span></span> | <span data-ttu-id="cb0c0-122">16x16</span><span class="sxs-lookup"><span data-stu-id="cb0c0-122">Pixel</span></span> | <span data-ttu-id="cb0c0-123">Computação</span><span class="sxs-lookup"><span data-stu-id="cb0c0-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cb0c0-124">X</span><span class="sxs-lookup"><span data-stu-id="cb0c0-124">X</span></span>      | <span data-ttu-id="cb0c0-125">X</span><span class="sxs-lookup"><span data-stu-id="cb0c0-125">X</span></span>    | <span data-ttu-id="cb0c0-126">X</span><span class="sxs-lookup"><span data-stu-id="cb0c0-126">X</span></span>      | <span data-ttu-id="cb0c0-127">X</span><span class="sxs-lookup"><span data-stu-id="cb0c0-127">X</span></span>        | <span data-ttu-id="cb0c0-128">X</span><span class="sxs-lookup"><span data-stu-id="cb0c0-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cb0c0-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="cb0c0-129">Minimum Shader Model</span></span>

<span data-ttu-id="cb0c0-130">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cb0c0-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cb0c0-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cb0c0-131">Shader Model</span></span>                                              | <span data-ttu-id="cb0c0-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cb0c0-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cb0c0-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cb0c0-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cb0c0-134">sim</span><span class="sxs-lookup"><span data-stu-id="cb0c0-134">yes</span></span>       |
| [<span data-ttu-id="cb0c0-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cb0c0-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cb0c0-136">não</span><span class="sxs-lookup"><span data-stu-id="cb0c0-136">no</span></span>        |
| [<span data-ttu-id="cb0c0-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cb0c0-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cb0c0-138">não</span><span class="sxs-lookup"><span data-stu-id="cb0c0-138">no</span></span>        |
| [<span data-ttu-id="cb0c0-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb0c0-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cb0c0-140">não</span><span class="sxs-lookup"><span data-stu-id="cb0c0-140">no</span></span>        |
| [<span data-ttu-id="cb0c0-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb0c0-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cb0c0-142">não</span><span class="sxs-lookup"><span data-stu-id="cb0c0-142">no</span></span>        |
| [<span data-ttu-id="cb0c0-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb0c0-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cb0c0-144">não</span><span class="sxs-lookup"><span data-stu-id="cb0c0-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cb0c0-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb0c0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb0c0-146">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb0c0-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





