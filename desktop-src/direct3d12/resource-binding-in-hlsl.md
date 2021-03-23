---
title: Associação de recursos em HLSL
description: Este tópico descreve alguns recursos específicos do usando o modelo de sombreador HLSL (sombreamento de alto nível) 5,1 com o Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548278"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="87549-103">Associação de recursos em HLSL</span><span class="sxs-lookup"><span data-stu-id="87549-103">Resource binding in HLSL</span></span>

<span data-ttu-id="87549-104">Este tópico descreve alguns recursos específicos do usando o [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (sombreamento de alto nível) 5,1 com o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="87549-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="87549-105">Todo o hardware do Direct3D 12 dá suporte ao modelo de sombreador 5,1, portanto, o suporte para esse modelo não depende do nível de recurso de hardware.</span><span class="sxs-lookup"><span data-stu-id="87549-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="87549-106">Tipos de recursos e matrizes</span><span class="sxs-lookup"><span data-stu-id="87549-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="87549-107">Matrizes de descritores e matrizes de textura</span><span class="sxs-lookup"><span data-stu-id="87549-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="87549-108">Alias de recurso</span><span class="sxs-lookup"><span data-stu-id="87549-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="87549-109">Divergência e derivações</span><span class="sxs-lookup"><span data-stu-id="87549-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="87549-110">UAVs em sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="87549-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="87549-111">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="87549-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="87549-112">Alterações de código de bytes no SM 5.1</span><span class="sxs-lookup"><span data-stu-id="87549-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="87549-113">Declarações HLSL de exemplo</span><span class="sxs-lookup"><span data-stu-id="87549-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="87549-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87549-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="87549-115">Tipos de recursos e matrizes</span><span class="sxs-lookup"><span data-stu-id="87549-115">Resource types and arrays</span></span>

<span data-ttu-id="87549-116">A sintaxe de recurso do Shader Model 5 (SM 5.0) usa a `register` palavra-chave para retransmitir informações importantes sobre o recurso para o compilador HLSL.</span><span class="sxs-lookup"><span data-stu-id="87549-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="87549-117">Por exemplo, a instrução a seguir declara uma matriz de quatro texturas associadas a Slots T3, T4, T5 e T6.</span><span class="sxs-lookup"><span data-stu-id="87549-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="87549-118">T3 é o único slot de registro que aparece na instrução, simplesmente sendo o primeiro na matriz de quatro.</span><span class="sxs-lookup"><span data-stu-id="87549-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="87549-119">A sintaxe de recurso do Shader Model 5,1 (SM 5.1) no HLSL é baseada na sintaxe de recurso de registro existente, para permitir portabilidade mais fácil.</span><span class="sxs-lookup"><span data-stu-id="87549-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="87549-120">Os recursos do Direct3D 12 no HLSL estão associados a registros virtuais em espaços de registro lógico:</span><span class="sxs-lookup"><span data-stu-id="87549-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="87549-121">t – para exibições de recurso do sombreador (SRV)</span><span class="sxs-lookup"><span data-stu-id="87549-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="87549-122">s – para exemplos</span><span class="sxs-lookup"><span data-stu-id="87549-122">s – for samplers</span></span>
-   <span data-ttu-id="87549-123">u – para exibições de acesso não ordenado (UAV)</span><span class="sxs-lookup"><span data-stu-id="87549-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="87549-124">b – para exibições de buffer de constantes (CBV)</span><span class="sxs-lookup"><span data-stu-id="87549-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="87549-125">A assinatura raiz que faz referência ao sombreador deve ser compatível com os slots de registro declarados.</span><span class="sxs-lookup"><span data-stu-id="87549-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="87549-126">Por exemplo, a seguinte parte de uma assinatura raiz seria compatível com o uso de Slots de textura T3 por meio de T6, pois descreve uma tabela de descritores com slots T0 a T98.</span><span class="sxs-lookup"><span data-stu-id="87549-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="87549-127">Uma declaração de recurso pode ser escalar, uma matriz 1D ou uma matriz multidimensional:</span><span class="sxs-lookup"><span data-stu-id="87549-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="87549-128">O SM 5.1 usa os mesmos tipos de recursos e tipos de elementos que o SM 5.0 faz.</span><span class="sxs-lookup"><span data-stu-id="87549-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="87549-129">Os limites de declaração SM 5.1 são mais flexíveis e restritos apenas pelos limites de tempo de execução/hardware.</span><span class="sxs-lookup"><span data-stu-id="87549-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="87549-130">A `space` palavra-chave especifica a qual espaço de registro lógico a variável declarada está associada.</span><span class="sxs-lookup"><span data-stu-id="87549-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="87549-131">Se a `space` palavra-chave for omitida, o índice de espaço padrão 0 será atribuído implicitamente ao intervalo (de modo que o `tex2` intervalo acima resida `space0` ).</span><span class="sxs-lookup"><span data-stu-id="87549-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="87549-132">`register(t3,  space0)` Nunca entrará em conflito com `register(t3,  space1)` , nem com nenhuma matriz em outro espaço que possa incluir T3.</span><span class="sxs-lookup"><span data-stu-id="87549-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="87549-133">Um recurso de matriz pode ter um tamanho não associado, que é declarado especificando a primeira dimensão como vazia ou 0:</span><span class="sxs-lookup"><span data-stu-id="87549-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="87549-134">A tabela de descritores de correspondência pode ser:</span><span class="sxs-lookup"><span data-stu-id="87549-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="87549-135">Uma matriz não associada em HLSL corresponde a um número fixo definido com `numDescriptors` na tabela de descritores e um tamanho fixo em HLSL corresponde a uma declaração não associada na tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="87549-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="87549-136">Matrizes multidimensionais são permitidas, incluindo um tamanho não associado.</span><span class="sxs-lookup"><span data-stu-id="87549-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="87549-137">Essas matrizes multidimensionais são achatadas no espaço de registro.</span><span class="sxs-lookup"><span data-stu-id="87549-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="87549-138">Não é permitido alias de intervalos de recursos.</span><span class="sxs-lookup"><span data-stu-id="87549-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="87549-139">Em outras palavras, para cada tipo de recurso (t, s, u, b), os intervalos de registro declarados não deve se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="87549-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="87549-140">Isso também inclui intervalos não associados.</span><span class="sxs-lookup"><span data-stu-id="87549-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="87549-141">Intervalos declarados em espaços de registro diferentes nunca se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="87549-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="87549-142">Observe que o não associado `tex2` (acima) reside no `space0` , embora `tex3` não esteja associado `space1` , de modo que eles não se sobreponham.</span><span class="sxs-lookup"><span data-stu-id="87549-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="87549-143">O acesso a recursos que foram declarados como matrizes é tão simples quanto indexá-los.</span><span class="sxs-lookup"><span data-stu-id="87549-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="87549-144">Há uma restrição padrão importante no uso dos índices ( `myMaterialID` e `samplerID` no código acima), pois eles não têm permissão para variar em uma [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="87549-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="87549-145">Mesmo alterando o índice com base em contagens de instâncias como variáveis.</span><span class="sxs-lookup"><span data-stu-id="87549-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="87549-146">Se a variação do índice for necessária, especifique o `NonUniformResourceIndex` qualificador no índice, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="87549-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="87549-147">Em alguns hardwares, o uso desse qualificador gera código adicional para impor a exatidão (incluindo entre threads), mas com um custo de desempenho secundário.</span><span class="sxs-lookup"><span data-stu-id="87549-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="87549-148">Se um índice for alterado sem esse qualificador e dentro de um empate/expedição, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="87549-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="87549-149">Matrizes de descritores e matrizes de textura</span><span class="sxs-lookup"><span data-stu-id="87549-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="87549-150">As matrizes de textura estão disponíveis desde o DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="87549-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="87549-151">As matrizes de textura exigem um descritor, no entanto, todas as fatias de matriz devem compartilhar o mesmo formato, largura, altura e contagem de MIP.</span><span class="sxs-lookup"><span data-stu-id="87549-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="87549-152">Além disso, a matriz deve ocupar um intervalo contíguo no espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="87549-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="87549-153">O código a seguir mostra um exemplo de como acessar uma matriz de textura de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="87549-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="87549-154">Em uma matriz de textura, o índice pode ser variado livremente, sem a necessidade de qualificadores como `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="87549-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="87549-155">A matriz de descritor equivalente seria:</span><span class="sxs-lookup"><span data-stu-id="87549-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="87549-156">Observe que o uso inadequado de um float para o índice de matriz é substituído por `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="87549-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="87549-157">Além disso, as matrizes de descritores oferecem mais flexibilidade com as dimensões.</span><span class="sxs-lookup"><span data-stu-id="87549-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="87549-158">O tipo, `Texture2D` é este exemplo, não pode variar, mas o formato, a largura, a altura e a contagem MIP podem variar com cada descritor.</span><span class="sxs-lookup"><span data-stu-id="87549-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="87549-159">É legítimo ter uma matriz de descritores de matrizes de textura:</span><span class="sxs-lookup"><span data-stu-id="87549-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="87549-160">Não é legítimo declarar uma matriz de estruturas, cada estrutura contendo descritores, por exemplo, o código a seguir não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="87549-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="87549-161">Isso teria permitido o layout de memória **abcabcabc..**., mas é uma limitação de idioma e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="87549-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="87549-162">Um método com suporte para fazer isso seria o seguinte, embora o layout de memória nesse caso seja **AAA... bbb... CCC...**</span><span class="sxs-lookup"><span data-stu-id="87549-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="87549-163">Para obter o layout **abcabcabc...** Memory, use uma tabela de descritor sem usar a `myStruct` estrutura.</span><span class="sxs-lookup"><span data-stu-id="87549-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="87549-164">Alias de recurso</span><span class="sxs-lookup"><span data-stu-id="87549-164">Resource aliasing</span></span>

<span data-ttu-id="87549-165">Os intervalos de recursos especificados nos sombreadores HLSL são intervalos lógicos.</span><span class="sxs-lookup"><span data-stu-id="87549-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="87549-166">Eles são associados a intervalos concretos de heap em tempo de execução por meio do mecanismo de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="87549-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="87549-167">Normalmente, um intervalo lógico é mapeado para um intervalo de heap que não se sobrepõe a outros intervalos de heap.</span><span class="sxs-lookup"><span data-stu-id="87549-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="87549-168">No entanto, o mecanismo de assinatura raiz torna possível o alias (sobreposição) de intervalos de heap de tipos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="87549-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="87549-169">Por exemplo, `tex2` e os `tex3` intervalos do exemplo acima podem ser mapeados para o mesmo intervalo de heap (ou sobreposição), que tem o efeito de texturas de alias no programa HLSL.</span><span class="sxs-lookup"><span data-stu-id="87549-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="87549-170">Se tal alias for desejado, o sombreador deverá ser compilado com \_ \_ a opção de alias d3d10 Shader Resources \_ \_ , que é definida usando a opção */res de \_ \_ alias de maio* para a ferramenta de compilador de [efeito](/windows/desktop/direct3dtools/fxc) (FXC).</span><span class="sxs-lookup"><span data-stu-id="87549-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="87549-171">A opção faz com que o compilador produza o código correto impedindo determinadas otimizações de carga/armazenamento sob a suposição de que os recursos podem ser alias.</span><span class="sxs-lookup"><span data-stu-id="87549-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="87549-172">Divergência e derivações</span><span class="sxs-lookup"><span data-stu-id="87549-172">Divergence and derivatives</span></span>

<span data-ttu-id="87549-173">O SM 5.1 não impõe limitações no índice de recursos; ou seja, ` tex2[idx].Sample(…)` – o índice Idx pode ser uma constante literal, uma constante CBuffer ou um valor interpolado.</span><span class="sxs-lookup"><span data-stu-id="87549-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="87549-174">Embora o modelo de programação ofereça uma grande flexibilidade, há problemas a serem considerados:</span><span class="sxs-lookup"><span data-stu-id="87549-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="87549-175">Se o índice divergir em um quad, as quantidades derivadas e derivados de hardware computadas, como LOD, poderão ser indefinidas.</span><span class="sxs-lookup"><span data-stu-id="87549-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="87549-176">O compilador HLSL também faz o melhor esforço para emitir um aviso nesse caso, mas não impedirá que um sombreador seja compilado.</span><span class="sxs-lookup"><span data-stu-id="87549-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="87549-177">Esse comportamento é semelhante à computação de derivações no fluxo de controle divergente.</span><span class="sxs-lookup"><span data-stu-id="87549-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="87549-178">Se o índice de recursos for divergente, o desempenho será reduzido em comparação com o caso de um índice uniforme, pois o hardware precisa executar operações em vários recursos.</span><span class="sxs-lookup"><span data-stu-id="87549-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="87549-179">Os índices de recursos que podem ser divergentes devem ser marcados com a `NonUniformResourceIndex` função no código HLSL.</span><span class="sxs-lookup"><span data-stu-id="87549-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="87549-180">Caso contrário, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="87549-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="87549-181">UAVs em sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="87549-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="87549-182">O SM 5.1 não impõe restrições em intervalos de UAV em sombreadores de pixel como foi o caso do SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="87549-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="87549-183">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="87549-183">Constant Buffers</span></span>

<span data-ttu-id="87549-184">A sintaxe de CBuffer (buffers de constantes) do SM 5.1 foi alterada do SM 5.0 para permitir que os desenvolvedores indexem buffers constantes.</span><span class="sxs-lookup"><span data-stu-id="87549-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="87549-185">Para habilitar buffers constantes indexáveis, o SM 5.1 apresenta a `ConstantBuffer` construção "template":</span><span class="sxs-lookup"><span data-stu-id="87549-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="87549-186">O código anterior declara a variável de buffer constante `myCB1` do tipo `Foo` e do tamanho 6, e uma variável de buffer escalar e constante `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="87549-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="87549-187">Uma variável de buffer constante agora pode ser indexada no sombreador como:</span><span class="sxs-lookup"><span data-stu-id="87549-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="87549-188">Os campos ' a ' e ' b ' não se tornam variáveis globais, mas, em vez disso, devem ser tratados como campos.</span><span class="sxs-lookup"><span data-stu-id="87549-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="87549-189">Para compatibilidade com versões anteriores, o SM 5.1 dá suporte ao conceito antigo de CBuffer para cbuffers escalar.</span><span class="sxs-lookup"><span data-stu-id="87549-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="87549-190">A instrução a seguir faz com que ' a ' e ' b ' as variáveis globais somente leitura como no SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="87549-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="87549-191">No entanto, esse CBuffer de estilo antigo não pode ser indexável.</span><span class="sxs-lookup"><span data-stu-id="87549-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="87549-192">Atualmente, o compilador do sombreador dá suporte `ConstantBuffer` apenas ao modelo para estruturas definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="87549-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="87549-193">Por motivos de compatibilidade, o compilador HLSL pode atribuir automaticamente registros de recursos para intervalos declarados em `space0` .</span><span class="sxs-lookup"><span data-stu-id="87549-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="87549-194">Se ' Space ' for omitido na cláusula Register, o padrão `space0` será usado.</span><span class="sxs-lookup"><span data-stu-id="87549-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="87549-195">O compilador usa a heurística do primeiro perfuração para atribuir os registros.</span><span class="sxs-lookup"><span data-stu-id="87549-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="87549-196">A atribuição pode ser recuperada por meio da API de reflexão, que foi estendida para adicionar o campo *espaço* para espaço, enquanto o campo *BindPoint* indica o limite inferior do intervalo de registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="87549-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="87549-197">Alterações de código de bytes no SM 5.1</span><span class="sxs-lookup"><span data-stu-id="87549-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="87549-198">O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções.</span><span class="sxs-lookup"><span data-stu-id="87549-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="87549-199">A sintaxe envolve a declaração de uma "variável" de registro, semelhante ao modo como é feito para os registros de memória compartilhada do Grupo:</span><span class="sxs-lookup"><span data-stu-id="87549-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

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

<span data-ttu-id="87549-200">Isso desmontará para:</span><span class="sxs-lookup"><span data-stu-id="87549-200">This will disassemble to:</span></span>

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

<span data-ttu-id="87549-201">Cada intervalo de recursos do sombreador agora tem uma ID (um nome) que é exclusiva para o código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="87549-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="87549-202">Por exemplo, a matriz de textura tex1 (T10) se torna 1 "no código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="87549-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="87549-203">Atribuir IDs exclusivas a cada intervalo de recursos permite duas coisas:</span><span class="sxs-lookup"><span data-stu-id="87549-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="87549-204">Identifique de forma não ambígua qual intervalo de recursos (consulte o \_ recurso DCL \_ Texture2D) está sendo indexado em uma instrução (consulte a instrução de exemplo).</span><span class="sxs-lookup"><span data-stu-id="87549-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="87549-205">Anexando um conjunto de atributos à declaração, por exemplo, tipo de elemento, tamanho de Stride, modo de operação de varredura, etc.</span><span class="sxs-lookup"><span data-stu-id="87549-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="87549-206">Observe que a ID do intervalo não está relacionada à declaração de limite inferior do HLSL.</span><span class="sxs-lookup"><span data-stu-id="87549-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="87549-207">A ordem das associações de recursos de reflexão (listagem na parte superior) e as instruções de declaração de sombreador (DCL \_ \* ) são as mesmas para auxiliar na identificação da correspondência entre as variáveis HLSL e as IDs de código de bytes.</span><span class="sxs-lookup"><span data-stu-id="87549-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="87549-208">Cada instrução de declaração no SM 5.1 usa um operando 3D para definir: ID de intervalo, limites inferiores e superiores.</span><span class="sxs-lookup"><span data-stu-id="87549-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="87549-209">Um token adicional é emitido para especificar o espaço de registro.</span><span class="sxs-lookup"><span data-stu-id="87549-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="87549-210">Outros tokens podem ser emitidos também para transmitir propriedades adicionais do intervalo, por exemplo, CBuffer ou instrução de declaração de buffer estruturado emite o tamanho do CBuffer ou da estrutura.</span><span class="sxs-lookup"><span data-stu-id="87549-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="87549-211">Os detalhes exatos da codificação podem ser encontrados em d3d12TokenizedProgramFormat. h e **D3D10ShaderBinary:: CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="87549-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="87549-212">As instruções do SM 5.1 não emitirão informações adicionais do operando de recurso como parte da instrução (como no SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="87549-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="87549-213">Essas informações agora estão nas instruções da declaração.</span><span class="sxs-lookup"><span data-stu-id="87549-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="87549-214">No SM 5.0, as instruções de indexação de recursos exigiam atributos de recurso a serem descritos em tokens de opcode estendidos, já que a indexação ofusca a associação à declaração.</span><span class="sxs-lookup"><span data-stu-id="87549-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="87549-215">No SM 5.1, cada ID (como ' t 1 ') é associada sem ambigüidade a uma única declaração que descreve as informações de recursos necessárias.</span><span class="sxs-lookup"><span data-stu-id="87549-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="87549-216">Portanto, os tokens de opcode estendidos usados em instruções para descrever as informações de recursos não são mais emitidos.</span><span class="sxs-lookup"><span data-stu-id="87549-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="87549-217">Em instruções de não declaração, um operando de recurso para amostras, SRVs e UAVs é um operando 2D.</span><span class="sxs-lookup"><span data-stu-id="87549-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="87549-218">O primeiro índice é uma constante literal que especifica a ID do intervalo.</span><span class="sxs-lookup"><span data-stu-id="87549-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="87549-219">O segundo índice representa o valor linear do índice.</span><span class="sxs-lookup"><span data-stu-id="87549-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="87549-220">O valor é calculado em relação ao início do espaço de registro correspondente (não relativo ao início do intervalo lógico) para correlacionar melhor com a assinatura raiz e para reduzir a carga do compilador de driver de ajustar o índice.</span><span class="sxs-lookup"><span data-stu-id="87549-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="87549-221">Um operando de recurso para CBVs é um operando 3D, contendo: ID literal do intervalo, índice do buffer de constantes, offset na instância específica do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="87549-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="87549-222">Declarações HLSL de exemplo</span><span class="sxs-lookup"><span data-stu-id="87549-222">Example HLSL Declarations</span></span>

<span data-ttu-id="87549-223">Os programas HLSL não precisam saber nada sobre assinaturas raiz.</span><span class="sxs-lookup"><span data-stu-id="87549-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="87549-224">Eles podem atribuir associações ao espaço de associação virtual "Register", t \# para SRVs, u \# para UAVs, b \# para CBVs, s \# para amostragens ou dependem do compilador para selecionar atribuições (e consultar os mapeamentos resultantes usando a reflexão do sombreador posteriormente).</span><span class="sxs-lookup"><span data-stu-id="87549-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="87549-225">As tabelas de descritores de mapeamentos de assinatura raiz e as constantes raiz para esse espaço de registro virtual.</span><span class="sxs-lookup"><span data-stu-id="87549-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="87549-226">Veja a seguir algumas declarações de exemplo que um sombreador HLSL pode ter.</span><span class="sxs-lookup"><span data-stu-id="87549-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="87549-227">Observe que não há referências a assinaturas raiz ou tabelas de descritores.</span><span class="sxs-lookup"><span data-stu-id="87549-227">Note that there are no references to root signatures or descriptor tables.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="87549-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87549-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87549-229">Indexação dinâmica usando HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="87549-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="87549-230">Efeito-ferramenta do compilador</span><span class="sxs-lookup"><span data-stu-id="87549-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="87549-231">Recursos do HLSL Shader Model 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="87549-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="87549-232">Exibições ordenadas do rasterizador</span><span class="sxs-lookup"><span data-stu-id="87549-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="87549-233">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="87549-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="87549-234">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="87549-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="87549-235">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="87549-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="87549-236">Valor de referência de estêncil especificado do sombreador</span><span class="sxs-lookup"><span data-stu-id="87549-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="87549-237">Especificando assinaturas raiz em HLSL</span><span class="sxs-lookup"><span data-stu-id="87549-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 