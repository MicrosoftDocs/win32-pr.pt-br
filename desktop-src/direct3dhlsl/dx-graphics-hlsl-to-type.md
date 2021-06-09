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
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825766"
---
# <a name="texture-object"></a><span data-ttu-id="810cb-105">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="810cb-105">Texture Object</span></span>

<span data-ttu-id="810cb-106">No Direct3D 10, você especifica os exemplos e as texturas de forma independente; a amostragem de textura é implementada usando um objeto de textura de modelo.</span><span class="sxs-lookup"><span data-stu-id="810cb-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="810cb-107">Este objeto de textura de modelo tem um formato específico, retorna um tipo específico e implementa vários métodos.</span><span class="sxs-lookup"><span data-stu-id="810cb-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="810cb-108">Diferenças entre o Direct3D9 e o Direct3D10:</span><span class="sxs-lookup"><span data-stu-id="810cb-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="810cb-109">No Direct3D 9, os exemplos são associados a texturas específicas.</span><span class="sxs-lookup"><span data-stu-id="810cb-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="810cb-110">No Direct3D 10, as texturas e os exemplos são objetos independentes.</span><span class="sxs-lookup"><span data-stu-id="810cb-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="810cb-111">Cada objeto modelo-Texture implementa métodos de amostragem de textura que usam a textura e a amostra como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="810cb-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="810cb-112">Aqui está a sintaxe para criar todos os objetos de textura (exceto objetos com uma amostra).</span><span class="sxs-lookup"><span data-stu-id="810cb-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="810cb-113">Nome do \[ < *tipo* de Object1 > \] ;</span><span class="sxs-lookup"><span data-stu-id="810cb-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="810cb-114">Os objetos com várias amostras (Texture2DMS e Texture2DMSArray) exigem que o tamanho da textura seja explicitamente declarado e expresso como o número de amostras.</span><span class="sxs-lookup"><span data-stu-id="810cb-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="810cb-115">\[ < *Tipo de Object2, nome de amostra* > \] ;</span><span class="sxs-lookup"><span data-stu-id="810cb-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="810cb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="810cb-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="810cb-117">Item</span><span class="sxs-lookup"><span data-stu-id="810cb-117">Item</span></span></th>
<th><span data-ttu-id="810cb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="810cb-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="810cb-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="810cb-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="810cb-120">Um objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-120">A texture object.</span></span> <span data-ttu-id="810cb-121">Deve ser um dos tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="810cb-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="810cb-122">Tipo de Object1</span><span class="sxs-lookup"><span data-stu-id="810cb-122">Object1 Type</span></span></th>
<th><span data-ttu-id="810cb-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="810cb-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="810cb-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="810cb-124">Buffer</span></span></td>
<td><span data-ttu-id="810cb-125">Buffer</span><span class="sxs-lookup"><span data-stu-id="810cb-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="810cb-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="810cb-126">Texture1D</span></span></td>
<td><span data-ttu-id="810cb-127">textura 1D</span><span class="sxs-lookup"><span data-stu-id="810cb-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810cb-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="810cb-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="810cb-129">Matriz de texturas 1D</span><span class="sxs-lookup"><span data-stu-id="810cb-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810cb-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="810cb-130">Texture2D</span></span></td>
<td><span data-ttu-id="810cb-131">textura 2D</span><span class="sxs-lookup"><span data-stu-id="810cb-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810cb-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="810cb-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="810cb-133">Matriz de texturas 2D</span><span class="sxs-lookup"><span data-stu-id="810cb-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810cb-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="810cb-134">Texture3D</span></span></td>
<td><span data-ttu-id="810cb-135">textura 3D</span><span class="sxs-lookup"><span data-stu-id="810cb-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810cb-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="810cb-136">TextureCube</span></span></td>
<td><span data-ttu-id="810cb-137">Textura do cubo</span><span class="sxs-lookup"><span data-stu-id="810cb-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810cb-138">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="810cb-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="810cb-139">Matriz de texturas de cubo</span><span class="sxs-lookup"><span data-stu-id="810cb-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810cb-140">Tipo de Object2</span><span class="sxs-lookup"><span data-stu-id="810cb-140">Object2 Type</span></span></td>
<td><span data-ttu-id="810cb-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="810cb-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810cb-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="810cb-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="810cb-143">textura de multiamostras 2D</span><span class="sxs-lookup"><span data-stu-id="810cb-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810cb-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="810cb-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="810cb-145">Matriz de texturas com multiamostragens 2D</span><span class="sxs-lookup"><span data-stu-id="810cb-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="810cb-146">O tipo de buffer oferece suporte à maioria dos métodos de objeto de textura, exceto GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="810cb-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="810cb-147">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="810cb-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="810cb-148">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="810cb-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="810cb-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Escreva</em></span><span class="sxs-lookup"><span data-stu-id="810cb-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="810cb-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="810cb-150">Optional.</span></span> <span data-ttu-id="810cb-151">Qualquer tipo de <a href="dx-graphics-hlsl-scalar.md">HLSL escalar</a> ou <a href="dx-graphics-hlsl-vector.md"><strong>tipo de HLSL de vetor</strong></a>, entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="810cb-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="810cb-152">O tipo padrão é <strong>FLOAT4</strong>.</span><span class="sxs-lookup"><span data-stu-id="810cb-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="810cb-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nomes</em></span><span class="sxs-lookup"><span data-stu-id="810cb-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="810cb-154">Uma cadeia de caracteres ASCII que especifica o nome do objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="810cb-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Amostras</em></span><span class="sxs-lookup"><span data-stu-id="810cb-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="810cb-156">O número de amostras (intervalos entre 1 e 128).</span><span class="sxs-lookup"><span data-stu-id="810cb-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="810cb-157">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="810cb-157">Example 1</span></span>

<span data-ttu-id="810cb-158">Aqui está um exemplo de declaração de um objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="810cb-159">Métodos de objeto de textura</span><span class="sxs-lookup"><span data-stu-id="810cb-159">Texture Object Methods</span></span>

<span data-ttu-id="810cb-160">Cada objeto de textura implementa determinados métodos; Aqui está a tabela que lista todos os métodos.</span><span class="sxs-lookup"><span data-stu-id="810cb-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="810cb-161">Consulte a página de referência para cada método para ver quais objetos podem usar esse método.</span><span class="sxs-lookup"><span data-stu-id="810cb-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="810cb-162">Método de textura</span><span class="sxs-lookup"><span data-stu-id="810cb-162">Texture Method</span></span>                                                                     | <span data-ttu-id="810cb-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="810cb-163">Description</span></span>                                                                                                       | <span data-ttu-id="810cb-164">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="810cb-164">vs\_4\_0</span></span> | <span data-ttu-id="810cb-165">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="810cb-165">vs\_4\_1</span></span>  | <span data-ttu-id="810cb-166">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="810cb-166">ps\_4\_0</span></span> | <span data-ttu-id="810cb-167">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="810cb-167">ps\_4\_1</span></span>  | <span data-ttu-id="810cb-168">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="810cb-168">gs\_4\_0</span></span> | <span data-ttu-id="810cb-169">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="810cb-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="810cb-170">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="810cb-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="810cb-171">Calcule o LOD, retorne um resultado de clamped.</span><span class="sxs-lookup"><span data-stu-id="810cb-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="810cb-172">x</span><span class="sxs-lookup"><span data-stu-id="810cb-172">x</span></span>         |          |           |
| [<span data-ttu-id="810cb-173">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="810cb-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="810cb-174">Calcule o LOD, retorne um resultado de unclamped.</span><span class="sxs-lookup"><span data-stu-id="810cb-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="810cb-175">x</span><span class="sxs-lookup"><span data-stu-id="810cb-175">x</span></span>         |          |           |
| [<span data-ttu-id="810cb-176">Gather</span><span class="sxs-lookup"><span data-stu-id="810cb-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="810cb-177">Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="810cb-178">x</span><span class="sxs-lookup"><span data-stu-id="810cb-178">x</span></span>         |          | <span data-ttu-id="810cb-179">x</span><span class="sxs-lookup"><span data-stu-id="810cb-179">x</span></span>         |          | <span data-ttu-id="810cb-180">x</span><span class="sxs-lookup"><span data-stu-id="810cb-180">x</span></span>         |
| [<span data-ttu-id="810cb-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="810cb-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="810cb-182">Obter a dimensão de textura para um nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="810cb-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="810cb-183">x</span><span class="sxs-lookup"><span data-stu-id="810cb-183">x</span></span>        | <span data-ttu-id="810cb-184">x</span><span class="sxs-lookup"><span data-stu-id="810cb-184">x</span></span>         | <span data-ttu-id="810cb-185">x</span><span class="sxs-lookup"><span data-stu-id="810cb-185">x</span></span>        | <span data-ttu-id="810cb-186">x</span><span class="sxs-lookup"><span data-stu-id="810cb-186">x</span></span>         | <span data-ttu-id="810cb-187">x</span><span class="sxs-lookup"><span data-stu-id="810cb-187">x</span></span>        | <span data-ttu-id="810cb-188">x</span><span class="sxs-lookup"><span data-stu-id="810cb-188">x</span></span>         |
| [<span data-ttu-id="810cb-189">GetDimensions (multiamostra)</span><span class="sxs-lookup"><span data-stu-id="810cb-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="810cb-190">Obter a dimensão de textura para um nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="810cb-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="810cb-191">x</span><span class="sxs-lookup"><span data-stu-id="810cb-191">x</span></span>         |          | <span data-ttu-id="810cb-192">x</span><span class="sxs-lookup"><span data-stu-id="810cb-192">x</span></span>         |          | <span data-ttu-id="810cb-193">x</span><span class="sxs-lookup"><span data-stu-id="810cb-193">x</span></span>         |
| [<span data-ttu-id="810cb-194">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="810cb-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="810cb-195">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="810cb-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="810cb-196">x</span><span class="sxs-lookup"><span data-stu-id="810cb-196">x</span></span>         |          | <span data-ttu-id="810cb-197">x</span><span class="sxs-lookup"><span data-stu-id="810cb-197">x</span></span>         |          | <span data-ttu-id="810cb-198">x</span><span class="sxs-lookup"><span data-stu-id="810cb-198">x</span></span>         |
| [<span data-ttu-id="810cb-199">Carregar</span><span class="sxs-lookup"><span data-stu-id="810cb-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="810cb-200">Carregar dados sem nenhuma filtragem ou amostragem.</span><span class="sxs-lookup"><span data-stu-id="810cb-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="810cb-201">x</span><span class="sxs-lookup"><span data-stu-id="810cb-201">x</span></span>        | <span data-ttu-id="810cb-202">x</span><span class="sxs-lookup"><span data-stu-id="810cb-202">x</span></span>         | <span data-ttu-id="810cb-203">x</span><span class="sxs-lookup"><span data-stu-id="810cb-203">x</span></span>        | <span data-ttu-id="810cb-204">x</span><span class="sxs-lookup"><span data-stu-id="810cb-204">x</span></span>         | <span data-ttu-id="810cb-205">x</span><span class="sxs-lookup"><span data-stu-id="810cb-205">x</span></span>        | <span data-ttu-id="810cb-206">x</span><span class="sxs-lookup"><span data-stu-id="810cb-206">x</span></span>         |
| [<span data-ttu-id="810cb-207">Carregar (multiamostrar)</span><span class="sxs-lookup"><span data-stu-id="810cb-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="810cb-208">Carregar dados sem nenhuma filtragem ou amostragem.</span><span class="sxs-lookup"><span data-stu-id="810cb-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="810cb-209">x</span><span class="sxs-lookup"><span data-stu-id="810cb-209">x</span></span>         | <span data-ttu-id="810cb-210">x</span><span class="sxs-lookup"><span data-stu-id="810cb-210">x</span></span>        | <span data-ttu-id="810cb-211">x</span><span class="sxs-lookup"><span data-stu-id="810cb-211">x</span></span>         |          | <span data-ttu-id="810cb-212">x</span><span class="sxs-lookup"><span data-stu-id="810cb-212">x</span></span>         |
| [<span data-ttu-id="810cb-213">Amostra</span><span class="sxs-lookup"><span data-stu-id="810cb-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="810cb-214">Amostra de uma textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="810cb-215">x</span><span class="sxs-lookup"><span data-stu-id="810cb-215">x</span></span>        | <span data-ttu-id="810cb-216">x</span><span class="sxs-lookup"><span data-stu-id="810cb-216">x</span></span>         |          |           |
| [<span data-ttu-id="810cb-217">SampleBias</span><span class="sxs-lookup"><span data-stu-id="810cb-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="810cb-218">Exemplo de textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="810cb-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="810cb-219">x</span><span class="sxs-lookup"><span data-stu-id="810cb-219">x</span></span>        | <span data-ttu-id="810cb-220">x</span><span class="sxs-lookup"><span data-stu-id="810cb-220">x</span></span>         |          |           |
| [<span data-ttu-id="810cb-221">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="810cb-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="810cb-222">Amostra de uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="810cb-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="810cb-223">x</span><span class="sxs-lookup"><span data-stu-id="810cb-223">x</span></span>        | <span data-ttu-id="810cb-224">x</span><span class="sxs-lookup"><span data-stu-id="810cb-224">x</span></span>         |          |           |
| [<span data-ttu-id="810cb-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="810cb-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="810cb-226">Amostra de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="810cb-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="810cb-227">x</span><span class="sxs-lookup"><span data-stu-id="810cb-227">x</span></span>        | <span data-ttu-id="810cb-228">x</span><span class="sxs-lookup"><span data-stu-id="810cb-228">x</span></span>         | <span data-ttu-id="810cb-229">x</span><span class="sxs-lookup"><span data-stu-id="810cb-229">x</span></span>        | <span data-ttu-id="810cb-230">x</span><span class="sxs-lookup"><span data-stu-id="810cb-230">x</span></span>         | <span data-ttu-id="810cb-231">x</span><span class="sxs-lookup"><span data-stu-id="810cb-231">x</span></span>        | <span data-ttu-id="810cb-232">x</span><span class="sxs-lookup"><span data-stu-id="810cb-232">x</span></span>         |
| [<span data-ttu-id="810cb-233">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="810cb-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="810cb-234">Exemplo de uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="810cb-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="810cb-235">x</span><span class="sxs-lookup"><span data-stu-id="810cb-235">x</span></span>        | <span data-ttu-id="810cb-236">x</span><span class="sxs-lookup"><span data-stu-id="810cb-236">x</span></span>         | <span data-ttu-id="810cb-237">x</span><span class="sxs-lookup"><span data-stu-id="810cb-237">x</span></span>        | <span data-ttu-id="810cb-238">x</span><span class="sxs-lookup"><span data-stu-id="810cb-238">x</span></span>         | <span data-ttu-id="810cb-239">x</span><span class="sxs-lookup"><span data-stu-id="810cb-239">x</span></span>        | <span data-ttu-id="810cb-240">x</span><span class="sxs-lookup"><span data-stu-id="810cb-240">x</span></span>         |
| [<span data-ttu-id="810cb-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="810cb-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="810cb-242">Exemplo de uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="810cb-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="810cb-243">x</span><span class="sxs-lookup"><span data-stu-id="810cb-243">x</span></span>        | <span data-ttu-id="810cb-244">x</span><span class="sxs-lookup"><span data-stu-id="810cb-244">x</span></span>         | <span data-ttu-id="810cb-245">x</span><span class="sxs-lookup"><span data-stu-id="810cb-245">x</span></span>        | <span data-ttu-id="810cb-246">x</span><span class="sxs-lookup"><span data-stu-id="810cb-246">x</span></span>         | <span data-ttu-id="810cb-247">x</span><span class="sxs-lookup"><span data-stu-id="810cb-247">x</span></span>        | <span data-ttu-id="810cb-248">x</span><span class="sxs-lookup"><span data-stu-id="810cb-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="810cb-249">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="810cb-249">Return Type</span></span>

<span data-ttu-id="810cb-250">O tipo de retorno de um método de objeto de textura é FLOAT4, a menos que especificado de outra forma, com exceção dos objetos de textura com alias multiamostrados que sempre precisam do tipo e da contagem de amostras especificadas.</span><span class="sxs-lookup"><span data-stu-id="810cb-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="810cb-251">O tipo de retorno é o mesmo que o tipo de recurso de textura ([**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="810cb-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="810cb-252">Em outras palavras, pode ser qualquer um dos tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="810cb-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="810cb-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="810cb-253">Type</span></span>                       | <span data-ttu-id="810cb-254">Descrição</span><span class="sxs-lookup"><span data-stu-id="810cb-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810cb-255">FLOAT</span><span class="sxs-lookup"><span data-stu-id="810cb-255">float</span></span>                      | <span data-ttu-id="810cb-256">32-bit float (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="810cb-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="810cb-257">INT</span><span class="sxs-lookup"><span data-stu-id="810cb-257">int</span></span>                        | <span data-ttu-id="810cb-258">Inteiro com sinal de 32 bits</span><span class="sxs-lookup"><span data-stu-id="810cb-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="810cb-259">unsigned int</span><span class="sxs-lookup"><span data-stu-id="810cb-259">unsigned int</span></span>               | <span data-ttu-id="810cb-260">Inteiro sem sinal de 32 bits</span><span class="sxs-lookup"><span data-stu-id="810cb-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="810cb-261">snorm</span><span class="sxs-lookup"><span data-stu-id="810cb-261">snorm</span></span>                      | <span data-ttu-id="810cb-262">32-bit float no intervalo de 1 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="810cb-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="810cb-263">unorm</span><span class="sxs-lookup"><span data-stu-id="810cb-263">unorm</span></span>                      | <span data-ttu-id="810cb-264">32-bit float no intervalo de 0 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="810cb-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="810cb-265">qualquer tipo ou struct de textura</span><span class="sxs-lookup"><span data-stu-id="810cb-265">any texture type or struct</span></span> | <span data-ttu-id="810cb-266">O número de componentes retornados deve estar entre 1 e 3, inclusive.</span><span class="sxs-lookup"><span data-stu-id="810cb-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="810cb-267">Além disso, o tipo de retorno pode ser qualquer tipo de textura, incluindo uma estrutura, mas deve ser inferior a 4 componentes, como um tipo float1 que retorna um componente.</span><span class="sxs-lookup"><span data-stu-id="810cb-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="810cb-268">Valores padrão para componentes ausentes em uma textura</span><span class="sxs-lookup"><span data-stu-id="810cb-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="810cb-269">O valor padrão para componentes ausentes em um tipo de recurso de textura é zero para qualquer componente, exceto o componente alfa (A); o valor padrão para o que está faltando é um.</span><span class="sxs-lookup"><span data-stu-id="810cb-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="810cb-270">A maneira que ele aparece para o sombreador depende do tipo de recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="810cb-271">Ele assume a forma do primeiro componente tipado que está realmente presente no tipo de recurso de textura (a partir da esquerda na ordem RGBA).</span><span class="sxs-lookup"><span data-stu-id="810cb-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="810cb-272">Se esse formulário for UNORM ou FLOAT, o valor padrão para o que está faltando é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="810cb-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="810cb-273">Se o formulário for Santo ou UINT, o valor padrão para a ausente é 0x1.</span><span class="sxs-lookup"><span data-stu-id="810cb-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="810cb-274">Por exemplo, quando um sombreador lê [**o \_ formato dxgi \_ R24 \_ UNORM \_ x8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) tipo de recurso de textura sem tipos, os valores padrão para G e B são zero e o valor padrão de a é 1,0 f; quando um sombreador lê o tipo de recurso de textura [**R16G16 do \_ formato \_ \_ dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , o valor padrão de B é zero e o valor padrão de a é 0x00000001; quando um sombreador lê o tipo de recurso de textura de [**\_ formato dxgi \_ R16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , os valores padrão para G e B são zero e o valor padrão de a é 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="810cb-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="810cb-275">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="810cb-275">Example 2</span></span>

<span data-ttu-id="810cb-276">Aqui está um exemplo de amostragem de textura usando um método de textura.</span><span class="sxs-lookup"><span data-stu-id="810cb-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="810cb-277">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="810cb-277">Minimum Shader Model</span></span>

<span data-ttu-id="810cb-278">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="810cb-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="810cb-279">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="810cb-279">Shader Model</span></span>                                                        | <span data-ttu-id="810cb-280">Com suporte</span><span class="sxs-lookup"><span data-stu-id="810cb-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="810cb-281">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="810cb-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="810cb-282">sim</span><span class="sxs-lookup"><span data-stu-id="810cb-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="810cb-283">Confira também</span><span class="sxs-lookup"><span data-stu-id="810cb-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810cb-284">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="810cb-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

