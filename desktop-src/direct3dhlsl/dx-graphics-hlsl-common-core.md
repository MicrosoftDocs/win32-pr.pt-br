---
title: Núcleo de Common-Shader
description: Núcleo de Common-Shader
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129713"
---
# <a name="common-shader-core"></a><span data-ttu-id="12f5f-103">Núcleo de Common-Shader</span><span class="sxs-lookup"><span data-stu-id="12f5f-103">Common-Shader Core</span></span>

<span data-ttu-id="12f5f-104">No sombreador modelo 4, todos os estágios de sombreador implementam a mesma funcionalidade base usando um núcleo de sombreador comum.</span><span class="sxs-lookup"><span data-stu-id="12f5f-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="12f5f-105">Além disso, cada um dos três estágios do sombreador (Vertex, Geometry e pixel) oferece a funcionalidade exclusiva para cada estágio, como a capacidade de gerar novos primitivos a partir do palco do sombreador de geometry ou para descartar um pixel específico no estágio do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="12f5f-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="12f5f-106">O diagrama a seguir mostra como os dados fluem por meio de um estágio do sombreador e a relação entre o núcleo do sombreador comum e os recursos de memória do sombreador.</span><span class="sxs-lookup"><span data-stu-id="12f5f-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagrama de fluxo de dados em um estágio do sombreador](images/d3d10-shader-unit.png)

-   <span data-ttu-id="12f5f-108">**Dados de entrada**: um sombreador de vértice recebe suas entradas do estágio de Assembler de entrada; os sombreadores de geometria e pixel recebem suas entradas do estágio do sombreador anterior.</span><span class="sxs-lookup"><span data-stu-id="12f5f-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="12f5f-109">Entradas adicionais incluem [semântica de valor do sistema](dx-graphics-hlsl-semantics.md), que são consumíveis pela primeira unidade no pipeline ao qual são aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="12f5f-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="12f5f-110">**Dados de saída**: os sombreadores geram resultados de saída a serem passados para o estágio subsequente no pipeline.</span><span class="sxs-lookup"><span data-stu-id="12f5f-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="12f5f-111">Para um sombreador de geometria, a quantidade de saída de dados de uma única invocação pode variar.</span><span class="sxs-lookup"><span data-stu-id="12f5f-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="12f5f-112">Algumas saídas são interpretadas pelo núcleo do sombreador comum (como a posição do vértice e o índice de destino de renderização), outras foram projetadas para serem interpretadas por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12f5f-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="12f5f-113">**Código do sombreador**: os sombreadores podem ler da memória, executar o ponto flutuante de vetor e operações aritméticas de inteiros ou operações de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="12f5f-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="12f5f-114">Não há nenhum limite para o número de instruções que podem ser implementadas em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="12f5f-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="12f5f-115">**Amostras**: os exemplos definem como filtrar as texturas de amostra e de filtro.</span><span class="sxs-lookup"><span data-stu-id="12f5f-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="12f5f-116">Até 16 amostras podem ser associadas simultaneamente a um sombreador.</span><span class="sxs-lookup"><span data-stu-id="12f5f-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="12f5f-117">**Texturas**: as texturas podem ser filtradas usando amostras ou lidas em uma base por Texel diretamente com a função intrínseca de [carregamento](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="12f5f-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="12f5f-118">**Buffers**: os buffers nunca são filtrados, mas podem ser lidos da memória por elemento diretamente com a função intrínseca de [carregamento](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="12f5f-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="12f5f-119">Até 128 recursos de textura e buffer (combinados) podem ser associados simultaneamente a um sombreador.</span><span class="sxs-lookup"><span data-stu-id="12f5f-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="12f5f-120">**Buffers de constantes**: os buffers de constantes são otimizados para variáveis de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="12f5f-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="12f5f-121">Até 16 buffers de constante podem ser associados a um estágio de sombreador simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="12f5f-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="12f5f-122">Elas foram projetadas para atualização mais frequente da CPU; Portanto, têm restrições de tamanho, de layout e de acesso adicionais.</span><span class="sxs-lookup"><span data-stu-id="12f5f-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="12f5f-123">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="12f5f-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="12f5f-124">No Direct3D 9, cada unidade do sombreador tinha um único arquivo de registro constante pequeno para armazenar todas as variáveis de sombreador constantes.</span><span class="sxs-lookup"><span data-stu-id="12f5f-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="12f5f-125">Acomodar todos os sombreadores com esse espaço de constante limitado exigiu reciclagem frequente de constantes pela CPU.</span><span class="sxs-lookup"><span data-stu-id="12f5f-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="12f5f-126">No Direct3D 10, as constantes são armazenadas em buffers imutáveis na memória e são gerenciadas como qualquer outro recurso.</span><span class="sxs-lookup"><span data-stu-id="12f5f-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="12f5f-127">Não há nenhum limite para o número de buffers constantes que um aplicativo pode criar.</span><span class="sxs-lookup"><span data-stu-id="12f5f-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="12f5f-128">Ao organizar constantes em buffers por frequência de atualização e uso, a quantidade de largura de banda necessária para atualizar constantes para acomodar todos os sombreadores pode ser significativamente reduzida.</span><span class="sxs-lookup"><span data-stu-id="12f5f-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="12f5f-129">Suporte a inteiros e a bits</span><span class="sxs-lookup"><span data-stu-id="12f5f-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="12f5f-130">O Core do sombreador comum fornece um conjunto completo de operações de inteiro e bit-bit de 32 bits em conformidade com IEEE.</span><span class="sxs-lookup"><span data-stu-id="12f5f-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="12f5f-131">Essas operações permitem uma nova classe de algoritmos nos exemplos de hardware de gráficos: técnicas de compactação e empacotamento, FFTs e controle de fluxo de programa de bits.</span><span class="sxs-lookup"><span data-stu-id="12f5f-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="12f5f-132">Os tipos de dados **int** e **uint** no Direct3D 10 HLSL são mapeados para inteiros de 32 bits no hardware.</span><span class="sxs-lookup"><span data-stu-id="12f5f-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f5f-133">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="12f5f-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="12f5f-134">Nas entradas de fluxo do Direct3D 9 marcadas como número inteiro em HLSL foram interpretadas como ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="12f5f-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="12f5f-135">No Direct3D 10, as entradas de fluxo marcadas como números inteiros são interpretadas como um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="12f5f-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="12f5f-136">Além disso, os valores Boolianos agora são todos definidos bits ou todos os bits são desdefinidos.</span><span class="sxs-lookup"><span data-stu-id="12f5f-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="12f5f-137">Os dados convertidos em **bool** serão interpretados como true se o valor não for igual a 0,0 f (zero positivo e negativo) puderem ser falsos) e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="12f5f-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="12f5f-138">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="12f5f-138">Bitwise operators</span></span>

<span data-ttu-id="12f5f-139">O sombreador comum do é compatível com os seguintes operadores bits:</span><span class="sxs-lookup"><span data-stu-id="12f5f-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="12f5f-140">Operador</span><span class="sxs-lookup"><span data-stu-id="12f5f-140">Operator</span></span>  | <span data-ttu-id="12f5f-141">Função</span><span class="sxs-lookup"><span data-stu-id="12f5f-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="12f5f-142">Não lógico</span><span class="sxs-lookup"><span data-stu-id="12f5f-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="12f5f-143">Deslocamento à esquerda</span><span class="sxs-lookup"><span data-stu-id="12f5f-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="12f5f-144">Deslocamento à direita</span><span class="sxs-lookup"><span data-stu-id="12f5f-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="12f5f-145">AND lógico</span><span class="sxs-lookup"><span data-stu-id="12f5f-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="12f5f-146">Ou lógico</span><span class="sxs-lookup"><span data-stu-id="12f5f-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="12f5f-147">XOR lógico</span><span class="sxs-lookup"><span data-stu-id="12f5f-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="12f5f-148">Deslocamento à esquerda igual</span><span class="sxs-lookup"><span data-stu-id="12f5f-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="12f5f-149">Deslocamento à direita igual</span><span class="sxs-lookup"><span data-stu-id="12f5f-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="12f5f-150">E igual a</span><span class="sxs-lookup"><span data-stu-id="12f5f-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="12f5f-151">Ou igual a</span><span class="sxs-lookup"><span data-stu-id="12f5f-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="12f5f-152">XOR igual</span><span class="sxs-lookup"><span data-stu-id="12f5f-152">Xor Equal</span></span>         |



 

<span data-ttu-id="12f5f-153">Os operadores bit a bit são definidos para operar somente em tipos de dados **int** e **uint** .</span><span class="sxs-lookup"><span data-stu-id="12f5f-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="12f5f-154">A tentativa de usar operadores de bit que não seja em tipos de dados **float** ou **struct** resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="12f5f-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="12f5f-155">Os operadores de bits a bit seguem a mesma precedência de C com relação a outros operadores.</span><span class="sxs-lookup"><span data-stu-id="12f5f-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="12f5f-156">Conversões binárias</span><span class="sxs-lookup"><span data-stu-id="12f5f-156">Binary Casts</span></span>

<span data-ttu-id="12f5f-157">A conversão entre um número inteiro e um tipo de ponto flutuante converterá o valor numérico após as regras de truncamento de C.</span><span class="sxs-lookup"><span data-stu-id="12f5f-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="12f5f-158">Converter um valor de um **float**, para um **int** e voltar para um **float** é uma conversão com perda dependente da precisão do tipo de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="12f5f-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="12f5f-159">Aqui estão algumas das funções de conversão: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**Asent (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="12f5f-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="12f5f-160">As conversões binárias também podem ser executadas usando funções intrínsecas HLSL.</span><span class="sxs-lookup"><span data-stu-id="12f5f-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="12f5f-161">Isso faz com que o compilador reinterprete a representação de bits de um número para o tipo de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="12f5f-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12f5f-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12f5f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f5f-163">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="12f5f-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





