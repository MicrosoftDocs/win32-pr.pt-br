---
title: ResInfo (sm4-ASM)
description: Consultar as dimensões de um determinado recurso de entrada.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365216"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="30441-103">ResInfo (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="30441-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="30441-104">Consultar as dimensões de um determinado recurso de entrada.</span><span class="sxs-lookup"><span data-stu-id="30441-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="30441-105">ResInfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="30441-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="30441-106">\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Selecione \_ componente, srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="30441-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="30441-107">Item</span><span class="sxs-lookup"><span data-stu-id="30441-107">Item</span></span>                                                                                                               | <span data-ttu-id="30441-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="30441-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30441-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="30441-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="30441-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="30441-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="30441-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span><span class="sxs-lookup"><span data-stu-id="30441-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="30441-112">\[no \] nível MIP.</span><span class="sxs-lookup"><span data-stu-id="30441-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="30441-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="30441-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="30441-114">\[em \] uma \# \# textura de entrada t ou u para a qual as dimensões estão sendo consultadas.</span><span class="sxs-lookup"><span data-stu-id="30441-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="30441-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="30441-115">Remarks</span></span>

<span data-ttu-id="30441-116">*srcMipLevel* é lido como um escalar de inteiro sem sinal, de modo que um único seletor de componente é necessário para o registro de origem, se não for um valor escalar imediato.</span><span class="sxs-lookup"><span data-stu-id="30441-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="30441-117">o *dest* recebe \[ a largura, a altura, a profundidade ou o tamanho da matriz, total-MIP-Count \] , selecionado pela máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="30441-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="30441-118">Os valores de largura, altura e profundidade retornados são para o nível de MIP selecionado pelo parâmetro *srcMipLevel* e estão no número de texels, independentemente do tamanho dos dados do Texel.</span><span class="sxs-lookup"><span data-stu-id="30441-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="30441-119">Para recursos de multiamostra ( \[ matriz texture2D \] MS \# ), a largura e a altura também são retornadas em texels, não em exemplos.</span><span class="sxs-lookup"><span data-stu-id="30441-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="30441-120">A contagem total de MIP retornada no *dest. w* não é afetada pelo parâmetro *srcMipLevel* .</span><span class="sxs-lookup"><span data-stu-id="30441-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="30441-121">Para UAVs (u \# ), o número de níveis MIP é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="30441-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="30441-122">Todos os aspectos desta instrução baseiam-se nas características da exibição de recurso associada ao t \# /u \# , não ao recurso base subjacente.</span><span class="sxs-lookup"><span data-stu-id="30441-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="30441-123">Os valores retornados são todos os pontos flutuantes, a menos que o \_ modificador uint seja usado; nesse caso, os valores retornados são todos os inteiros.</span><span class="sxs-lookup"><span data-stu-id="30441-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="30441-124">Se o \_ modificador rcpFloat for usado, todos os valores retornados serão de ponto flutuante, e a largura, a altura e a profundidade serão retornadas como recíprocos (1,0 f/largura, 1,0 f/altura, 1,0 f/profundidade), incluindo inf se largura/altura/profundidade forem 0 do comportamento *srcMipLevel* fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="30441-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="30441-125">O \_ modificador rcpFloat só se aplica a valores de largura, altura e profundidade retornados e não se aplica a valores que são definidos como 0 e, portanto, não retornados e também não se aplicam a retornos de tamanho de matriz.</span><span class="sxs-lookup"><span data-stu-id="30441-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="30441-126">O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="30441-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="30441-127">Se *srcResource* for um Texture1D, a largura será retornada em *dest. x* e *dest. YZ* serão definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="30441-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="30441-128">Se *srcResource* for um Texture1DArray, a largura será retornada em *dest. x*, o tamanho da matriz será retornado em *dest. y* e *dest. z* será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="30441-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="30441-129">Se *srcResource* for um Texture2D, a largura e a altura serão retornadas em *dest. XY* e *dest. z* será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="30441-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="30441-130">Se *srcResource* for um Texture2DArray, a largura e a altura serão retornadas em *dest. XY* e o tamanho da matriz será retornado em *dest. z*.</span><span class="sxs-lookup"><span data-stu-id="30441-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="30441-131">Se *srcResource* for um Texture3D, a largura, a altura e a profundidade serão retornadas em *dest.xyz*.</span><span class="sxs-lookup"><span data-stu-id="30441-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="30441-132">Se *srcResource* for um TextureCube, a largura e a altura das dimensões de face do cubo individual serão retornadas em *dest. XY* e *dest. z* será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="30441-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="30441-133">Se *srcResource* for um TextureCubeArray, a largura e a altura das dimensões de face do cubo individual serão retornadas em *dest. XY*.</span><span class="sxs-lookup"><span data-stu-id="30441-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="30441-134">*dest. z* é definido como um valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="30441-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="30441-135">Se o fixe MIP por recurso for especificado em *srcResource*, ResInfo sempre retornará o número total de mipmaps na exibição para a contagem MIP, independentemente do fixe.</span><span class="sxs-lookup"><span data-stu-id="30441-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="30441-136">No entanto, se as dimensões de um determinado MipLevel forem solicitadas por ResInfo e o MipLevel tiver sido clamped desativado (por exemplo, um fixe de 2,2 significa que o MIPS 0 e o 1 foram clamped), as dimensões retornadas serão indefinidas.</span><span class="sxs-lookup"><span data-stu-id="30441-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="30441-137">Algumas implementações retornarão o comportamento fora dos limites especificado para ResInfo quando o MipLevel estiver fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="30441-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="30441-138">Outras implementações retornarão as dimensões de MIP como se não tivesse sido clamped.</span><span class="sxs-lookup"><span data-stu-id="30441-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="30441-139">Restrições</span><span class="sxs-lookup"><span data-stu-id="30441-139">Restrictions</span></span>

-   <span data-ttu-id="30441-140">*srcResource* deve ser um \# registro t ou u \# que não seja um buffer, mas é uma textura \* .</span><span class="sxs-lookup"><span data-stu-id="30441-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="30441-141">O endereçamento relativo de *srcResource* não é permitido.</span><span class="sxs-lookup"><span data-stu-id="30441-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="30441-142">*srcMipLevel* deve usar um seletor de componente único se não for um escalar imediato.</span><span class="sxs-lookup"><span data-stu-id="30441-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="30441-143">A busca de t \# ou u \# que não tem nada associado a ele retorna 0 para largura, altura, profundidade ou matrizize e total-MIP-Count.</span><span class="sxs-lookup"><span data-stu-id="30441-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="30441-144">O \_ modificador rcpFloat ainda é respeitado nesse caso, retornando, portanto, o inf para os valores retornados aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="30441-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="30441-145">Se *srcMipLevel* estiver fora do intervalo do número disponível de miplevels no recurso, o comportamento para o retorno de tamanho (*dest.xyz*) é idêntico ao de um recurso t ou u não associado \# \# .</span><span class="sxs-lookup"><span data-stu-id="30441-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="30441-146">A contagem total de MIP ainda é retornada no *dest. w* para esse caso.</span><span class="sxs-lookup"><span data-stu-id="30441-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="30441-147">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="30441-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="30441-148">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="30441-148">Vertex Shader</span></span> | <span data-ttu-id="30441-149">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="30441-149">Geometry Shader</span></span> | <span data-ttu-id="30441-150">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="30441-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="30441-151">x</span><span class="sxs-lookup"><span data-stu-id="30441-151">x</span></span>             | <span data-ttu-id="30441-152">x</span><span class="sxs-lookup"><span data-stu-id="30441-152">x</span></span>               | <span data-ttu-id="30441-153">x</span><span class="sxs-lookup"><span data-stu-id="30441-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="30441-154">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="30441-154">Minimum Shader Model</span></span>

<span data-ttu-id="30441-155">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="30441-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="30441-156">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="30441-156">Shader Model</span></span>                                              | <span data-ttu-id="30441-157">Com suporte</span><span class="sxs-lookup"><span data-stu-id="30441-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="30441-158">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="30441-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="30441-159">sim</span><span class="sxs-lookup"><span data-stu-id="30441-159">yes</span></span>       |
| [<span data-ttu-id="30441-160">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="30441-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="30441-161">sim</span><span class="sxs-lookup"><span data-stu-id="30441-161">yes</span></span>       |
| [<span data-ttu-id="30441-162">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="30441-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="30441-163">sim</span><span class="sxs-lookup"><span data-stu-id="30441-163">yes</span></span>       |
| [<span data-ttu-id="30441-164">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30441-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="30441-165">não</span><span class="sxs-lookup"><span data-stu-id="30441-165">no</span></span>        |
| [<span data-ttu-id="30441-166">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30441-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="30441-167">não</span><span class="sxs-lookup"><span data-stu-id="30441-167">no</span></span>        |
| [<span data-ttu-id="30441-168">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30441-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="30441-169">não</span><span class="sxs-lookup"><span data-stu-id="30441-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="30441-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30441-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30441-171">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30441-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





