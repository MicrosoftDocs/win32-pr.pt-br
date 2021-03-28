---
title: texm3x3vspec-PS
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916881"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="f57e3-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="f57e3-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="f57e3-104">Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="f57e3-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="f57e3-105">Isso pode ser usado para a reflexão especular e o mapeamento de ambiente em que o vetor de raio de olho não é constante.</span><span class="sxs-lookup"><span data-stu-id="f57e3-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="f57e3-106">texm3x3vspec deve ser usado em conjunto com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f57e3-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="f57e3-107">Se o vetor de raio de olho for constante, a instrução [texm3x3spec-PS](texm3x3spec---ps.md) executará a mesma matriz de multiplicação e pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="f57e3-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="f57e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f57e3-108">Syntax</span></span>



| <span data-ttu-id="f57e3-109">texm3x3vspec DST, src</span><span class="sxs-lookup"><span data-stu-id="f57e3-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="f57e3-110">onde</span><span class="sxs-lookup"><span data-stu-id="f57e3-110">where</span></span>

-   <span data-ttu-id="f57e3-111">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f57e3-111">dst is the destination register.</span></span>
-   <span data-ttu-id="f57e3-112">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="f57e3-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f57e3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f57e3-113">Remarks</span></span>



| <span data-ttu-id="f57e3-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f57e3-114">Pixel shader versions</span></span> | <span data-ttu-id="f57e3-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f57e3-115">1\_1</span></span> | <span data-ttu-id="f57e3-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="f57e3-116">1\_2</span></span> | <span data-ttu-id="f57e3-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f57e3-117">1\_3</span></span> | <span data-ttu-id="f57e3-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="f57e3-118">1\_4</span></span> | <span data-ttu-id="f57e3-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f57e3-119">2\_0</span></span> | <span data-ttu-id="f57e3-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f57e3-120">2\_x</span></span> | <span data-ttu-id="f57e3-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f57e3-121">2\_sw</span></span> | <span data-ttu-id="f57e3-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f57e3-122">3\_0</span></span> | <span data-ttu-id="f57e3-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f57e3-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f57e3-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="f57e3-124">texm3x3vspec</span></span>          | <span data-ttu-id="f57e3-125">x</span><span class="sxs-lookup"><span data-stu-id="f57e3-125">x</span></span>    | <span data-ttu-id="f57e3-126">x</span><span class="sxs-lookup"><span data-stu-id="f57e3-126">x</span></span>    | <span data-ttu-id="f57e3-127">x</span><span class="sxs-lookup"><span data-stu-id="f57e3-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="f57e3-128">Essa instrução executa a linha final de uma operação de multiplicação de matriz de 3x3, interpreta o vetor resultante como um vetor normal para refletir um vetor de raio de olho e, em seguida, usa o vetor refletido como um endereço de textura para uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="f57e3-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="f57e3-129">Ele funciona exatamente como [texm3x3spec-PS](texm3x3spec---ps.md), exceto pelo fato de que o vetor de raio de olho é tirado do quarto componente das coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f57e3-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="f57e3-130">A multiplicação da matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.</span><span class="sxs-lookup"><span data-stu-id="f57e3-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="f57e3-131">A matriz de 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e dos dois estágios de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="f57e3-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="f57e3-132">O vetor pós-reflexão resultante (UVW) é usado para exemplificar a textura no estágio 3.</span><span class="sxs-lookup"><span data-stu-id="f57e3-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="f57e3-133">Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada.</span><span class="sxs-lookup"><span data-stu-id="f57e3-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="f57e3-134">Essa instrução deve ser usada com a instrução texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="f57e3-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="f57e3-135">Os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="f57e3-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="f57e3-136">A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f57e3-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="f57e3-137">u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f57e3-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="f57e3-138">A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f57e3-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="f57e3-139">v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f57e3-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f57e3-140">A instrução texm3x3spec executa a terceira linha da multiplicação para localizar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f57e3-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="f57e3-141">w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f57e3-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f57e3-142">A instrução texm3x3vspec também faz um cálculo de reflexo.</span><span class="sxs-lookup"><span data-stu-id="f57e3-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="f57e3-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="f57e3-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="f57e3-144">onde o N normal é fornecido por</span><span class="sxs-lookup"><span data-stu-id="f57e3-144">// where the normal N is given by</span></span>

<span data-ttu-id="f57e3-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="f57e3-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="f57e3-146">e o vetor de raio de olho e é fornecido por</span><span class="sxs-lookup"><span data-stu-id="f57e3-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="f57e3-147">E = (TextureCoordinates (estágio m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="f57e3-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="f57e3-148">TextureCoordinates (etapa m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="f57e3-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="f57e3-149">TextureCoordinates (etapa m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="f57e3-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="f57e3-150">Por fim, os exemplos de instrução texm3x3vspec t (m + 2) com (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e armazena o resultado em t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="f57e3-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="f57e3-151">t (m + 2)<sub>RGBA</sub> = TextureSample (estágio m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="f57e3-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="f57e3-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f57e3-152">Examples</span></span>

<span data-ttu-id="f57e3-153">Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="f57e3-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="f57e3-154">Este exemplo requer a configuração de estágio de textura a seguir.</span><span class="sxs-lookup"><span data-stu-id="f57e3-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="f57e3-155">O estágio 0 é atribuído a um mapa de textura com dados normais.</span><span class="sxs-lookup"><span data-stu-id="f57e3-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="f57e3-156">Isso é geralmente conhecido como um mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="f57e3-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="f57e3-157">Os dados são normais (XYZ) para cada Texel.</span><span class="sxs-lookup"><span data-stu-id="f57e3-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="f57e3-158">As coordenadas de textura no estágio n definem como fazer a amostragem deste mapa normal.</span><span class="sxs-lookup"><span data-stu-id="f57e3-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="f57e3-159">O conjunto de coordenadas de textura m é atribuído à linha 1 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f57e3-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="f57e3-160">Qualquer textura atribuída ao estágio m é ignorada.</span><span class="sxs-lookup"><span data-stu-id="f57e3-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="f57e3-161">O conjunto de coordenadas de textura m + 1 é atribuído à linha 2 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f57e3-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="f57e3-162">Qualquer textura atribuída ao estágio m + 1 é ignorada.</span><span class="sxs-lookup"><span data-stu-id="f57e3-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="f57e3-163">O conjunto de coordenadas de textura m + 2 é atribuído à linha 3 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f57e3-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="f57e3-164">O estágio m + 2 é atribuído a um mapa de textura de um volume ou cubo.</span><span class="sxs-lookup"><span data-stu-id="f57e3-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="f57e3-165">A textura fornece dados de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="f57e3-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="f57e3-166">O vetor de raio de olho E é passado para a instrução no quarto componente (q) dos dados de coordenadas de textura em estágios m, m + 1 e m + 2.</span><span class="sxs-lookup"><span data-stu-id="f57e3-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f57e3-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f57e3-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f57e3-168">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f57e3-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




