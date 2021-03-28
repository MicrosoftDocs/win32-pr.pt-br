---
title: texm3x3tex-PS
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma pesquisa de textura. texm3x3tex deve ser usado com duas instruções texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365303"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="aa64c-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="aa64c-104">texm3x3tex - ps</span></span>

<span data-ttu-id="aa64c-105">Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="aa64c-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="aa64c-106">texm3x3tex deve ser usado com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="aa64c-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa64c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa64c-107">Syntax</span></span>



| <span data-ttu-id="aa64c-108">texm3x3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="aa64c-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="aa64c-109">onde</span><span class="sxs-lookup"><span data-stu-id="aa64c-109">where</span></span>

-   <span data-ttu-id="aa64c-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="aa64c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="aa64c-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="aa64c-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa64c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa64c-112">Remarks</span></span>



| <span data-ttu-id="aa64c-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="aa64c-113">Pixel shader versions</span></span> | <span data-ttu-id="aa64c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="aa64c-114">1\_1</span></span> | <span data-ttu-id="aa64c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="aa64c-115">1\_2</span></span> | <span data-ttu-id="aa64c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aa64c-116">1\_3</span></span> | <span data-ttu-id="aa64c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="aa64c-117">1\_4</span></span> | <span data-ttu-id="aa64c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa64c-118">2\_0</span></span> | <span data-ttu-id="aa64c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aa64c-119">2\_x</span></span> | <span data-ttu-id="aa64c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa64c-120">2\_sw</span></span> | <span data-ttu-id="aa64c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa64c-121">3\_0</span></span> | <span data-ttu-id="aa64c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa64c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aa64c-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="aa64c-123">texm3x3tex</span></span>            | <span data-ttu-id="aa64c-124">x</span><span class="sxs-lookup"><span data-stu-id="aa64c-124">x</span></span>    | <span data-ttu-id="aa64c-125">x</span><span class="sxs-lookup"><span data-stu-id="aa64c-125">x</span></span>    | <span data-ttu-id="aa64c-126">x</span><span class="sxs-lookup"><span data-stu-id="aa64c-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="aa64c-127">Essa instrução é usada como a última das três instruções que representam uma operação de multiplicação de matriz 3x3, seguida por uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="aa64c-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="aa64c-128">A matriz de 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e dos dois estágios de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="aa64c-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="aa64c-129">O vetor de três componentes resultante (u, v, w) é usado para exemplificar a textura no estágio 3.</span><span class="sxs-lookup"><span data-stu-id="aa64c-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="aa64c-130">Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada.</span><span class="sxs-lookup"><span data-stu-id="aa64c-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="aa64c-131">A multiplicação da matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.</span><span class="sxs-lookup"><span data-stu-id="aa64c-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="aa64c-132">Essa instrução deve ser usada com a instrução texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="aa64c-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="aa64c-133">Os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa64c-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="aa64c-134">Veja mais detalhes sobre como a multiplicação de 3x3 é realizada.</span><span class="sxs-lookup"><span data-stu-id="aa64c-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="aa64c-135">A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="aa64c-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="aa64c-136">u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="aa64c-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="aa64c-137">A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="aa64c-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="aa64c-138">v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="aa64c-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="aa64c-139">A instrução texm3x3spec executa a terceira linha da multiplicação para localizar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="aa64c-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="aa64c-140">w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="aa64c-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="aa64c-141">Por fim, os exemplos de instrução texm3x3tex t (m + 2) com (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e armazena o resultado em t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="aa64c-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="aa64c-142">t (m + 2)<sub>RGBA</sub> = TextureSample (estágio m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas.</span><span class="sxs-lookup"><span data-stu-id="aa64c-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="aa64c-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa64c-143">Examples</span></span>

<span data-ttu-id="aa64c-144">Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="aa64c-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="aa64c-145">Este exemplo requer a configuração de estágio de textura a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa64c-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="aa64c-146">O estágio 0 é atribuído a um mapa de textura com dados normais.</span><span class="sxs-lookup"><span data-stu-id="aa64c-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="aa64c-147">Isso é geralmente conhecido como um mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="aa64c-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="aa64c-148">Os dados são normais (XYZ) para cada Texel.</span><span class="sxs-lookup"><span data-stu-id="aa64c-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="aa64c-149">O conjunto de coordenadas de textura 0 define como fazer a amostragem deste mapa normal.</span><span class="sxs-lookup"><span data-stu-id="aa64c-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="aa64c-150">O conjunto de coordenadas de textura 1 é atribuído à linha 1 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="aa64c-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="aa64c-151">Qualquer textura atribuída ao estágio 1 é ignorada.</span><span class="sxs-lookup"><span data-stu-id="aa64c-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="aa64c-152">O conjunto de coordenadas de textura 2 é atribuído à linha 2 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="aa64c-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="aa64c-153">Qualquer textura atribuída ao estágio 2 é ignorada.</span><span class="sxs-lookup"><span data-stu-id="aa64c-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="aa64c-154">A coordenada de textura definida 3 é atribuída à linha 3 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="aa64c-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="aa64c-155">Uma textura de volume ou cubo deve ser definida como o estágio 3 para pesquisa pelo vetor 3D transformado.</span><span class="sxs-lookup"><span data-stu-id="aa64c-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa64c-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa64c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa64c-157">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="aa64c-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




