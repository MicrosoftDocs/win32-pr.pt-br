---
title: texldp-PS
description: Instrução de carregamento de textura projetada. Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (. a ou. w) logo antes da amostragem.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294479"
---
# <a name="texldp---ps"></a><span data-ttu-id="7ba7b-104">texldp-PS</span><span class="sxs-lookup"><span data-stu-id="7ba7b-104">texldp - ps</span></span>

<span data-ttu-id="7ba7b-105">Instrução de carregamento de textura projetada.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-105">Projected texture load instruction.</span></span> <span data-ttu-id="7ba7b-106">Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (. a ou. w) logo antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba7b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba7b-107">Syntax</span></span>



| <span data-ttu-id="7ba7b-108">texldp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="7ba7b-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="7ba7b-109">onde</span><span class="sxs-lookup"><span data-stu-id="7ba7b-109">where</span></span>

-   <span data-ttu-id="7ba7b-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-110">dst is the destination register.</span></span>
-   <span data-ttu-id="7ba7b-111">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="7ba7b-112">Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="7ba7b-113">src1 identifica a [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="7ba7b-114">O classificador foi associado a ele uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="7ba7b-115">Para obter o conjunto de restrições ao usar texldp, consulte [texld](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba7b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ba7b-116">Remarks</span></span>

<span data-ttu-id="7ba7b-117">texldp executa projeção nas coordenadas lidas de src0 antes de executar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="7ba7b-118">Cada coordenada de textura é dividida por src0. w; em seguida, a textura é amostrada.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="7ba7b-119">Quando o texldp é concluído, o conteúdo de src0 não é afetado (a menos que o DST seja o mesmo registro).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="7ba7b-120">Uma alternativa ao uso de texldp é executar manualmente a divisão de projeção no sombreador.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="7ba7b-121">No entanto, a execução da divisão no código do sombreador é geralmente mais lenta do que quando executada pela instrução texldp, portanto, evite essa matemática adicional quando possível.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="7ba7b-122">O número de coordenadas necessárias para src0 executar o exemplo de textura depende de como src1 foi declarado, além do componente. w.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="7ba7b-123">Os tipos de amostra são declarados com o tipo de [ \_ amostra DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="7ba7b-124">Se src1 for declarado como um classificador 2D, então src0 deverá conter coordenadas. xyw; se src1 for declarado como uma amostra de cubo ou uma amostra de volume, então src0 deverá conter coordenadas. xyzw.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="7ba7b-125">A amostragem de uma textura 2D com coordenadas. xyzw é permitida (a coordenada z é ignorada).</span><span class="sxs-lookup"><span data-stu-id="7ba7b-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="7ba7b-126">Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="7ba7b-127">Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="7ba7b-128">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="7ba7b-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="7ba7b-129">Valores padrão para componentes ausentes</span><span class="sxs-lookup"><span data-stu-id="7ba7b-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="7ba7b-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="7ba7b-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="7ba7b-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-131">A = 1.0</span></span>                               |
| <span data-ttu-id="7ba7b-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="7ba7b-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="7ba7b-133">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="7ba7b-134">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="7ba7b-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="7ba7b-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="7ba7b-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="7ba7b-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="7ba7b-137">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="7ba7b-138">Todos os formatos de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="7ba7b-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="7ba7b-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="7ba7b-140">Essa instrução tem suporte nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="7ba7b-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="7ba7b-141">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7ba7b-141">Pixel shader versions</span></span> | <span data-ttu-id="7ba7b-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="7ba7b-142">1\_1</span></span> | <span data-ttu-id="7ba7b-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="7ba7b-143">1\_2</span></span> | <span data-ttu-id="7ba7b-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7ba7b-144">1\_3</span></span> | <span data-ttu-id="7ba7b-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="7ba7b-145">1\_4</span></span> | <span data-ttu-id="7ba7b-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-146">2\_0</span></span> | <span data-ttu-id="7ba7b-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-147">2\_x</span></span> | <span data-ttu-id="7ba7b-148">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ba7b-148">2\_sw</span></span> | <span data-ttu-id="7ba7b-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-149">3\_0</span></span> | <span data-ttu-id="7ba7b-150">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ba7b-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7ba7b-151">texldp</span><span class="sxs-lookup"><span data-stu-id="7ba7b-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="7ba7b-152">x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-152">x</span></span>    | <span data-ttu-id="7ba7b-153">x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-153">x</span></span>    | <span data-ttu-id="7ba7b-154">x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-154">x</span></span>     | <span data-ttu-id="7ba7b-155">x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-155">x</span></span>    | <span data-ttu-id="7ba7b-156">x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="7ba7b-157">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ba7b-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="7ba7b-158">o horário de verão deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) e somente a máscara de xyzw (máscara padrão) é permitida.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="7ba7b-159">src0 deve ser um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="7ba7b-160">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="7ba7b-161">Se o \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT Cap não estiver definido (em D3DPSHADERCAPS2 \_ 0), uma instrução de textura específica ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) poderá ser dependente, no máximo, terceiro pedido.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="7ba7b-162">Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:</span><span class="sxs-lookup"><span data-stu-id="7ba7b-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="7ba7b-163">src0 é um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="7ba7b-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="7ba7b-164">o DST foi gravado anteriormente, agora sendo gravado novamente.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="7ba7b-165">Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cujo conteúdo, antes de executar a instrução de textura, dependa (talvez indiretamente) no resultado de uma instrução de textura dependente de primeira ordem.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="7ba7b-166">Uma instrução de textura dependente de ordem<sup>th</sup>é derivada de uma instrução de textura de ordem (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="7ba7b-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="7ba7b-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ba7b-167">ps\_3\_0</span></span>

<span data-ttu-id="7ba7b-168">Para \_ o PS 3 \_ 0, src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="7ba7b-169">Swizzle é permitido em src1 e, quando aplicado, os resultados da pesquisa de textura são pré-swizzled antes de gravados no DST.</span><span class="sxs-lookup"><span data-stu-id="7ba7b-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ba7b-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ba7b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ba7b-171">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7ba7b-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 