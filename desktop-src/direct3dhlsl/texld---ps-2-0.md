---
title: texld-ps_2_0 e cima
description: Exemplo de uma textura em uma amostra específica, usando coordenadas de textura fornecidas. Essa instrução é diferente da instrução texld-PS \_ 1 \_ 4 usada no sombreador de pixel versão 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499077"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="003d2-104">texld-PS \_ 2 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="003d2-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="003d2-105">Exemplo de uma textura em uma amostra específica, usando coordenadas de textura fornecidas.</span><span class="sxs-lookup"><span data-stu-id="003d2-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="003d2-106">Essa instrução é diferente da instrução [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) usada no sombreador de pixel versão 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="003d2-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="003d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="003d2-107">Syntax</span></span>



| <span data-ttu-id="003d2-108">texld DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="003d2-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="003d2-109">Em que:</span><span class="sxs-lookup"><span data-stu-id="003d2-109">Where:</span></span>

-   <span data-ttu-id="003d2-110">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="003d2-110">dst is a destination register.</span></span>
-   <span data-ttu-id="003d2-111">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="003d2-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="003d2-112">src1 identifica a [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="003d2-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="003d2-113">O classificador foi associado a ele uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="003d2-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="003d2-114">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="003d2-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="003d2-115">o horário de verão deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) e somente a máscara de xyzw (máscara padrão) é permitida.</span><span class="sxs-lookup"><span data-stu-id="003d2-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="003d2-116">src0 deve ser um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="003d2-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="003d2-117">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador ou swizzle.</span><span class="sxs-lookup"><span data-stu-id="003d2-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="003d2-118">Se o \_ bit D3DD3DPSHADERCAPS2 \_ 0 NODEPENDENTREADLIMIT Cap não estiver definido (em D3DPSHADERCAPS2 \_ 0), uma instrução de textura específica[(texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) poderá ser dependente, no máximo, terceiro pedido.</span><span class="sxs-lookup"><span data-stu-id="003d2-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="003d2-119">Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:</span><span class="sxs-lookup"><span data-stu-id="003d2-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="003d2-120">src0 é um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="003d2-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="003d2-121">o DST foi gravado anteriormente, agora sendo gravado novamente.</span><span class="sxs-lookup"><span data-stu-id="003d2-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="003d2-122">Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cujo conteúdo, antes de executar a instrução de textura, dependa (talvez indiretamente) no resultado de uma instrução de textura dependente de primeira ordem.</span><span class="sxs-lookup"><span data-stu-id="003d2-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="003d2-123">Uma instrução de textura dependente de ordem<sup>th</sup>é derivada de uma instrução de textura de ordem (n-<sup>1).</sup></span><span class="sxs-lookup"><span data-stu-id="003d2-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="003d2-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="003d2-124">ps\_3\_0</span></span>

<span data-ttu-id="003d2-125">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem nenhum modificador.</span><span class="sxs-lookup"><span data-stu-id="003d2-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="003d2-126">Swizzle é permitido em src0 ou src1.</span><span class="sxs-lookup"><span data-stu-id="003d2-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="003d2-127">O swizzle é aplicado ao coordintates de textura antes da pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="003d2-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="003d2-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="003d2-128">Remarks</span></span>

<span data-ttu-id="003d2-129">Essa instrução tem suporte nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="003d2-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="003d2-130">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="003d2-130">Pixel shader versions</span></span> | <span data-ttu-id="003d2-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="003d2-131">1\_1</span></span> | <span data-ttu-id="003d2-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="003d2-132">1\_2</span></span> | <span data-ttu-id="003d2-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="003d2-133">1\_3</span></span> | <span data-ttu-id="003d2-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="003d2-134">1\_4</span></span> | <span data-ttu-id="003d2-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="003d2-135">2\_0</span></span> | <span data-ttu-id="003d2-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="003d2-136">2\_x</span></span> | <span data-ttu-id="003d2-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="003d2-137">2\_sw</span></span> | <span data-ttu-id="003d2-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="003d2-138">3\_0</span></span> | <span data-ttu-id="003d2-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="003d2-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="003d2-140">texld</span><span class="sxs-lookup"><span data-stu-id="003d2-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="003d2-141">x</span><span class="sxs-lookup"><span data-stu-id="003d2-141">x</span></span>    | <span data-ttu-id="003d2-142">x</span><span class="sxs-lookup"><span data-stu-id="003d2-142">x</span></span>    | <span data-ttu-id="003d2-143">x</span><span class="sxs-lookup"><span data-stu-id="003d2-143">x</span></span>     | <span data-ttu-id="003d2-144">x</span><span class="sxs-lookup"><span data-stu-id="003d2-144">x</span></span>    | <span data-ttu-id="003d2-145">x</span><span class="sxs-lookup"><span data-stu-id="003d2-145">x</span></span>     |



 

<span data-ttu-id="003d2-146">O número de coordenadas necessárias para src0 executar o exemplo de textura depende de como src1 foi declarado, além do componente. w.</span><span class="sxs-lookup"><span data-stu-id="003d2-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="003d2-147">Os tipos de amostra são declarados com o tipo de [ \_ amostra DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="003d2-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="003d2-148">Se src1 for declarado como uma amostra 2D, então src0 deverá conter as coordenadas. XY; se src1 for declarado como uma amostra de cubo ou uma amostra de volume, então src0 deverá conter coordenadas. xyz.</span><span class="sxs-lookup"><span data-stu-id="003d2-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="003d2-149">É permitida a amostragem de uma textura com menos dimensões do que as presentes na coordenada de textura, pois os componentes da coordenada de textura extra são ignorados.</span><span class="sxs-lookup"><span data-stu-id="003d2-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="003d2-150">Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="003d2-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="003d2-151">Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="003d2-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="003d2-152">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="003d2-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="003d2-153">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="003d2-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="003d2-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="003d2-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="003d2-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="003d2-155">A = 1.0</span></span>              |
| <span data-ttu-id="003d2-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT G16R16F \_ , D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="003d2-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="003d2-157">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="003d2-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="003d2-158">D3DFMT \_ a8</span><span class="sxs-lookup"><span data-stu-id="003d2-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="003d2-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="003d2-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="003d2-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="003d2-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="003d2-161">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="003d2-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="003d2-162">Todos os formatos de profundidade/estêncil</span><span class="sxs-lookup"><span data-stu-id="003d2-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="003d2-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="003d2-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="003d2-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="003d2-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="003d2-165">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="003d2-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 