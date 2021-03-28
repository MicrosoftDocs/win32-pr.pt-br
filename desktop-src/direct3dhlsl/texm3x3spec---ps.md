---
title: texm3x3spec-PS
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura. Isso pode ser usado para a reflexão especular e o mapeamento de ambiente. texm3x3spec deve ser usado em conjunto com duas instruções texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365215"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="a64c8-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="a64c8-105">texm3x3spec - ps</span></span>

<span data-ttu-id="a64c8-106">Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="a64c8-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="a64c8-107">Isso pode ser usado para a reflexão especular e o mapeamento de ambiente.</span><span class="sxs-lookup"><span data-stu-id="a64c8-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="a64c8-108">texm3x3spec deve ser usado em conjunto com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="a64c8-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a64c8-109">Syntax</span></span>



| <span data-ttu-id="a64c8-110">texm3x3spec DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a64c8-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="a64c8-111">onde</span><span class="sxs-lookup"><span data-stu-id="a64c8-111">where</span></span>

-   <span data-ttu-id="a64c8-112">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a64c8-112">dst is the destination register.</span></span>
-   <span data-ttu-id="a64c8-113">src0 e src1 são registros de origem.</span><span class="sxs-lookup"><span data-stu-id="a64c8-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="a64c8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a64c8-114">Remarks</span></span>



| <span data-ttu-id="a64c8-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a64c8-115">Pixel shader versions</span></span> | <span data-ttu-id="a64c8-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="a64c8-116">1\_1</span></span> | <span data-ttu-id="a64c8-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="a64c8-117">1\_2</span></span> | <span data-ttu-id="a64c8-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a64c8-118">1\_3</span></span> | <span data-ttu-id="a64c8-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="a64c8-119">1\_4</span></span> | <span data-ttu-id="a64c8-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a64c8-120">2\_0</span></span> | <span data-ttu-id="a64c8-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a64c8-121">2\_x</span></span> | <span data-ttu-id="a64c8-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a64c8-122">2\_sw</span></span> | <span data-ttu-id="a64c8-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a64c8-123">3\_0</span></span> | <span data-ttu-id="a64c8-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a64c8-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a64c8-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="a64c8-125">texm3x3spec</span></span>           | <span data-ttu-id="a64c8-126">x</span><span class="sxs-lookup"><span data-stu-id="a64c8-126">x</span></span>    | <span data-ttu-id="a64c8-127">x</span><span class="sxs-lookup"><span data-stu-id="a64c8-127">x</span></span>    | <span data-ttu-id="a64c8-128">x</span><span class="sxs-lookup"><span data-stu-id="a64c8-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="a64c8-129">Essa instrução executa a linha final de uma multiplicação de matriz 3x3, usa o vetor resultante como um vetor normal para refletir um vetor de raio e, em seguida, usa o vetor refletido para executar uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="a64c8-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="a64c8-130">O sombreador lê o vetor de olho-raio de um registro constante.</span><span class="sxs-lookup"><span data-stu-id="a64c8-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="a64c8-131">A multiplicação da matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.</span><span class="sxs-lookup"><span data-stu-id="a64c8-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="a64c8-132">A matriz de 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e dos dois estágios de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="a64c8-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="a64c8-133">O vetor de reflexo posterior (u, v, w) resultante é usado para exemplificar a textura no estágio de textura final.</span><span class="sxs-lookup"><span data-stu-id="a64c8-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="a64c8-134">Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada.</span><span class="sxs-lookup"><span data-stu-id="a64c8-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="a64c8-135">Essa instrução deve ser usada com duas instruções texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="a64c8-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="a64c8-136">Os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="a64c8-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="a64c8-137">A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="a64c8-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="a64c8-138">u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="a64c8-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="a64c8-139">A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="a64c8-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="a64c8-140">v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="a64c8-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="a64c8-141">A instrução texm3x3spec executa a terceira linha da multiplicação para localizar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="a64c8-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="a64c8-142">w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="a64c8-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="a64c8-143">Em seguida, a instrução texm3x3spec faz um cálculo de reflexo.</span><span class="sxs-lookup"><span data-stu-id="a64c8-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="a64c8-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="a64c8-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="a64c8-145">onde o N normal é fornecido por</span><span class="sxs-lookup"><span data-stu-id="a64c8-145">// where the normal N is given by</span></span>

<span data-ttu-id="a64c8-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="a64c8-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="a64c8-147">e o vetor de raio de olho e é fornecido pelo registro constante</span><span class="sxs-lookup"><span data-stu-id="a64c8-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="a64c8-148">E = c \# (qualquer constante Register--C0, C1, C2, etc.--pode ser usado)</span><span class="sxs-lookup"><span data-stu-id="a64c8-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="a64c8-149">Por fim, os exemplos de instrução texm3x3spec t (m + 2) com (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e armazena o resultado em t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="a64c8-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="a64c8-150">t (m + 2)<sub>RGBA</sub> = TextureSample (estágio m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="a64c8-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="a64c8-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a64c8-151">Examples</span></span>

<span data-ttu-id="a64c8-152">Aqui está um sombreador de exemplo com os mapas de textura e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="a64c8-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="a64c8-153">Este exemplo requer a configuração de estágio de textura a seguir.</span><span class="sxs-lookup"><span data-stu-id="a64c8-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="a64c8-154">O estágio 0 é atribuído a um mapa de textura com dados normais.</span><span class="sxs-lookup"><span data-stu-id="a64c8-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="a64c8-155">Isso é geralmente conhecido como um mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="a64c8-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="a64c8-156">Os dados são normais (XYZ) para cada Texel.</span><span class="sxs-lookup"><span data-stu-id="a64c8-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="a64c8-157">As coordenadas de textura no estágio n definem onde fazer a amostragem deste mapa normal.</span><span class="sxs-lookup"><span data-stu-id="a64c8-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="a64c8-158">O conjunto de coordenadas de textura m é atribuído à linha 1 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="a64c8-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="a64c8-159">Qualquer textura atribuída ao estágio m é ignorada.</span><span class="sxs-lookup"><span data-stu-id="a64c8-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="a64c8-160">O conjunto de coordenadas de textura m + 1 é atribuído à linha 2 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="a64c8-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="a64c8-161">Qualquer textura atribuída ao estágio m + 1 é ignorada.</span><span class="sxs-lookup"><span data-stu-id="a64c8-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="a64c8-162">O conjunto de coordenadas de textura m + 2 é atribuído à linha 3 da matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="a64c8-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="a64c8-163">O estágio m + 2 é atribuído a um mapa de textura de um volume ou cubo.</span><span class="sxs-lookup"><span data-stu-id="a64c8-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="a64c8-164">A textura fornece dados de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="a64c8-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="a64c8-165">O vetor de raio de olho E é fornecido por uma constante Register E = c \# .</span><span class="sxs-lookup"><span data-stu-id="a64c8-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a64c8-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a64c8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64c8-167">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a64c8-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




