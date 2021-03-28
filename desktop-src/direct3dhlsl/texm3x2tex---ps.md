---
title: texm3x2tex-PS
description: Executa a linha final de uma multiplicação de matriz 3x2 e usa o resultado para fazer uma pesquisa de textura. texm3x2tex deve ser usado em conjunto com a instrução texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988586"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="0d8d6-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="0d8d6-104">texm3x2tex - ps</span></span>

<span data-ttu-id="0d8d6-105">Executa a linha final de uma multiplicação de matriz 3x2 e usa o resultado para fazer uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="0d8d6-106">texm3x2tex deve ser usado em conjunto com a instrução [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0d8d6-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d8d6-107">Syntax</span></span>



| <span data-ttu-id="0d8d6-108">texm3x2tex DST, src</span><span class="sxs-lookup"><span data-stu-id="0d8d6-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="0d8d6-109">onde</span><span class="sxs-lookup"><span data-stu-id="0d8d6-109">where</span></span>

-   <span data-ttu-id="0d8d6-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-110">dst is the destination register.</span></span>
-   <span data-ttu-id="0d8d6-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8d6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d8d6-112">Remarks</span></span>



| <span data-ttu-id="0d8d6-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0d8d6-113">Pixel shader versions</span></span> | <span data-ttu-id="0d8d6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0d8d6-114">1\_1</span></span> | <span data-ttu-id="0d8d6-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0d8d6-115">1\_2</span></span> | <span data-ttu-id="0d8d6-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0d8d6-116">1\_3</span></span> | <span data-ttu-id="0d8d6-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0d8d6-117">1\_4</span></span> | <span data-ttu-id="0d8d6-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d8d6-118">2\_0</span></span> | <span data-ttu-id="0d8d6-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0d8d6-119">2\_x</span></span> | <span data-ttu-id="0d8d6-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d8d6-120">2\_sw</span></span> | <span data-ttu-id="0d8d6-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d8d6-121">3\_0</span></span> | <span data-ttu-id="0d8d6-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d8d6-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0d8d6-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="0d8d6-123">texm3x2tex</span></span>            | <span data-ttu-id="0d8d6-124">x</span><span class="sxs-lookup"><span data-stu-id="0d8d6-124">x</span></span>    | <span data-ttu-id="0d8d6-125">x</span><span class="sxs-lookup"><span data-stu-id="0d8d6-125">x</span></span>    | <span data-ttu-id="0d8d6-126">x</span><span class="sxs-lookup"><span data-stu-id="0d8d6-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0d8d6-127">A instrução é usada como uma das duas instruções que representam uma operação de multiplicação de matriz 3x2.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="0d8d6-128">Essa instrução deve ser usada com a instrução [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0d8d6-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="0d8d6-129">Ao usar essas duas instruções, os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="0d8d6-130">Veja mais detalhes sobre como a multiplicação de 3x2 é realizada.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="0d8d6-131">A instrução texm3x2pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="0d8d6-132">u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (estágio m)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="0d8d6-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="0d8d6-133">A instrução texm3x2tex executa a segunda linha da multiplicação para localizar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="0d8d6-134">v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (estágio m + 1)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="0d8d6-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="0d8d6-135">A instrução texm3x2tex amostra a textura no estágio (m + 1) com (u<sup>'</sup>, v<sup>'</sup>) e armazena o resultado em t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="0d8d6-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="0d8d6-136">t (m + 1)<sub>RGB</sub> = TextureSample (estágio m + 1)<sub>RGB</sub> usando (u<sup>'</sup>, v<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="0d8d6-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="0d8d6-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d8d6-137">Examples</span></span>

<span data-ttu-id="0d8d6-138">Aqui está um sombreador de exemplo com os mapas de textura e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="0d8d6-139">Este exemplo requer as seguintes texturas nos seguintes estágios de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="0d8d6-140">O estágio 0 usa um mapa com dados de muito (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="0d8d6-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="0d8d6-141">O estágio 1 contém coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="0d8d6-142">Nenhuma textura é necessária no estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="0d8d6-143">O estágio 2 mantém as coordenadas de textura, bem como uma textura 2D definida nesse estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d8d6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d8d6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d8d6-145">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0d8d6-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




