---
title: udiv (sm4-ASM)
description: Divisão de inteiro sem sinal.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365229"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="bda90-103">udiv (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bda90-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="bda90-104">Divisão de inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="bda90-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="bda90-105">udiv destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bda90-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="bda90-106">Item</span><span class="sxs-lookup"><span data-stu-id="bda90-106">Item</span></span>                                                                                                   | <span data-ttu-id="bda90-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bda90-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bda90-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span><span class="sxs-lookup"><span data-stu-id="bda90-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="bda90-109">\[no \] endereço do quociente resultante.</span><span class="sxs-lookup"><span data-stu-id="bda90-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="bda90-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span><span class="sxs-lookup"><span data-stu-id="bda90-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="bda90-111">\[no \] endereço do restante resultante.</span><span class="sxs-lookup"><span data-stu-id="bda90-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="bda90-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bda90-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="bda90-113">\[nos \] componentes a serem divididos por *src1*.</span><span class="sxs-lookup"><span data-stu-id="bda90-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="bda90-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bda90-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="bda90-115">\[nos \] componentes de qual para dividir *src0*.</span><span class="sxs-lookup"><span data-stu-id="bda90-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bda90-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bda90-116">Remarks</span></span>

<span data-ttu-id="bda90-117">Essa instrução executa uma divisão não assinada por componente do operando de 32 bits *src0* pelo operando de 32 bits *src1*.</span><span class="sxs-lookup"><span data-stu-id="bda90-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="bda90-118">Os resultados das divisões são os quocientes de 32 bits colocados em *destQUOT* e os restantes de 32 bits colocados em *destREM*.</span><span class="sxs-lookup"><span data-stu-id="bda90-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="bda90-119">A divisão por zero retorna 0xFFFFFFFF para o quociente e o resto.</span><span class="sxs-lookup"><span data-stu-id="bda90-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="bda90-120">Você pode especificar *destQUOT* ou *destREM* como NULL em vez de especificar um registro, se o quociente ou o resto não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="bda90-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="bda90-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bda90-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bda90-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="bda90-122">Vertex Shader</span></span> | <span data-ttu-id="bda90-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="bda90-123">Geometry Shader</span></span> | <span data-ttu-id="bda90-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bda90-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bda90-125">x</span><span class="sxs-lookup"><span data-stu-id="bda90-125">x</span></span>             | <span data-ttu-id="bda90-126">x</span><span class="sxs-lookup"><span data-stu-id="bda90-126">x</span></span>               | <span data-ttu-id="bda90-127">x</span><span class="sxs-lookup"><span data-stu-id="bda90-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bda90-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bda90-128">Minimum Shader Model</span></span>

<span data-ttu-id="bda90-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bda90-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bda90-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bda90-130">Shader Model</span></span>                                              | <span data-ttu-id="bda90-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bda90-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bda90-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bda90-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bda90-133">sim</span><span class="sxs-lookup"><span data-stu-id="bda90-133">yes</span></span>       |
| [<span data-ttu-id="bda90-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bda90-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bda90-135">sim</span><span class="sxs-lookup"><span data-stu-id="bda90-135">yes</span></span>       |
| [<span data-ttu-id="bda90-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bda90-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bda90-137">sim</span><span class="sxs-lookup"><span data-stu-id="bda90-137">yes</span></span>       |
| [<span data-ttu-id="bda90-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda90-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bda90-139">não</span><span class="sxs-lookup"><span data-stu-id="bda90-139">no</span></span>        |
| [<span data-ttu-id="bda90-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda90-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bda90-141">não</span><span class="sxs-lookup"><span data-stu-id="bda90-141">no</span></span>        |
| [<span data-ttu-id="bda90-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda90-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bda90-143">não</span><span class="sxs-lookup"><span data-stu-id="bda90-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bda90-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bda90-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda90-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bda90-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





