---
title: texldb-PS
description: Instrução de carregamento de textura tendenciosa. Essa instrução usa o quarto elemento (. a ou. w) para diferenciar o nível de detalhes de amostragem de textura antes da amostragem.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084615"
---
# <a name="texldb---ps"></a><span data-ttu-id="b4eb1-104">texldb-PS</span><span class="sxs-lookup"><span data-stu-id="b4eb1-104">texldb - ps</span></span>

<span data-ttu-id="b4eb1-105">Instrução de carregamento de textura tendenciosa.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-105">Biased texture load instruction.</span></span> <span data-ttu-id="b4eb1-106">Essa instrução usa o quarto elemento (. a ou. w) para diferenciar o nível de detalhes de amostragem de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eb1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4eb1-107">Syntax</span></span>



| <span data-ttu-id="b4eb1-108">texldb DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b4eb1-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="b4eb1-109">Em que:</span><span class="sxs-lookup"><span data-stu-id="b4eb1-109">Where:</span></span>

-   <span data-ttu-id="b4eb1-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-110">dst is the destination register.</span></span>
-   <span data-ttu-id="b4eb1-111">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="b4eb1-112">Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="b4eb1-113">src1 identifica a [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="b4eb1-114">O classificador foi associado a ele uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="b4eb1-115">Para obter as restrições ao usar texldb, consulte a instrução [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="b4eb1-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="b4eb1-116">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="b4eb1-117">o horário de verão deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) e somente a máscara de xyzw (máscara padrão) é permitida.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="b4eb1-118">src0 deve ser um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="b4eb1-119">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="b4eb1-120">Se o \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT Cap não estiver definido (em D3DPSHADERCAPS2 \_ 0), uma instrução de textura específica (texld, texldp, texldb, texldd) poderá ser dependente, no máximo, terceiro.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="b4eb1-121">Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:</span><span class="sxs-lookup"><span data-stu-id="b4eb1-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="b4eb1-122">src0 é um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="b4eb1-123">o DST foi gravado anteriormente, agora sendo gravado novamente.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="b4eb1-124">Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cujo conteúdo, antes de executar a instrução de textura, dependa (talvez indiretamente) no resultado de uma instrução de textura dependente de primeira ordem.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="b4eb1-125">Uma instrução de textura dependente de ordem<sup>th</sup>é derivada de uma instrução de textura de ordem (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="b4eb1-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="b4eb1-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-126">ps\_3\_0</span></span>

<span data-ttu-id="b4eb1-127">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem nenhum modificador.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="b4eb1-128">Swizzle é permitido em src1 e, quando aplicado, os resultados da pesquisa de textura são pré-swizzled antes de gravados no DST.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4eb1-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4eb1-129">Remarks</span></span>



| <span data-ttu-id="b4eb1-130">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b4eb1-130">Pixel shader versions</span></span> | <span data-ttu-id="b4eb1-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="b4eb1-131">1\_1</span></span> | <span data-ttu-id="b4eb1-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="b4eb1-132">1\_2</span></span> | <span data-ttu-id="b4eb1-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b4eb1-133">1\_3</span></span> | <span data-ttu-id="b4eb1-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="b4eb1-134">1\_4</span></span> | <span data-ttu-id="b4eb1-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-135">2\_0</span></span> | <span data-ttu-id="b4eb1-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-136">2\_x</span></span> | <span data-ttu-id="b4eb1-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b4eb1-137">2\_sw</span></span> | <span data-ttu-id="b4eb1-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-138">3\_0</span></span> | <span data-ttu-id="b4eb1-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b4eb1-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b4eb1-140">texldb</span><span class="sxs-lookup"><span data-stu-id="b4eb1-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="b4eb1-141">x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-141">x</span></span>    | <span data-ttu-id="b4eb1-142">x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-142">x</span></span>    | <span data-ttu-id="b4eb1-143">x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-143">x</span></span>     | <span data-ttu-id="b4eb1-144">x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-144">x</span></span>    | <span data-ttu-id="b4eb1-145">x</span><span class="sxs-lookup"><span data-stu-id="b4eb1-145">x</span></span>     |



 

<span data-ttu-id="b4eb1-146">texldb ajusta o nível de detalhe mipmap, calculado normalmente como parte do processo de exemplo pelo valor (assinado) em src0. w.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="b4eb1-147">Valores de tendência positivos resultarão na seleção de mipmaps menor e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="b4eb1-148">Para PS \_ 2 \_ 0 e PS \_ 2 \_ x, os valores de tendência podem estar dentro do intervalo \[ de-3,0, + 3,0 \] .</span><span class="sxs-lookup"><span data-stu-id="b4eb1-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="b4eb1-149">Para \_ o PS 3 \_ 0, os valores de tendência podem estar dentro do intervalo \[ de-16,0, + 15,0 \] .</span><span class="sxs-lookup"><span data-stu-id="b4eb1-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="b4eb1-150">Os valores de tendência fora desses intervalos produzem resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="b4eb1-151">O estado de amostra D3DSAMP \_ MIPMAPLODBIAS ainda é respeitado, e a tendência de texldb é adicionada a isso, mas em uma base por pixel.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="b4eb1-152">Depois que o nível de detalhe tendenciosa é calculado, D3DSAMP \_ MAXMIPLEVEL ainda é respeitado e ocorre o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="b4eb1-153">Após texldb, o conteúdo de src0 não será afetado (a menos que o DST seja o mesmo registro).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="b4eb1-154">O número de coordenadas necessárias para src0 executar o exemplo de textura depende de como src1 foi declarado, além do componente. w.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="b4eb1-155">Os tipos de amostra são declarados com o tipo de [ \_ amostra DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="b4eb1-156">Se src1 for declarado como um classificador 2D, então src0 deverá conter coordenadas. xyw; se src1 for declarado como uma amostra de cubo ou uma amostra de volume, então src0 deverá conter coordenadas. xyzw.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="b4eb1-157">A amostragem de uma textura 2D com coordenadas. xyzw é permitida (a coordenada z é ignorada).</span><span class="sxs-lookup"><span data-stu-id="b4eb1-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="b4eb1-158">Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="b4eb1-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="b4eb1-159">Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="b4eb1-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="b4eb1-160">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="b4eb1-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="b4eb1-161">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="b4eb1-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="b4eb1-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="b4eb1-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="b4eb1-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-163">A = 1.0</span></span>              |
| <span data-ttu-id="b4eb1-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="b4eb1-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="b4eb1-165">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="b4eb1-166">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="b4eb1-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="b4eb1-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="b4eb1-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="b4eb1-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="b4eb1-169">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="b4eb1-170">Todos os formatos de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="b4eb1-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="b4eb1-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="b4eb1-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b4eb1-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4eb1-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4eb1-173">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b4eb1-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 