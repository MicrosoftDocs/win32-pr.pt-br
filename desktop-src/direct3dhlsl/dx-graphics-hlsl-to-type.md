---
title: Objeto de textura
description: No Direct3D 10, você especifica os exemplos e as texturas de forma independente; a amostragem de textura é implementada usando um objeto de textura de modelo. Este objeto de textura de modelo tem um formato específico, retorna um tipo específico e implementa vários métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objeto de textura HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172899"
---
# <a name="texture-object"></a><span data-ttu-id="dec80-105">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="dec80-105">Texture Object</span></span>

<span data-ttu-id="dec80-106">No Direct3D 10, você especifica os exemplos e as texturas de forma independente; a amostragem de textura é implementada usando um objeto de textura de modelo.</span><span class="sxs-lookup"><span data-stu-id="dec80-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="dec80-107">Este objeto de textura de modelo tem um formato específico, retorna um tipo específico e implementa vários métodos.</span><span class="sxs-lookup"><span data-stu-id="dec80-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec80-108">Diferenças entre o Direct3D9 e o Direct3D10: no Direct3D 9, os exemplos são associados a texturas específicas; no Direct3D 10, as texturas e os exemplos são objetos independentes.</span><span class="sxs-lookup"><span data-stu-id="dec80-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="dec80-109">Cada objeto modelo-Texture implementa métodos de amostragem de textura que usam a textura e a amostra como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="dec80-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="dec80-110">Aqui está a sintaxe para criar todos os objetos de textura (exceto objetos com uma amostra).</span><span class="sxs-lookup"><span data-stu-id="dec80-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="dec80-111">Nome do \[ < *tipo* de Object1 > \] ;</span><span class="sxs-lookup"><span data-stu-id="dec80-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="dec80-112">Os objetos com várias amostras (Texture2DMS e Texture2DMSArray) exigem que o tamanho da textura seja explicitamente declarado e expresso como o número de amostras.</span><span class="sxs-lookup"><span data-stu-id="dec80-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="dec80-113">\[ < *Tipo de Object2, nome de amostra* > \] ;</span><span class="sxs-lookup"><span data-stu-id="dec80-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="dec80-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dec80-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dec80-115">Item</span><span class="sxs-lookup"><span data-stu-id="dec80-115">Item</span></span></th>
<th><span data-ttu-id="dec80-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dec80-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dec80-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="dec80-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="dec80-118">Um objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-118">A texture object.</span></span> <span data-ttu-id="dec80-119">Deve ser um dos tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="dec80-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dec80-120">Tipo de Object1</span><span class="sxs-lookup"><span data-stu-id="dec80-120">Object1 Type</span></span></th>
<th><span data-ttu-id="dec80-121">Description</span><span class="sxs-lookup"><span data-stu-id="dec80-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dec80-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="dec80-122">Buffer</span></span></td>
<td><span data-ttu-id="dec80-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="dec80-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec80-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="dec80-124">Texture1D</span></span></td>
<td><span data-ttu-id="dec80-125">textura 1D</span><span class="sxs-lookup"><span data-stu-id="dec80-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec80-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="dec80-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="dec80-127">Matriz de texturas 1D</span><span class="sxs-lookup"><span data-stu-id="dec80-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec80-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="dec80-128">Texture2D</span></span></td>
<td><span data-ttu-id="dec80-129">textura 2D</span><span class="sxs-lookup"><span data-stu-id="dec80-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec80-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="dec80-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="dec80-131">Matriz de texturas 2D</span><span class="sxs-lookup"><span data-stu-id="dec80-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec80-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="dec80-132">Texture3D</span></span></td>
<td><span data-ttu-id="dec80-133">textura 3D</span><span class="sxs-lookup"><span data-stu-id="dec80-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec80-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="dec80-134">TextureCube</span></span></td>
<td><span data-ttu-id="dec80-135">Textura do cubo</span><span class="sxs-lookup"><span data-stu-id="dec80-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec80-136">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="dec80-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="dec80-137">Matriz de texturas de cubo</span><span class="sxs-lookup"><span data-stu-id="dec80-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec80-138">Tipo de Object2</span><span class="sxs-lookup"><span data-stu-id="dec80-138">Object2 Type</span></span></td>
<td><span data-ttu-id="dec80-139">Description</span><span class="sxs-lookup"><span data-stu-id="dec80-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec80-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="dec80-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="dec80-141">textura de multiamostras 2D</span><span class="sxs-lookup"><span data-stu-id="dec80-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec80-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dec80-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="dec80-143">Matriz de texturas com multiamostragens 2D</span><span class="sxs-lookup"><span data-stu-id="dec80-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="dec80-144">O tipo de buffer oferece suporte à maioria dos métodos de objeto de textura, exceto GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="dec80-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="dec80-145">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="dec80-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="dec80-146">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="dec80-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec80-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Escreva</em></span><span class="sxs-lookup"><span data-stu-id="dec80-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="dec80-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dec80-148">Optional.</span></span> <span data-ttu-id="dec80-149">Qualquer tipo de <a href="dx-graphics-hlsl-scalar.md">HLSL escalar</a> ou <a href="dx-graphics-hlsl-vector.md"><strong>tipo de HLSL de vetor</strong></a>, entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="dec80-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="dec80-150">O tipo padrão é <strong>FLOAT4</strong>.</span><span class="sxs-lookup"><span data-stu-id="dec80-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dec80-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nomes</em></span><span class="sxs-lookup"><span data-stu-id="dec80-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="dec80-152">Uma cadeia de caracteres ASCII que especifica o nome do objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dec80-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Amostras</em></span><span class="sxs-lookup"><span data-stu-id="dec80-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="dec80-154">O número de amostras (intervalos entre 1 e 128).</span><span class="sxs-lookup"><span data-stu-id="dec80-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="dec80-155">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dec80-155">Example 1</span></span>

<span data-ttu-id="dec80-156">Aqui está um exemplo de declaração de um objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="dec80-157">Métodos de objeto de textura</span><span class="sxs-lookup"><span data-stu-id="dec80-157">Texture Object Methods</span></span>

<span data-ttu-id="dec80-158">Cada objeto de textura implementa determinados métodos; Aqui está a tabela que lista todos os métodos.</span><span class="sxs-lookup"><span data-stu-id="dec80-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="dec80-159">Consulte a página de referência para cada método para ver quais objetos podem usar esse método.</span><span class="sxs-lookup"><span data-stu-id="dec80-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="dec80-160">Método de textura</span><span class="sxs-lookup"><span data-stu-id="dec80-160">Texture Method</span></span>                                                                     | <span data-ttu-id="dec80-161">Description</span><span class="sxs-lookup"><span data-stu-id="dec80-161">Description</span></span>                                                                                                       | <span data-ttu-id="dec80-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dec80-162">vs\_4\_0</span></span> | <span data-ttu-id="dec80-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dec80-163">vs\_4\_1</span></span>  | <span data-ttu-id="dec80-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dec80-164">ps\_4\_0</span></span> | <span data-ttu-id="dec80-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dec80-165">ps\_4\_1</span></span>  | <span data-ttu-id="dec80-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dec80-166">gs\_4\_0</span></span> | <span data-ttu-id="dec80-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dec80-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="dec80-168">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="dec80-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="dec80-169">Calcule o LOD, retorne um resultado de clamped.</span><span class="sxs-lookup"><span data-stu-id="dec80-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="dec80-170">x</span><span class="sxs-lookup"><span data-stu-id="dec80-170">x</span></span>         |          |           |
| [<span data-ttu-id="dec80-171">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="dec80-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="dec80-172">Calcule o LOD, retorne um resultado de unclamped.</span><span class="sxs-lookup"><span data-stu-id="dec80-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="dec80-173">x</span><span class="sxs-lookup"><span data-stu-id="dec80-173">x</span></span>         |          |           |
| [<span data-ttu-id="dec80-174">Gather</span><span class="sxs-lookup"><span data-stu-id="dec80-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="dec80-175">Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="dec80-176">x</span><span class="sxs-lookup"><span data-stu-id="dec80-176">x</span></span>         |          | <span data-ttu-id="dec80-177">x</span><span class="sxs-lookup"><span data-stu-id="dec80-177">x</span></span>         |          | <span data-ttu-id="dec80-178">x</span><span class="sxs-lookup"><span data-stu-id="dec80-178">x</span></span>         |
| [<span data-ttu-id="dec80-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="dec80-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="dec80-180">Obter a dimensão de textura para um nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="dec80-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="dec80-181">x</span><span class="sxs-lookup"><span data-stu-id="dec80-181">x</span></span>        | <span data-ttu-id="dec80-182">x</span><span class="sxs-lookup"><span data-stu-id="dec80-182">x</span></span>         | <span data-ttu-id="dec80-183">x</span><span class="sxs-lookup"><span data-stu-id="dec80-183">x</span></span>        | <span data-ttu-id="dec80-184">x</span><span class="sxs-lookup"><span data-stu-id="dec80-184">x</span></span>         | <span data-ttu-id="dec80-185">x</span><span class="sxs-lookup"><span data-stu-id="dec80-185">x</span></span>        | <span data-ttu-id="dec80-186">x</span><span class="sxs-lookup"><span data-stu-id="dec80-186">x</span></span>         |
| [<span data-ttu-id="dec80-187">GetDimensions (multiamostra)</span><span class="sxs-lookup"><span data-stu-id="dec80-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="dec80-188">Obter a dimensão de textura para um nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="dec80-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="dec80-189">x</span><span class="sxs-lookup"><span data-stu-id="dec80-189">x</span></span>         |          | <span data-ttu-id="dec80-190">x</span><span class="sxs-lookup"><span data-stu-id="dec80-190">x</span></span>         |          | <span data-ttu-id="dec80-191">x</span><span class="sxs-lookup"><span data-stu-id="dec80-191">x</span></span>         |
| [<span data-ttu-id="dec80-192">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="dec80-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="dec80-193">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="dec80-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="dec80-194">x</span><span class="sxs-lookup"><span data-stu-id="dec80-194">x</span></span>         |          | <span data-ttu-id="dec80-195">x</span><span class="sxs-lookup"><span data-stu-id="dec80-195">x</span></span>         |          | <span data-ttu-id="dec80-196">x</span><span class="sxs-lookup"><span data-stu-id="dec80-196">x</span></span>         |
| [<span data-ttu-id="dec80-197">Carregar</span><span class="sxs-lookup"><span data-stu-id="dec80-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="dec80-198">Carregar dados sem nenhuma filtragem ou amostragem.</span><span class="sxs-lookup"><span data-stu-id="dec80-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="dec80-199">x</span><span class="sxs-lookup"><span data-stu-id="dec80-199">x</span></span>        | <span data-ttu-id="dec80-200">x</span><span class="sxs-lookup"><span data-stu-id="dec80-200">x</span></span>         | <span data-ttu-id="dec80-201">x</span><span class="sxs-lookup"><span data-stu-id="dec80-201">x</span></span>        | <span data-ttu-id="dec80-202">x</span><span class="sxs-lookup"><span data-stu-id="dec80-202">x</span></span>         | <span data-ttu-id="dec80-203">x</span><span class="sxs-lookup"><span data-stu-id="dec80-203">x</span></span>        | <span data-ttu-id="dec80-204">x</span><span class="sxs-lookup"><span data-stu-id="dec80-204">x</span></span>         |
| [<span data-ttu-id="dec80-205">Carregar (multiamostrar)</span><span class="sxs-lookup"><span data-stu-id="dec80-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="dec80-206">Carregar dados sem nenhuma filtragem ou amostragem.</span><span class="sxs-lookup"><span data-stu-id="dec80-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="dec80-207">x</span><span class="sxs-lookup"><span data-stu-id="dec80-207">x</span></span>         | <span data-ttu-id="dec80-208">x</span><span class="sxs-lookup"><span data-stu-id="dec80-208">x</span></span>        | <span data-ttu-id="dec80-209">x</span><span class="sxs-lookup"><span data-stu-id="dec80-209">x</span></span>         |          | <span data-ttu-id="dec80-210">x</span><span class="sxs-lookup"><span data-stu-id="dec80-210">x</span></span>         |
| [<span data-ttu-id="dec80-211">Amostra</span><span class="sxs-lookup"><span data-stu-id="dec80-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="dec80-212">Amostra de uma textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="dec80-213">x</span><span class="sxs-lookup"><span data-stu-id="dec80-213">x</span></span>        | <span data-ttu-id="dec80-214">x</span><span class="sxs-lookup"><span data-stu-id="dec80-214">x</span></span>         |          |           |
| [<span data-ttu-id="dec80-215">SampleBias</span><span class="sxs-lookup"><span data-stu-id="dec80-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="dec80-216">Exemplo de textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="dec80-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="dec80-217">x</span><span class="sxs-lookup"><span data-stu-id="dec80-217">x</span></span>        | <span data-ttu-id="dec80-218">x</span><span class="sxs-lookup"><span data-stu-id="dec80-218">x</span></span>         |          |           |
| [<span data-ttu-id="dec80-219">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="dec80-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="dec80-220">Amostra de uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="dec80-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="dec80-221">x</span><span class="sxs-lookup"><span data-stu-id="dec80-221">x</span></span>        | <span data-ttu-id="dec80-222">x</span><span class="sxs-lookup"><span data-stu-id="dec80-222">x</span></span>         |          |           |
| [<span data-ttu-id="dec80-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="dec80-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="dec80-224">Amostra de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="dec80-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="dec80-225">x</span><span class="sxs-lookup"><span data-stu-id="dec80-225">x</span></span>        | <span data-ttu-id="dec80-226">x</span><span class="sxs-lookup"><span data-stu-id="dec80-226">x</span></span>         | <span data-ttu-id="dec80-227">x</span><span class="sxs-lookup"><span data-stu-id="dec80-227">x</span></span>        | <span data-ttu-id="dec80-228">x</span><span class="sxs-lookup"><span data-stu-id="dec80-228">x</span></span>         | <span data-ttu-id="dec80-229">x</span><span class="sxs-lookup"><span data-stu-id="dec80-229">x</span></span>        | <span data-ttu-id="dec80-230">x</span><span class="sxs-lookup"><span data-stu-id="dec80-230">x</span></span>         |
| [<span data-ttu-id="dec80-231">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="dec80-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="dec80-232">Exemplo de uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="dec80-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="dec80-233">x</span><span class="sxs-lookup"><span data-stu-id="dec80-233">x</span></span>        | <span data-ttu-id="dec80-234">x</span><span class="sxs-lookup"><span data-stu-id="dec80-234">x</span></span>         | <span data-ttu-id="dec80-235">x</span><span class="sxs-lookup"><span data-stu-id="dec80-235">x</span></span>        | <span data-ttu-id="dec80-236">x</span><span class="sxs-lookup"><span data-stu-id="dec80-236">x</span></span>         | <span data-ttu-id="dec80-237">x</span><span class="sxs-lookup"><span data-stu-id="dec80-237">x</span></span>        | <span data-ttu-id="dec80-238">x</span><span class="sxs-lookup"><span data-stu-id="dec80-238">x</span></span>         |
| [<span data-ttu-id="dec80-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="dec80-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="dec80-240">Exemplo de uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="dec80-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="dec80-241">x</span><span class="sxs-lookup"><span data-stu-id="dec80-241">x</span></span>        | <span data-ttu-id="dec80-242">x</span><span class="sxs-lookup"><span data-stu-id="dec80-242">x</span></span>         | <span data-ttu-id="dec80-243">x</span><span class="sxs-lookup"><span data-stu-id="dec80-243">x</span></span>        | <span data-ttu-id="dec80-244">x</span><span class="sxs-lookup"><span data-stu-id="dec80-244">x</span></span>         | <span data-ttu-id="dec80-245">x</span><span class="sxs-lookup"><span data-stu-id="dec80-245">x</span></span>        | <span data-ttu-id="dec80-246">x</span><span class="sxs-lookup"><span data-stu-id="dec80-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="dec80-247">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="dec80-247">Return Type</span></span>

<span data-ttu-id="dec80-248">O tipo de retorno de um método de objeto de textura é FLOAT4, a menos que especificado de outra forma, com exceção dos objetos de textura com alias multiamostrados que sempre precisam do tipo e da contagem de amostras especificadas.</span><span class="sxs-lookup"><span data-stu-id="dec80-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="dec80-249">O tipo de retorno é o mesmo que o tipo de recurso de textura ([**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="dec80-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="dec80-250">Em outras palavras, pode ser qualquer um dos tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="dec80-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="dec80-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="dec80-251">Type</span></span>                       | <span data-ttu-id="dec80-252">Description</span><span class="sxs-lookup"><span data-stu-id="dec80-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec80-253">FLOAT</span><span class="sxs-lookup"><span data-stu-id="dec80-253">float</span></span>                      | <span data-ttu-id="dec80-254">32-bit float (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="dec80-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="dec80-255">INT</span><span class="sxs-lookup"><span data-stu-id="dec80-255">int</span></span>                        | <span data-ttu-id="dec80-256">Inteiro com sinal de 32 bits</span><span class="sxs-lookup"><span data-stu-id="dec80-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="dec80-257">unsigned int</span><span class="sxs-lookup"><span data-stu-id="dec80-257">unsigned int</span></span>               | <span data-ttu-id="dec80-258">Inteiro sem sinal de 32 bits</span><span class="sxs-lookup"><span data-stu-id="dec80-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="dec80-259">snorm</span><span class="sxs-lookup"><span data-stu-id="dec80-259">snorm</span></span>                      | <span data-ttu-id="dec80-260">32-bit float no intervalo de 1 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="dec80-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="dec80-261">unorm</span><span class="sxs-lookup"><span data-stu-id="dec80-261">unorm</span></span>                      | <span data-ttu-id="dec80-262">32-bit float no intervalo de 0 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="dec80-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="dec80-263">qualquer tipo ou struct de textura</span><span class="sxs-lookup"><span data-stu-id="dec80-263">any texture type or struct</span></span> | <span data-ttu-id="dec80-264">O número de componentes retornados deve estar entre 1 e 3, inclusive.</span><span class="sxs-lookup"><span data-stu-id="dec80-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="dec80-265">Além disso, o tipo de retorno pode ser qualquer tipo de textura, incluindo uma estrutura, mas deve ser inferior a 4 componentes, como um tipo float1 que retorna um componente.</span><span class="sxs-lookup"><span data-stu-id="dec80-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="dec80-266">Valores padrão para componentes ausentes em uma textura</span><span class="sxs-lookup"><span data-stu-id="dec80-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="dec80-267">O valor padrão para componentes ausentes em um tipo de recurso de textura é zero para qualquer componente, exceto o componente alfa (A); o valor padrão para o que está faltando é um.</span><span class="sxs-lookup"><span data-stu-id="dec80-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="dec80-268">A maneira que ele aparece para o sombreador depende do tipo de recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="dec80-269">Ele assume a forma do primeiro componente tipado que está realmente presente no tipo de recurso de textura (a partir da esquerda na ordem RGBA).</span><span class="sxs-lookup"><span data-stu-id="dec80-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="dec80-270">Se esse formulário for UNORM ou FLOAT, o valor padrão para o que está faltando é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="dec80-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="dec80-271">Se o formulário for Santo ou UINT, o valor padrão para a ausente é 0x1.</span><span class="sxs-lookup"><span data-stu-id="dec80-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="dec80-272">Por exemplo, quando um sombreador lê [**o \_ formato dxgi \_ R24 \_ UNORM \_ x8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) tipo de recurso de textura sem tipos, os valores padrão para G e B são zero e o valor padrão de a é 1,0 f; quando um sombreador lê o tipo de recurso de textura [**R16G16 do \_ formato \_ \_ dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , o valor padrão de B é zero e o valor padrão de a é 0x00000001; quando um sombreador lê o tipo de recurso de textura de [**\_ formato dxgi \_ R16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , os valores padrão para G e B são zero e o valor padrão de a é 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="dec80-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="dec80-273">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dec80-273">Example 2</span></span>

<span data-ttu-id="dec80-274">Aqui está um exemplo de amostragem de textura usando um método de textura.</span><span class="sxs-lookup"><span data-stu-id="dec80-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="dec80-275">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="dec80-275">Minimum Shader Model</span></span>

<span data-ttu-id="dec80-276">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dec80-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="dec80-277">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="dec80-277">Shader Model</span></span>                                                        | <span data-ttu-id="dec80-278">Com suporte</span><span class="sxs-lookup"><span data-stu-id="dec80-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="dec80-279">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="dec80-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="dec80-280">sim</span><span class="sxs-lookup"><span data-stu-id="dec80-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dec80-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec80-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec80-282">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dec80-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

