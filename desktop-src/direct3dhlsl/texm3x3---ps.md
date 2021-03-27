---
title: texm3x3-PS
description: Executa uma matriz 3x3 multiplicada quando usada em conjunto com duas instruções texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967101"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="5df7c-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="5df7c-103">texm3x3 - ps</span></span>

<span data-ttu-id="5df7c-104">Executa uma matriz 3x3 multiplicada quando usada em conjunto com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="5df7c-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df7c-105">Syntax</span></span>



| <span data-ttu-id="5df7c-106">texm3x3 DST, src</span><span class="sxs-lookup"><span data-stu-id="5df7c-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="5df7c-107">onde</span><span class="sxs-lookup"><span data-stu-id="5df7c-107">where</span></span>

-   <span data-ttu-id="5df7c-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5df7c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="5df7c-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5df7c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df7c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5df7c-110">Remarks</span></span>



| <span data-ttu-id="5df7c-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5df7c-111">Pixel shader versions</span></span> | <span data-ttu-id="5df7c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5df7c-112">1\_1</span></span> | <span data-ttu-id="5df7c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="5df7c-113">1\_2</span></span> | <span data-ttu-id="5df7c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5df7c-114">1\_3</span></span> | <span data-ttu-id="5df7c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="5df7c-115">1\_4</span></span> | <span data-ttu-id="5df7c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5df7c-116">2\_0</span></span> | <span data-ttu-id="5df7c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5df7c-117">2\_x</span></span> | <span data-ttu-id="5df7c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5df7c-118">2\_sw</span></span> | <span data-ttu-id="5df7c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5df7c-119">3\_0</span></span> | <span data-ttu-id="5df7c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5df7c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5df7c-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="5df7c-121">texm3x3</span></span>               |      | <span data-ttu-id="5df7c-122">x</span><span class="sxs-lookup"><span data-stu-id="5df7c-122">x</span></span>    | <span data-ttu-id="5df7c-123">x</span><span class="sxs-lookup"><span data-stu-id="5df7c-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="5df7c-124">Essa instrução é a mesma que a instrução [texm3x3tex-PS](texm3x3tex---ps.md) , sem a pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="5df7c-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="5df7c-125">Essa instrução é usada como a última das três instruções que representam uma operação de multiplicação de matriz 3x3.</span><span class="sxs-lookup"><span data-stu-id="5df7c-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="5df7c-126">A matriz 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e pelos dois estágios de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="5df7c-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="5df7c-127">Qualquer textura atribuída a qualquer um dos três estágios de textura é ignorada.</span><span class="sxs-lookup"><span data-stu-id="5df7c-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="5df7c-128">Essa instrução deve ser usada com duas instruções texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="5df7c-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="5df7c-129">Os registros de textura devem seguir a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="5df7c-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="5df7c-130">Veja mais detalhes sobre como a multiplicação de 3x3 é realizada.</span><span class="sxs-lookup"><span data-stu-id="5df7c-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="5df7c-131">A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="5df7c-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="5df7c-132">u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="5df7c-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="5df7c-133">A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="5df7c-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="5df7c-134">v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="5df7c-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="5df7c-135">A instrução texm3x3tex executa a terceira linha da multiplicação para localizar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="5df7c-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="5df7c-136">w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="5df7c-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="5df7c-137">Coloque o resultado da matriz multiplique no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5df7c-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="5df7c-138">t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span><span class="sxs-lookup"><span data-stu-id="5df7c-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5df7c-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5df7c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df7c-140">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5df7c-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




