---
title: GetDimensions (objeto de textura DirectX HLSL)
description: Obtém informações de tamanho da textura. O bloco de sintaxe mostra todos os parâmetros que são possíveis na declaração do método. A tabela na seção de comentários mostra quais parâmetros são implementados para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823442"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="bdb7d-105">GetDimensions (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bdb7d-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="bdb7d-106">Obtém informações de tamanho da textura.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-106">Gets texture size information.</span></span> <span data-ttu-id="bdb7d-107">O bloco de sintaxe mostra todos os parâmetros que são possíveis na declaração do método.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="bdb7d-108">A tabela na seção de comentários mostra quais parâmetros são implementados para cada tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb7d-109">void Object. GetDimensions (UINT MipLevel, largura de typeX, altura de typeX, elementos typeX, profundidade de typeX, typeX NumberOfLevels, typeX NumberOfSamples);</span><span class="sxs-lookup"><span data-stu-id="bdb7d-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="bdb7d-110">typeX denota que há dois tipos possíveis: **uint** ou **float**.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdb7d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdb7d-111">Parameters</span></span>



| <span data-ttu-id="bdb7d-112">Item</span><span class="sxs-lookup"><span data-stu-id="bdb7d-112">Item</span></span>                                                                                                                               | <span data-ttu-id="bdb7d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdb7d-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb7d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="bdb7d-115">Qualquer tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) , exceto um objeto de **buffer** .</span><span class="sxs-lookup"><span data-stu-id="bdb7d-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="bdb7d-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="bdb7d-117">\[em \] um índice de base zero que identifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="bdb7d-118">Se esse argumento não for usado, o primeiro nível de MIP será assumido.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="bdb7d-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Largura*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="bdb7d-120">\[fora \] da largura da textura, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="bdb7d-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Tamanho*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="bdb7d-122">\[fora \] da altura da textura, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="bdb7d-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementos*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="bdb7d-124">\[\]o número de elementos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="bdb7d-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Detalhado*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="bdb7d-126">\[\]a profundidade da textura, em texels.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="bdb7d-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="bdb7d-128">\[\]o número de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="bdb7d-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="bdb7d-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="bdb7d-130">\[\]o número de amostras.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="bdb7d-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bdb7d-131">Return Value</span></span>

<span data-ttu-id="bdb7d-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdb7d-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="bdb7d-133">Métodos sobrecarregados</span><span class="sxs-lookup"><span data-stu-id="bdb7d-133">Overloaded Methods</span></span>

<span data-ttu-id="bdb7d-134">Esta tabela lista todas as versões diferentes do método; as versões são diferentes pelo número de parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="bdb7d-135">Observe que, para cada método que usa parâmetros inteiros, há um método sobrecarregado que usa parâmetros de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="bdb7d-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bdb7d-136">Texture-Object Type</span></span> | <span data-ttu-id="bdb7d-137">Parâmetros de Entrada</span><span class="sxs-lookup"><span data-stu-id="bdb7d-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bdb7d-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-138">Texture1D</span></span>           | <span data-ttu-id="bdb7d-139">UINT MipLevel, largura UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="bdb7d-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-140">Texture1D</span></span>           | <span data-ttu-id="bdb7d-141">Largura de UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="bdb7d-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-142">Texture1D</span></span>           | <span data-ttu-id="bdb7d-143">UINT MipLevel, largura flutuante, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="bdb7d-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-144">Texture1D</span></span>           | <span data-ttu-id="bdb7d-145">Largura flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-145">float Width</span></span>                                                                    |
| <span data-ttu-id="bdb7d-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-146">Texture1DArray</span></span>      | <span data-ttu-id="bdb7d-147">UINT MipLevel, largura UINT, elementos UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="bdb7d-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-148">Texture1DArray</span></span>      | <span data-ttu-id="bdb7d-149">Elementos de largura UINT, UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="bdb7d-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-150">Texture1DArray</span></span>      | <span data-ttu-id="bdb7d-151">UINT MipLevel, largura flutuante, elementos float, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="bdb7d-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-152">Texture1DArray</span></span>      | <span data-ttu-id="bdb7d-153">Largura flutuante, elementos float</span><span class="sxs-lookup"><span data-stu-id="bdb7d-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="bdb7d-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-154">Texture2D</span></span>           | <span data-ttu-id="bdb7d-155">UINT MipLevel, largura UINT, altura UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="bdb7d-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-156">Texture2D</span></span>           | <span data-ttu-id="bdb7d-157">Largura UINT, altura UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="bdb7d-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-158">Texture2D</span></span>           | <span data-ttu-id="bdb7d-159">UINT MipLevel, largura de flutuação, altura flutuante, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="bdb7d-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-160">Texture2D</span></span>           | <span data-ttu-id="bdb7d-161">Largura flutuante, altura flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="bdb7d-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-162">Texture2DArray</span></span>      | <span data-ttu-id="bdb7d-163">UINT MipLevel, largura UINT, altura UINT, elementos UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="bdb7d-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-164">Texture2DArray</span></span>      | <span data-ttu-id="bdb7d-165">Largura de UINT, altura UINT, elementos UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="bdb7d-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-166">Texture2DArray</span></span>      | <span data-ttu-id="bdb7d-167">UINT MipLevel, largura flutuante, altura flutuante, elementos float, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="bdb7d-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-168">Texture2DArray</span></span>      | <span data-ttu-id="bdb7d-169">Largura float, altura flutuante, elementos float</span><span class="sxs-lookup"><span data-stu-id="bdb7d-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="bdb7d-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-170">Texture3D</span></span>           | <span data-ttu-id="bdb7d-171">UINT MipLevel, largura UINT, altura UINT, profundidade UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="bdb7d-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-172">Texture3D</span></span>           | <span data-ttu-id="bdb7d-173">Largura UINT, altura UINT, profundidade de UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="bdb7d-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-174">Texture3D</span></span>           | <span data-ttu-id="bdb7d-175">UINT MipLevel, largura flutuante, altura flutuante, profundidade flutuante, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="bdb7d-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bdb7d-176">Texture3D</span></span>           | <span data-ttu-id="bdb7d-177">Largura de flutuação, altura flutuante, profundidade de flutuação</span><span class="sxs-lookup"><span data-stu-id="bdb7d-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="bdb7d-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bdb7d-178">TextureCube</span></span>         | <span data-ttu-id="bdb7d-179">UINT MipLevel, largura UINT, altura UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="bdb7d-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bdb7d-180">TextureCube</span></span>         | <span data-ttu-id="bdb7d-181">Largura UINT, altura UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="bdb7d-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bdb7d-182">TextureCube</span></span>         | <span data-ttu-id="bdb7d-183">UINT MipLevel, largura flutuante, altura flutuante, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="bdb7d-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="bdb7d-184">TextureCube</span></span>         | <span data-ttu-id="bdb7d-185">Largura flutuante, altura flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="bdb7d-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-186">TextureCubeArray</span></span>    | <span data-ttu-id="bdb7d-187">UINT MipLevel, largura UINT, altura UINT, elementos UINT, NumberOfLevels UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="bdb7d-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-188">TextureCubeArray</span></span>    | <span data-ttu-id="bdb7d-189">Largura de UINT, altura UINT, elementos UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="bdb7d-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-190">TextureCubeArray</span></span>    | <span data-ttu-id="bdb7d-191">UINT MipLevel, largura flutuante, altura flutuante, elementos float, NumberOfLevels flutuante</span><span class="sxs-lookup"><span data-stu-id="bdb7d-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="bdb7d-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-192">TextureCubeArray</span></span>    | <span data-ttu-id="bdb7d-193">Largura float, altura flutuante, elementos float</span><span class="sxs-lookup"><span data-stu-id="bdb7d-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="bdb7d-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="bdb7d-194">Texture2DMS</span></span>         | <span data-ttu-id="bdb7d-195">Largura UINT, altura UINT, amostras UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="bdb7d-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="bdb7d-196">Texture2DMS</span></span>         | <span data-ttu-id="bdb7d-197">Largura float, altura float, amostras float</span><span class="sxs-lookup"><span data-stu-id="bdb7d-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="bdb7d-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-198">Texture2DMSArray</span></span>    | <span data-ttu-id="bdb7d-199">Largura UINT, altura UINT, elementos UINT, amostras UINT</span><span class="sxs-lookup"><span data-stu-id="bdb7d-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="bdb7d-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="bdb7d-200">Texture2DMSArray</span></span>    | <span data-ttu-id="bdb7d-201">Largura float, altura float, elementos float, amostras float</span><span class="sxs-lookup"><span data-stu-id="bdb7d-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bdb7d-202">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bdb7d-202">Minimum Shader Model</span></span>

<span data-ttu-id="bdb7d-203">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bdb7d-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bdb7d-204">vs\_4\_0</span></span> | <span data-ttu-id="bdb7d-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdb7d-205">vs\_4\_1</span></span>  | <span data-ttu-id="bdb7d-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bdb7d-206">ps\_4\_0</span></span> | <span data-ttu-id="bdb7d-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdb7d-207">ps\_4\_1</span></span>  | <span data-ttu-id="bdb7d-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bdb7d-208">gs\_4\_0</span></span> | <span data-ttu-id="bdb7d-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdb7d-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="bdb7d-210">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-210">x</span></span>        | <span data-ttu-id="bdb7d-211">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-211">x</span></span>         | <span data-ttu-id="bdb7d-212">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-212">x</span></span>        | <span data-ttu-id="bdb7d-213">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-213">x</span></span>         | <span data-ttu-id="bdb7d-214">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-214">x</span></span>        | <span data-ttu-id="bdb7d-215">x</span><span class="sxs-lookup"><span data-stu-id="bdb7d-215">x</span></span>         |



 

1.  <span data-ttu-id="bdb7d-216">Retorna dimensões para o maior nível de mipmap (inicial).</span><span class="sxs-lookup"><span data-stu-id="bdb7d-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="bdb7d-217">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="bdb7d-218">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="bdb7d-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdb7d-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdb7d-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb7d-220">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="bdb7d-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





