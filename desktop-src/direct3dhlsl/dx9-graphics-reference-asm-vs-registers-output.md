---
title: Registros de saída
description: Registros de saída
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988501"
---
# <a name="output-registers"></a><span data-ttu-id="6fb11-103">Registros de saída</span><span class="sxs-lookup"><span data-stu-id="6fb11-103">Output Registers</span></span>

-   <span data-ttu-id="6fb11-104">Registro de cor do vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-104">Vertex Color Register</span></span>
-   <span data-ttu-id="6fb11-105">Registro de neblina</span><span class="sxs-lookup"><span data-stu-id="6fb11-105">Fog Register</span></span>
-   <span data-ttu-id="6fb11-106">Registro de posição \_</span><span class="sxs-lookup"><span data-stu-id="6fb11-106">Position\_Register</span></span>
-   <span data-ttu-id="6fb11-107">\_Registro de tamanho do ponto \_</span><span class="sxs-lookup"><span data-stu-id="6fb11-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="6fb11-108">\_Registro de coordenadas de textura \_</span><span class="sxs-lookup"><span data-stu-id="6fb11-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="6fb11-109">Os nomes de registro são precedidos por uma letra minúscula o, indicando que os registros de saída são somente gravação.</span><span class="sxs-lookup"><span data-stu-id="6fb11-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="6fb11-110">Registro de cor do vértice-oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="6fb11-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="6fb11-111">oD0 é o registro de cores difusas.</span><span class="sxs-lookup"><span data-stu-id="6fb11-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="6fb11-112">oD1 é o registro de cor especular.</span><span class="sxs-lookup"><span data-stu-id="6fb11-112">oD1 is the specular color register.</span></span> <span data-ttu-id="6fb11-113">O valor de oD0 é interpolado e gravado no registro de cor de entrada 0 (V0) do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6fb11-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="6fb11-114">O valor de oD1 é interpolado e gravado no registro de cor de entrada 1 (v1) do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6fb11-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="6fb11-115">Para obter mais informações sobre registros de cores do sombreador de pixel, consulte registros.</span><span class="sxs-lookup"><span data-stu-id="6fb11-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="6fb11-116">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-116">Vertex shader versions</span></span> | <span data-ttu-id="6fb11-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fb11-117">1\_1</span></span> | <span data-ttu-id="6fb11-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-118">2\_0</span></span> | <span data-ttu-id="6fb11-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-119">2\_sw</span></span> | <span data-ttu-id="6fb11-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fb11-120">2\_x</span></span> | <span data-ttu-id="6fb11-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-121">3\_0</span></span> | <span data-ttu-id="6fb11-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fb11-123">Registro de cor do vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-123">Vertex Color Register</span></span>  | <span data-ttu-id="6fb11-124">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-124">x</span></span>    | <span data-ttu-id="6fb11-125">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-125">x</span></span>    | <span data-ttu-id="6fb11-126">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-126">x</span></span>     | <span data-ttu-id="6fb11-127">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="6fb11-128">Registro de neblina-oFog</span><span class="sxs-lookup"><span data-stu-id="6fb11-128">Fog Register - oFog</span></span>

<span data-ttu-id="6fb11-129">O valor de neblina de saída é registrado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-129">The output fog value registers.</span></span> <span data-ttu-id="6fb11-130">O valor é o fator de neblina a ser interpolado e, em seguida, roteado para a tabela de neblina.</span><span class="sxs-lookup"><span data-stu-id="6fb11-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="6fb11-131">Somente o componente x escalar da neblina é usado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="6fb11-132">Os valores são clamped entre zero e um antes de passar para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="6fb11-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="6fb11-133">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-133">Vertex shader versions</span></span> | <span data-ttu-id="6fb11-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fb11-134">1\_1</span></span> | <span data-ttu-id="6fb11-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-135">2\_0</span></span> | <span data-ttu-id="6fb11-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-136">2\_sw</span></span> | <span data-ttu-id="6fb11-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fb11-137">2\_x</span></span> | <span data-ttu-id="6fb11-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-138">3\_0</span></span> | <span data-ttu-id="6fb11-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fb11-140">Registro de neblina</span><span class="sxs-lookup"><span data-stu-id="6fb11-140">Fog Register</span></span>           | <span data-ttu-id="6fb11-141">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-141">x</span></span>    | <span data-ttu-id="6fb11-142">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-142">x</span></span>    | <span data-ttu-id="6fb11-143">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-143">x</span></span>     | <span data-ttu-id="6fb11-144">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="6fb11-145">Registro de posição – oPos</span><span class="sxs-lookup"><span data-stu-id="6fb11-145">Position Register - oPos</span></span>

<span data-ttu-id="6fb11-146">A posição de saída registra.</span><span class="sxs-lookup"><span data-stu-id="6fb11-146">The output position registers.</span></span> <span data-ttu-id="6fb11-147">O valor é a posição no espaço de recorte homogêneo.</span><span class="sxs-lookup"><span data-stu-id="6fb11-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="6fb11-148">Esse valor deve ser gravado pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6fb11-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="6fb11-149">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-149">Vertex shader versions</span></span> | <span data-ttu-id="6fb11-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fb11-150">1\_1</span></span> | <span data-ttu-id="6fb11-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-151">2\_0</span></span> | <span data-ttu-id="6fb11-152">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-152">2\_sw</span></span> | <span data-ttu-id="6fb11-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fb11-153">2\_x</span></span> | <span data-ttu-id="6fb11-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-154">3\_0</span></span> | <span data-ttu-id="6fb11-155">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fb11-156">Registro de posição</span><span class="sxs-lookup"><span data-stu-id="6fb11-156">Position Register</span></span>      | <span data-ttu-id="6fb11-157">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-157">x</span></span>    | <span data-ttu-id="6fb11-158">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-158">x</span></span>    | <span data-ttu-id="6fb11-159">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-159">x</span></span>     | <span data-ttu-id="6fb11-160">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="6fb11-161">Registro de tamanho de ponto – opta</span><span class="sxs-lookup"><span data-stu-id="6fb11-161">Point Size Register - oPts</span></span>

<span data-ttu-id="6fb11-162">O tamanho do ponto de saída é registrado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-162">The output point-size registers.</span></span> <span data-ttu-id="6fb11-163">Somente o componente x escalar do tamanho do ponto é usado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="6fb11-164">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-164">Vertex shader versions</span></span> | <span data-ttu-id="6fb11-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fb11-165">1\_1</span></span> | <span data-ttu-id="6fb11-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-166">2\_0</span></span> | <span data-ttu-id="6fb11-167">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-167">2\_sw</span></span> | <span data-ttu-id="6fb11-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fb11-168">2\_x</span></span> | <span data-ttu-id="6fb11-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-169">3\_0</span></span> | <span data-ttu-id="6fb11-170">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fb11-171">Registro de tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="6fb11-171">Point Size Register</span></span>    | <span data-ttu-id="6fb11-172">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-172">x</span></span>    | <span data-ttu-id="6fb11-173">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-173">x</span></span>    | <span data-ttu-id="6fb11-174">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-174">x</span></span>     | <span data-ttu-id="6fb11-175">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="6fb11-176">Registro de coordenadas de textura-oT0 para oT7</span><span class="sxs-lookup"><span data-stu-id="6fb11-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="6fb11-177">As coordenadas de textura de saída são registradas.</span><span class="sxs-lookup"><span data-stu-id="6fb11-177">The output texture coordinates registers.</span></span> <span data-ttu-id="6fb11-178">Especificamente, essas são uma matriz de registros de dados de saída que são iterados e usados como coordenadas de textura pelos estágios de amostragem de texturas que encaminham dados para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6fb11-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="6fb11-179">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-179">Vertex shader versions</span></span>      | <span data-ttu-id="6fb11-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fb11-180">1\_1</span></span> | <span data-ttu-id="6fb11-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-181">2\_0</span></span> | <span data-ttu-id="6fb11-182">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-182">2\_sw</span></span> | <span data-ttu-id="6fb11-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fb11-183">2\_x</span></span> | <span data-ttu-id="6fb11-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fb11-184">3\_0</span></span> | <span data-ttu-id="6fb11-185">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fb11-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fb11-186">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="6fb11-186">Texture Coordinate Register</span></span> | <span data-ttu-id="6fb11-187">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-187">x</span></span>    | <span data-ttu-id="6fb11-188">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-188">x</span></span>    | <span data-ttu-id="6fb11-189">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-189">x</span></span>     | <span data-ttu-id="6fb11-190">x</span><span class="sxs-lookup"><span data-stu-id="6fb11-190">x</span></span>    |      |       |



 

<span data-ttu-id="6fb11-191">Ao gravar em um registro de coordenadas de textura, é recomendável passar apenas o número de valores de ponto flutuante como a dimensão do mapa de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6fb11-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="6fb11-192">Controle os valores passados com um modificador.</span><span class="sxs-lookup"><span data-stu-id="6fb11-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="6fb11-193">Por exemplo, use. XY para um mapa de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="6fb11-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="6fb11-194">Quando a projeção de textura está habilitada para um estágio de textura, todos os quatro valores de ponto flutuante devem ser gravados no registro de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6fb11-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="6fb11-195">Qualquer um dos \* sinalizadores de transformação de textura D3DTTFF deve ser zero quando o pipeline programável está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="6fb11-196">Intervalo de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="6fb11-196">Texture Coordinate Range</span></span>

<span data-ttu-id="6fb11-197">Dados de vértice de objeto fornecem coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="6fb11-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="6fb11-198">Os objetos que não usavam texturas com ladrilhos normalmente têm coordenadas de textura no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="6fb11-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="6fb11-199">Os objetos que usam texturas de lado, como o terreno, normalmente têm coordenadas de textura que variam de \[ -?, +? \] onde?</span><span class="sxs-lookup"><span data-stu-id="6fb11-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="6fb11-200">pode ser um número de ponto flutuante grande.</span><span class="sxs-lookup"><span data-stu-id="6fb11-200">can be a large floating point number.</span></span>

<span data-ttu-id="6fb11-201">A interpolação de coordenadas de textura é executada em dados de vértice para rasterização.</span><span class="sxs-lookup"><span data-stu-id="6fb11-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="6fb11-202">Durante a rasterização, as coordenadas de textura são interpoladas entre os vértices de objeto, modificadas pelo encapsulamento de textura e dimensionadas pelo tamanho da textura (também levando em conta o modo de endereço de textura) para produzir um índice inteiro.</span><span class="sxs-lookup"><span data-stu-id="6fb11-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="6fb11-203">Em seguida, o índice é usado para executar uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="6fb11-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="6fb11-204">MaxTextureRepeat pode ser usado para determinar quantas vezes uma textura pode ser colocada lado a lado.</span><span class="sxs-lookup"><span data-stu-id="6fb11-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="6fb11-205">Se as coordenadas de textura forem lidas diretamente em um sombreador de pixel (usando texcoord ou texcrd), o intervalo de coordenadas de textura dependerá da instrução e da versão do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6fb11-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fb11-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6fb11-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb11-207">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fb11-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




