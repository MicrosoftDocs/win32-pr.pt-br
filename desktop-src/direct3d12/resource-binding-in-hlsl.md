---
title: Associação de recursos em HLSL
description: Este tópico descreve alguns recursos específicos do uso do modelo de sombreador HLSL (High Level Shader Language) 5.1 com o Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550381"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="61ea6-103">Associação de recursos em HLSL</span><span class="sxs-lookup"><span data-stu-id="61ea6-103">Resource binding in HLSL</span></span>

<span data-ttu-id="61ea6-104">Este tópico descreve alguns recursos específicos do uso do modelo de sombreador HLSL (High Level Shader Language) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) com o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="61ea6-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="61ea6-105">Todo o hardware do Direct3D 12 dá suporte ao Modelo de Sombreador 5.1, portanto, o suporte para esse modelo não depende de qual é o nível do recurso de hardware.</span><span class="sxs-lookup"><span data-stu-id="61ea6-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="61ea6-106">Tipos de recursos e matrizes</span><span class="sxs-lookup"><span data-stu-id="61ea6-106">Resource types and arrays</span></span>

<span data-ttu-id="61ea6-107">A sintaxe de recurso do Modelo de Sombreador 5 (SM5.0) usa a palavra-chave para retransmitir informações importantes sobre o recurso para o `register` compilador HLSL.</span><span class="sxs-lookup"><span data-stu-id="61ea6-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="61ea6-108">Por exemplo, a instrução a seguir declara uma matriz de quatro texturas vinculadas aos slots t3, t4, t5 e t6.</span><span class="sxs-lookup"><span data-stu-id="61ea6-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="61ea6-109">t3 é o único slot de registro que aparece na instrução , simplesmente sendo o primeiro na matriz de quatro.</span><span class="sxs-lookup"><span data-stu-id="61ea6-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="61ea6-110">A sintaxe de recurso do Modelo de Sombreador 5.1 (SM5.1) no HLSL é baseada na sintaxe de recurso de registro existente, para permitir a portação mais fácil.</span><span class="sxs-lookup"><span data-stu-id="61ea6-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="61ea6-111">Os recursos do Direct3D 12 no HLSL estão vinculados a registros virtuais em espaços de registro lógicos:</span><span class="sxs-lookup"><span data-stu-id="61ea6-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="61ea6-112">t – para SRV (exibições de recurso de sombreador)</span><span class="sxs-lookup"><span data-stu-id="61ea6-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="61ea6-113">s – para amostras</span><span class="sxs-lookup"><span data-stu-id="61ea6-113">s – for samplers</span></span>
-   <span data-ttu-id="61ea6-114">u – para exibições de acesso não organizado (UAV)</span><span class="sxs-lookup"><span data-stu-id="61ea6-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="61ea6-115">b – para exibições de buffer constante (CBV)</span><span class="sxs-lookup"><span data-stu-id="61ea6-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="61ea6-116">A assinatura raiz que referencia o sombreador deve ser compatível com os slots de registro declarados.</span><span class="sxs-lookup"><span data-stu-id="61ea6-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="61ea6-117">Por exemplo, a parte a seguir de uma assinatura raiz seria compatível com o uso de slots de textura t3 a t6, pois descreve uma tabela de descritor com slots t0 a t98.</span><span class="sxs-lookup"><span data-stu-id="61ea6-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="61ea6-118">Uma declaração de recurso pode ser escalar, uma matriz 1D ou uma matriz multidimensional:</span><span class="sxs-lookup"><span data-stu-id="61ea6-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="61ea6-119">O SM5.1 usa os mesmos tipos de recursos e tipos de elemento que o SM5.0.</span><span class="sxs-lookup"><span data-stu-id="61ea6-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="61ea6-120">Os limites de declaração SM5.1 são mais flexíveis e restritos somente pelos limites de runtime/hardware.</span><span class="sxs-lookup"><span data-stu-id="61ea6-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="61ea6-121">A `space` palavra-chave especifica a qual espaço de registro lógico a variável declarada está associada.</span><span class="sxs-lookup"><span data-stu-id="61ea6-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="61ea6-122">Se a `space` palavra-chave for omitida, o índice de espaço padrão 0 será atribuído implicitamente ao intervalo (de modo que o `tex2` intervalo acima resida `space0` ).</span><span class="sxs-lookup"><span data-stu-id="61ea6-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="61ea6-123">`register(t3,  space0)` Nunca entrará em conflito com `register(t3,  space1)` , nem com nenhuma matriz em outro espaço que possa incluir T3.</span><span class="sxs-lookup"><span data-stu-id="61ea6-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="61ea6-124">Um recurso de matriz pode ter um tamanho não associado, que é declarado especificando a primeira dimensão como vazia ou 0:</span><span class="sxs-lookup"><span data-stu-id="61ea6-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="61ea6-125">A tabela de descritores de correspondência pode ser:</span><span class="sxs-lookup"><span data-stu-id="61ea6-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="61ea6-126">Uma matriz não associada em HLSL corresponde a um número fixo definido com `numDescriptors` na tabela de descritores e um tamanho fixo em HLSL corresponde a uma declaração não associada na tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="61ea6-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="61ea6-127">Matrizes multidimensionais são permitidas, incluindo um tamanho não associado.</span><span class="sxs-lookup"><span data-stu-id="61ea6-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="61ea6-128">Essas matrizes multidimensionais são achatadas no espaço de registro.</span><span class="sxs-lookup"><span data-stu-id="61ea6-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="61ea6-129">Não é permitido alias de intervalos de recursos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="61ea6-130">Em outras palavras, para cada tipo de recurso (t, s, u, b), os intervalos de registro declarados não deve se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="61ea6-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="61ea6-131">Isso também inclui intervalos não associados.</span><span class="sxs-lookup"><span data-stu-id="61ea6-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="61ea6-132">Intervalos declarados em espaços de registro diferentes nunca se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="61ea6-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="61ea6-133">Observe que o não associado `tex2` (acima) reside no `space0` , embora `tex3` não esteja associado `space1` , de modo que eles não se sobreponham.</span><span class="sxs-lookup"><span data-stu-id="61ea6-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="61ea6-134">O acesso a recursos que foram declarados como matrizes é tão simples quanto indexá-los.</span><span class="sxs-lookup"><span data-stu-id="61ea6-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="61ea6-135">Há uma restrição padrão importante no uso dos índices ( `myMaterialID` e `samplerID` no código acima), pois eles não têm permissão para variar em uma [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="61ea6-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="61ea6-136">Mesmo alterando o índice com base em contagens de instâncias como variáveis.</span><span class="sxs-lookup"><span data-stu-id="61ea6-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="61ea6-137">Se a variação do índice for necessária, especifique o `NonUniformResourceIndex` qualificador no índice, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="61ea6-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="61ea6-138">Em alguns hardwares, o uso desse qualificador gera código adicional para impor a exatidão (incluindo entre threads), mas com um custo de desempenho secundário.</span><span class="sxs-lookup"><span data-stu-id="61ea6-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="61ea6-139">Se um índice for alterado sem esse qualificador e dentro de um empate/expedição, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="61ea6-140">Matrizes de descritores e matrizes de textura</span><span class="sxs-lookup"><span data-stu-id="61ea6-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="61ea6-141">As matrizes de textura estão disponíveis desde o DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="61ea6-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="61ea6-142">As matrizes de textura exigem um descritor, no entanto, todas as fatias de matriz devem compartilhar o mesmo formato, largura, altura e contagem de mip.</span><span class="sxs-lookup"><span data-stu-id="61ea6-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="61ea6-143">Além disso, a matriz deve ocupar um intervalo contíguo no espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="61ea6-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="61ea6-144">O código a seguir mostra um exemplo de acesso a uma matriz de textura de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="61ea6-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="61ea6-145">Em uma matriz de textura, o índice pode ser variado livremente, sem a necessidade de qualificadores como `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="61ea6-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="61ea6-146">A matriz de descritor equivalente seria:</span><span class="sxs-lookup"><span data-stu-id="61ea6-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="61ea6-147">Observe que o uso estranho de um float para o índice de matriz é substituído por `myArrayOfTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="61ea6-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="61ea6-148">As matrizes de descritor também oferecem mais flexibilidade com as dimensões.</span><span class="sxs-lookup"><span data-stu-id="61ea6-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="61ea6-149">O tipo , é este exemplo, não pode variar, mas o formato, a largura, a altura e a contagem de mip podem variar com `Texture2D` cada descritor.</span><span class="sxs-lookup"><span data-stu-id="61ea6-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="61ea6-150">É legítimo ter uma matriz de descritor de matrizes de textura:</span><span class="sxs-lookup"><span data-stu-id="61ea6-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="61ea6-151">Não é legítimo declarar uma matriz de estruturas, cada estrutura que contém descritores, por exemplo, não há suporte para o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ea6-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="61ea6-152">Isso teria permitido o layout de memória **abcabcabc....**, mas é uma limitação de linguagem e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="61ea6-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="61ea6-153">Um método com suporte para fazer isso seria o seguinte, embora o layout de memória nesse caso seja **aaa... Bbb... ccc...**.</span><span class="sxs-lookup"><span data-stu-id="61ea6-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="61ea6-154">Para obter o layout **de memória abcabcabc....** , use uma tabela de descritor sem usar a `myStruct` estrutura .</span><span class="sxs-lookup"><span data-stu-id="61ea6-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="61ea6-155">Alias de recurso</span><span class="sxs-lookup"><span data-stu-id="61ea6-155">Resource aliasing</span></span>

<span data-ttu-id="61ea6-156">Os intervalos de recursos especificados nos sombreadores HLSL são intervalos lógicos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="61ea6-157">Eles são vinculados a intervalos de heap concretos em runtime por meio do mecanismo de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="61ea6-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="61ea6-158">Normalmente, um intervalo lógico é mapeado para um intervalo de heap que não se sobrepõe a outros intervalos de heap.</span><span class="sxs-lookup"><span data-stu-id="61ea6-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="61ea6-159">No entanto, o mecanismo de assinatura raiz possibilita o alias (sobreposição) de intervalos de heap de tipos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="61ea6-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="61ea6-160">Por exemplo, e os intervalos do exemplo acima podem ser mapeados para o mesmo intervalo de heap (ou sobreposição), que tem o efeito de suavizar texturas no programa `tex2` `tex3` HLSL.</span><span class="sxs-lookup"><span data-stu-id="61ea6-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="61ea6-161">Se tal alias for desejado, o sombreador deverá ser compilado com \_ \_ a opção de alias d3d10 Shader Resources \_ \_ , que é definida usando a opção */res de \_ \_ alias de maio* para a ferramenta de compilador de [efeito](../direct3dtools/fxc.md) (FXC).</span><span class="sxs-lookup"><span data-stu-id="61ea6-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC).</span></span> <span data-ttu-id="61ea6-162">A opção faz com que o compilador produza o código correto impedindo determinadas otimizações de carga/armazenamento sob a suposição de que os recursos podem ser alias.</span><span class="sxs-lookup"><span data-stu-id="61ea6-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="61ea6-163">Divergência e derivações</span><span class="sxs-lookup"><span data-stu-id="61ea6-163">Divergence and derivatives</span></span>

<span data-ttu-id="61ea6-164">O SM 5.1 não impõe limitações no índice de recursos; ou seja, ` tex2[idx].Sample(…)` – o índice Idx pode ser uma constante literal, uma constante CBuffer ou um valor interpolado.</span><span class="sxs-lookup"><span data-stu-id="61ea6-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="61ea6-165">Embora o modelo de programação ofereça uma grande flexibilidade, há problemas a serem considerados:</span><span class="sxs-lookup"><span data-stu-id="61ea6-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="61ea6-166">Se o índice divergir em um quad, as quantidades derivadas e derivados de hardware computadas, como LOD, poderão ser indefinidas.</span><span class="sxs-lookup"><span data-stu-id="61ea6-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="61ea6-167">O compilador HLSL também faz o melhor esforço para emitir um aviso nesse caso, mas não impedirá que um sombreador seja compilado.</span><span class="sxs-lookup"><span data-stu-id="61ea6-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="61ea6-168">Esse comportamento é semelhante à computação de derivações no fluxo de controle divergente.</span><span class="sxs-lookup"><span data-stu-id="61ea6-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="61ea6-169">Se o índice de recursos for divergente, o desempenho será reduzido em comparação com o caso de um índice uniforme, pois o hardware precisa executar operações em vários recursos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="61ea6-170">Os índices de recursos que podem ser divergentes devem ser marcados com a `NonUniformResourceIndex` função no código HLSL.</span><span class="sxs-lookup"><span data-stu-id="61ea6-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="61ea6-171">Caso contrário, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="61ea6-172">UAVs em sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="61ea6-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="61ea6-173">O SM 5.1 não impõe restrições em intervalos de UAV em sombreadores de pixel como foi o caso do SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="61ea6-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="61ea6-174">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="61ea6-174">Constant Buffers</span></span>

<span data-ttu-id="61ea6-175">A sintaxe de CBuffer (buffers de constantes) do SM 5.1 foi alterada do SM 5.0 para permitir que os desenvolvedores indexem buffers constantes.</span><span class="sxs-lookup"><span data-stu-id="61ea6-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="61ea6-176">Para habilitar buffers constantes indexáveis, o SM 5.1 apresenta a `ConstantBuffer` construção "template":</span><span class="sxs-lookup"><span data-stu-id="61ea6-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="61ea6-177">O código anterior declara a variável de buffer constante `myCB1` do tipo `Foo` e do tamanho 6, e uma variável de buffer escalar e constante `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="61ea6-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="61ea6-178">Uma variável de buffer constante agora pode ser indexada no sombreador como:</span><span class="sxs-lookup"><span data-stu-id="61ea6-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="61ea6-179">Os campos ' a ' e ' b ' não se tornam variáveis globais, mas, em vez disso, devem ser tratados como campos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="61ea6-180">Para compatibilidade com versões anteriores, o SM 5.1 dá suporte ao conceito antigo de CBuffer para cbuffers escalar.</span><span class="sxs-lookup"><span data-stu-id="61ea6-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="61ea6-181">A instrução a seguir torna 'a' e 'b' variáveis globais somente leitura, como no SM5.0.</span><span class="sxs-lookup"><span data-stu-id="61ea6-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="61ea6-182">No entanto, um cbuffer de estilo antigo não pode ser indexável.</span><span class="sxs-lookup"><span data-stu-id="61ea6-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="61ea6-183">Atualmente, o compilador de sombreador dá suporte ao `ConstantBuffer` modelo apenas para estruturas definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61ea6-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="61ea6-184">Por motivos de compatibilidade, o compilador HLSL pode atribuir automaticamente registros de recursos para intervalos declarados no `space0` .</span><span class="sxs-lookup"><span data-stu-id="61ea6-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="61ea6-185">Se 'space' for omitido na cláusula register, o padrão `space0` será usado.</span><span class="sxs-lookup"><span data-stu-id="61ea6-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="61ea6-186">O compilador usa a heurística first-hole-fits para atribuir os registros.</span><span class="sxs-lookup"><span data-stu-id="61ea6-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="61ea6-187">A atribuição pode ser recuperada por meio da  API de reflexão, que foi estendida para adicionar o campo Espaço para espaço, enquanto o campo *BindPoint* indica o limite inferior do intervalo de registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="61ea6-188">Alterações de código de byte no SM5.1</span><span class="sxs-lookup"><span data-stu-id="61ea6-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="61ea6-189">O SM5.1 altera como os registros de recursos são declarados e referenciados nas instruções.</span><span class="sxs-lookup"><span data-stu-id="61ea6-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="61ea6-190">A sintaxe envolve declarar uma "variável" de registro, semelhante a como ela é feita para registros de memória compartilhada de grupo:</span><span class="sxs-lookup"><span data-stu-id="61ea6-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="61ea6-191">Isso será desmontado para:</span><span class="sxs-lookup"><span data-stu-id="61ea6-191">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="61ea6-192">Cada intervalo de recursos do sombreador agora tem uma ID (um nome) que é exclusiva para o código de byte do sombreador.</span><span class="sxs-lookup"><span data-stu-id="61ea6-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="61ea6-193">Por exemplo, a matriz de textura tex1 (t10) torna-se 'T1' no código de byte do sombreador.</span><span class="sxs-lookup"><span data-stu-id="61ea6-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="61ea6-194">A aplicação de IDs exclusivas para cada intervalo de recursos permite duas coisas:</span><span class="sxs-lookup"><span data-stu-id="61ea6-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="61ea6-195">Identifique sem ambígua qual intervalo de recursos (consulte dcl resource texture2d) está sendo indexado em uma instrução \_ \_ (consulte a instrução de exemplo).</span><span class="sxs-lookup"><span data-stu-id="61ea6-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="61ea6-196">Anexar um conjunto de atributos à declaração, por exemplo, o tipo de elemento, o tamanho do stride, o modo de operação de raster etc.</span><span class="sxs-lookup"><span data-stu-id="61ea6-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="61ea6-197">Observe que a ID do intervalo não está relacionada à declaração de limite inferior HLSL.</span><span class="sxs-lookup"><span data-stu-id="61ea6-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="61ea6-198">A ordem das vinculações de recursos de reflexão (listagem na parte superior) e instruções de declaração do sombreador (dcl ) é a mesma para ajudar a identificar a correspondência entre \_ variáveis HLSL e IDs de código de \* byte.</span><span class="sxs-lookup"><span data-stu-id="61ea6-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="61ea6-199">Cada instrução de declaração no SM5.1 usa um operand 3D para definir: ID de intervalo, limites inferiores e superiores.</span><span class="sxs-lookup"><span data-stu-id="61ea6-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="61ea6-200">Um token adicional é emitido para especificar o espaço de registro.</span><span class="sxs-lookup"><span data-stu-id="61ea6-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="61ea6-201">Outros tokens podem ser emitidos também para transmitir propriedades adicionais do intervalo, por exemplo, CBuffer ou instrução de declaração de buffer estruturado emite o tamanho do CBuffer ou da estrutura.</span><span class="sxs-lookup"><span data-stu-id="61ea6-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="61ea6-202">Os detalhes exatos da codificação podem ser encontrados em d3d12TokenizedProgramFormat. h e **D3D10ShaderBinary:: CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="61ea6-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="61ea6-203">As instruções do SM 5.1 não emitirão informações adicionais do operando de recurso como parte da instrução (como no SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="61ea6-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="61ea6-204">Essas informações agora estão nas instruções da declaração.</span><span class="sxs-lookup"><span data-stu-id="61ea6-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="61ea6-205">No SM 5.0, as instruções de indexação de recursos exigiam atributos de recurso a serem descritos em tokens de opcode estendidos, já que a indexação ofusca a associação à declaração.</span><span class="sxs-lookup"><span data-stu-id="61ea6-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="61ea6-206">No SM 5.1, cada ID (como ' t 1 ') é associada sem ambigüidade a uma única declaração que descreve as informações de recursos necessárias.</span><span class="sxs-lookup"><span data-stu-id="61ea6-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="61ea6-207">Portanto, os tokens de opcode estendidos usados em instruções para descrever as informações de recursos não são mais emitidos.</span><span class="sxs-lookup"><span data-stu-id="61ea6-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="61ea6-208">Em instruções de não declaração, um operando de recurso para amostras, SRVs e UAVs é um operando 2D.</span><span class="sxs-lookup"><span data-stu-id="61ea6-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="61ea6-209">O primeiro índice é uma constante literal que especifica a ID do intervalo.</span><span class="sxs-lookup"><span data-stu-id="61ea6-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="61ea6-210">O segundo índice representa o valor linear do índice.</span><span class="sxs-lookup"><span data-stu-id="61ea6-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="61ea6-211">O valor é calculado em relação ao início do espaço de registro correspondente (não relativo ao início do intervalo lógico) para correlacionar melhor com a assinatura raiz e para reduzir a carga do compilador de driver de ajustar o índice.</span><span class="sxs-lookup"><span data-stu-id="61ea6-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="61ea6-212">Um operando de recurso para CBVs é um operando 3D, contendo: ID literal do intervalo, índice do buffer de constantes, offset na instância específica do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="61ea6-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="61ea6-213">Declarações HLSL de exemplo</span><span class="sxs-lookup"><span data-stu-id="61ea6-213">Example HLSL Declarations</span></span>

<span data-ttu-id="61ea6-214">Os programas HLSL não precisam saber nada sobre assinaturas raiz.</span><span class="sxs-lookup"><span data-stu-id="61ea6-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="61ea6-215">Eles podem atribuir associações ao espaço de associação virtual "Register", t \# para SRVs, u \# para UAVs, b \# para CBVs, s \# para amostragens ou dependem do compilador para selecionar atribuições (e consultar os mapeamentos resultantes usando a reflexão do sombreador posteriormente).</span><span class="sxs-lookup"><span data-stu-id="61ea6-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="61ea6-216">As tabelas de descritores de mapeamentos de assinatura raiz e as constantes raiz para esse espaço de registro virtual.</span><span class="sxs-lookup"><span data-stu-id="61ea6-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="61ea6-217">A seguir estão alguns exemplos de declarações que um sombreador HLSL pode ter.</span><span class="sxs-lookup"><span data-stu-id="61ea6-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="61ea6-218">Observe que não há referências a assinaturas raiz ou tabelas de descritor.</span><span class="sxs-lookup"><span data-stu-id="61ea6-218">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="61ea6-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61ea6-219">Related topics</span></span>

* [<span data-ttu-id="61ea6-220">Indexação dinâmica usando HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="61ea6-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="61ea6-221">Ferramenta Effect-Compiler</span><span class="sxs-lookup"><span data-stu-id="61ea6-221">Effect-Compiler Tool</span></span>](../direct3dtools/fxc.md)
* [<span data-ttu-id="61ea6-222">Recursos do HLSL Shader Model 5.1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="61ea6-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [<span data-ttu-id="61ea6-223">Modos de exibição ordenados do rasterizador</span><span class="sxs-lookup"><span data-stu-id="61ea6-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="61ea6-224">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="61ea6-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="61ea6-225">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="61ea6-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="61ea6-226">Modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="61ea6-226">Shader Model 5.1</span></span>](../direct3dhlsl/shader-model-5-1.md)
* [<span data-ttu-id="61ea6-227">Valor de referência de estêncil especificado pelo sombreador</span><span class="sxs-lookup"><span data-stu-id="61ea6-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="61ea6-228">Como especificar assinaturas raiz no HLSL</span><span class="sxs-lookup"><span data-stu-id="61ea6-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)