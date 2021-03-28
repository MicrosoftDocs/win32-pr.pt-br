---
title: DP3-PS
description: Computa o produto de três componentes do ponto dos registros de origem. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968364"
---
# <a name="dp3---ps"></a><span data-ttu-id="dd64e-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="dd64e-104">dp3 - ps</span></span>

<span data-ttu-id="dd64e-105">Computa o produto de três componentes do ponto dos registros de origem.</span><span class="sxs-lookup"><span data-stu-id="dd64e-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd64e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd64e-106">Syntax</span></span>



| <span data-ttu-id="dd64e-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="dd64e-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="dd64e-108">onde</span><span class="sxs-lookup"><span data-stu-id="dd64e-108">where</span></span>

-   <span data-ttu-id="dd64e-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="dd64e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="dd64e-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="dd64e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="dd64e-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="dd64e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd64e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd64e-112">Remarks</span></span>



| <span data-ttu-id="dd64e-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dd64e-113">Pixel shader versions</span></span> | <span data-ttu-id="dd64e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="dd64e-114">1\_1</span></span> | <span data-ttu-id="dd64e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="dd64e-115">1\_2</span></span> | <span data-ttu-id="dd64e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dd64e-116">1\_3</span></span> | <span data-ttu-id="dd64e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="dd64e-117">1\_4</span></span> | <span data-ttu-id="dd64e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd64e-118">2\_0</span></span> | <span data-ttu-id="dd64e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dd64e-119">2\_x</span></span> | <span data-ttu-id="dd64e-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dd64e-120">2\_sw</span></span> | <span data-ttu-id="dd64e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd64e-121">3\_0</span></span> | <span data-ttu-id="dd64e-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dd64e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="dd64e-123">dp3</span><span class="sxs-lookup"><span data-stu-id="dd64e-123">dp3</span></span>                   | <span data-ttu-id="dd64e-124">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-124">x</span></span>    | <span data-ttu-id="dd64e-125">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-125">x</span></span>    | <span data-ttu-id="dd64e-126">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-126">x</span></span>    | <span data-ttu-id="dd64e-127">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-127">x</span></span>    | <span data-ttu-id="dd64e-128">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-128">x</span></span>    | <span data-ttu-id="dd64e-129">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-129">x</span></span>    | <span data-ttu-id="dd64e-130">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-130">x</span></span>     | <span data-ttu-id="dd64e-131">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-131">x</span></span>    | <span data-ttu-id="dd64e-132">x</span><span class="sxs-lookup"><span data-stu-id="dd64e-132">x</span></span>     |



 

<span data-ttu-id="dd64e-133">O trecho de código a seguir mostra as operações executadas:</span><span class="sxs-lookup"><span data-stu-id="dd64e-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="dd64e-134">Essa instrução é executada no pipeline de vetor, sempre gravando nos canais de cor.</span><span class="sxs-lookup"><span data-stu-id="dd64e-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="dd64e-135">Para a versão 1 \_ 4, essa instrução ainda usa o pipeline de vetor, mas pode gravar em qualquer canal.</span><span class="sxs-lookup"><span data-stu-id="dd64e-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="dd64e-136">Uma instrução com uma máscara de gravação de registro de destino. RGB (. xyz) pode ser emitida em conjunto com DP3, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="dd64e-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="dd64e-137">A instrução DP3 pode ser modificada usando o modificador de argumento de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) aplicado aos seus argumentos de entrada se eles ainda não estiverem expandidos para o intervalo dinâmico assinado.</span><span class="sxs-lookup"><span data-stu-id="dd64e-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="dd64e-138">Para um sombreador de iluminação, o modificador de instrução saturação ( \_ SAT) é geralmente usado para fixe os valores negativos para preto, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd64e-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="dd64e-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd64e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd64e-140">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dd64e-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




