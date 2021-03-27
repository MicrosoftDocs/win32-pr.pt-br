---
title: Escrevendo sombreadores HLSL no Direct3D 9
description: Escrevendo sombreadores HLSL no Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007936"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="fdf96-103">Escrevendo sombreadores HLSL no Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="fdf96-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="fdf96-104">Vértice – noções básicas do sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="fdf96-105">Noções básicas do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fdf96-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="fdf96-106">Estágio de textura e Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="fdf96-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="fdf96-107">Entradas do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fdf96-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="fdf96-108">Saídas de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fdf96-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="fdf96-109">Entradas de sombreador e variáveis de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="fdf96-110">Declarando variáveis de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="fdf96-111">Entradas de sombreador uniforme</span><span class="sxs-lookup"><span data-stu-id="fdf96-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="fdf96-112">Variantes de entradas e semânticas de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="fdf96-113">Exemplos e objetos de textura</span><span class="sxs-lookup"><span data-stu-id="fdf96-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="fdf96-114">Gravando funções</span><span class="sxs-lookup"><span data-stu-id="fdf96-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="fdf96-115">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="fdf96-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="fdf96-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf96-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="fdf96-117">Noções básicas do Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="fdf96-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="fdf96-118">Quando em operação, um sombreador de vértice programável substitui o processamento de vértice realizado pelo pipeline de gráficos do Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fdf96-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="fdf96-119">Ao usar um sombreador de vértice, as informações de estado sobre as operações de transformação e iluminação são ignoradas pelo pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="fdf96-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="fdf96-120">Quando o sombreador de vértice é desabilitado e o processamento de função fixa é retornado, todas as configurações de estado atuais se aplicam.</span><span class="sxs-lookup"><span data-stu-id="fdf96-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="fdf96-121">O mosaico de primitivos de ordem superior deve ser feito antes da execução do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="fdf96-122">As implementações que executam o mosaico de superfície após o processamento do sombreador devem fazer isso de forma que não seja aparente para o código do aplicativo e do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="fdf96-123">Como um mínimo, um sombreador de vértice deve produzir a posição do vértice no espaço de clipe homogêneo.</span><span class="sxs-lookup"><span data-stu-id="fdf96-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="fdf96-124">Opcionalmente, o sombreador de vértice pode gerar coordenadas de textura, cor de vértice, iluminação de vértice, fatores de neblina e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fdf96-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="fdf96-125">Noções básicas do Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="fdf96-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="fdf96-126">O processamento de pixel é executado por sombreadores de pixel em pixels individuais.</span><span class="sxs-lookup"><span data-stu-id="fdf96-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="fdf96-127">Sombreadores de pixel funcionam em conjunto com sombreadores de vértice; a saída de um sombreador de vértice fornece as entradas para um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="fdf96-128">Outras operações de pixel (mesclagem de neblina, operações de estêncil e mesclagem de destino de renderização) ocorrem após a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="fdf96-129">Estágio de textura e Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="fdf96-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="fdf96-130">Um sombreador de pixel substitui completamente a funcionalidade de mistura de pixels especificada pelo misturador de várias texturas, incluindo operações definidas anteriormente pelos Estados de estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="fdf96-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="fdf96-131">As operações de amostragem e filtragem de textura que foram controladas pelos Estados de estágio de textura padrão para minificação, ampliação, filtragem de MIP e os modos de endereçamento de encapsulamento podem ser inicializadas em sombreadores.</span><span class="sxs-lookup"><span data-stu-id="fdf96-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="fdf96-132">O aplicativo é livre para alterar esses Estados sem exigir a regeneração do sombreador atualmente ligado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="fdf96-133">O estado da configuração pode se tornar ainda mais fácil se os sombreadores forem projetados dentro de um efeito.</span><span class="sxs-lookup"><span data-stu-id="fdf96-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="fdf96-134">Entradas do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fdf96-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="fdf96-135">Para as versões do sombreador de pixel PS \_ 1 \_ 1-PS \_ 2 \_ 0, as cores difusa e especular são saturadas (clamped) no intervalo de 0 a 1 antes de serem usadas pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="fdf96-136">A entrada de valores de cor para o sombreador de pixel é considerada uma perspectiva correta, mas isso não é garantido (para todos os hardwares).</span><span class="sxs-lookup"><span data-stu-id="fdf96-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="fdf96-137">As cores amostradas das coordenadas de textura são iteradas de maneira correta da perspectiva e são clampeddas para o intervalo de 0 a 1 durante a iteração.</span><span class="sxs-lookup"><span data-stu-id="fdf96-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="fdf96-138">Saídas de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fdf96-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="fdf96-139">Para as versões do sombreador de pixel PS \_ 1 \_ 1-PS \_ 1 \_ 4, o resultado emitido pelo sombreador de pixel é o conteúdo de Register r0.</span><span class="sxs-lookup"><span data-stu-id="fdf96-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="fdf96-140">Tudo o que ele contém quando o sombreador conclui o processamento é enviado ao estágio de neblina e ao Blender de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="fdf96-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="fdf96-141">Para as versões PS \_ 2 \_ 0 e superior do pixel shader, a cor de saída é emitida de OC0-oC4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="fdf96-142">Entradas de sombreador e variáveis de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="fdf96-143">Declarando variáveis de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="fdf96-144">Entradas de sombreador uniforme</span><span class="sxs-lookup"><span data-stu-id="fdf96-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="fdf96-145">Variantes de entradas e semânticas de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="fdf96-146">Exemplos e objetos de textura</span><span class="sxs-lookup"><span data-stu-id="fdf96-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="fdf96-147">Declarando variáveis de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-147">Declaring Shader Variables</span></span>

<span data-ttu-id="fdf96-148">A declaração de variável mais simples inclui um tipo e um nome de variável, como esta declaração de ponto flutuante:</span><span class="sxs-lookup"><span data-stu-id="fdf96-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="fdf96-149">Você pode inicializar uma variável na mesma instrução.</span><span class="sxs-lookup"><span data-stu-id="fdf96-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="fdf96-150">Uma matriz de variáveis pode ser declarada,</span><span class="sxs-lookup"><span data-stu-id="fdf96-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="fdf96-151">ou declarados e inicializados na mesma instrução.</span><span class="sxs-lookup"><span data-stu-id="fdf96-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="fdf96-152">Aqui estão algumas declarações que demonstram muitas das características das variáveis de HLSL (linguagem de sombreamento de alto nível):</span><span class="sxs-lookup"><span data-stu-id="fdf96-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="fdf96-153">As declarações de dados podem usar qualquer tipo válido, incluindo:</span><span class="sxs-lookup"><span data-stu-id="fdf96-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="fdf96-154">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="fdf96-155">Tipo de vetor (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="fdf96-156">Tipo de matriz (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="fdf96-157">Tipo de sombreador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="fdf96-158">Tipo de amostra (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="fdf96-159">Tipo definido pelo usuário (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdf96-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="fdf96-160">Um sombreador pode ter variáveis, argumentos e funções de nível superior.</span><span class="sxs-lookup"><span data-stu-id="fdf96-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="fdf96-161">As variáveis de nível superior são declaradas fora de todas as funções.</span><span class="sxs-lookup"><span data-stu-id="fdf96-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="fdf96-162">Argumentos de nível superior são parâmetros para uma função de nível superior.</span><span class="sxs-lookup"><span data-stu-id="fdf96-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="fdf96-163">Uma função de nível superior é qualquer função chamada pelo aplicativo (em oposição a uma função que é chamada por outra função).</span><span class="sxs-lookup"><span data-stu-id="fdf96-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="fdf96-164">Entradas de sombreador uniforme</span><span class="sxs-lookup"><span data-stu-id="fdf96-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="fdf96-165">Os sombreadores de vértice e pixel aceitam dois tipos de dados de entrada: variáveis e uniformes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="fdf96-166">A entrada variável são os dados que são exclusivos para cada execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="fdf96-167">Para um sombreador de vértice, os dados variados (por exemplo: Position, normal, etc.) são provenientes dos fluxos de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="fdf96-168">Os dados uniformes (por exemplo: cor do material, transformação mundial, etc.) são constantes para várias execuções de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="fdf96-169">Para aqueles familiarizados com os modelos de sombreador de assembly, os dados uniformes são especificados por registros constantes e dados variados pelos registros v e t.</span><span class="sxs-lookup"><span data-stu-id="fdf96-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="fdf96-170">Os dados uniformes podem ser especificados por dois métodos.</span><span class="sxs-lookup"><span data-stu-id="fdf96-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="fdf96-171">O método mais comum é declarar variáveis globais e usá-las em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="fdf96-172">Qualquer uso de variáveis globais dentro de um sombreador resultará na adição dessa variável à lista de variáveis uniformes exigidas por esse sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="fdf96-173">O segundo método é marcar um parâmetro de entrada da função de sombreador de nível superior como uniforme.</span><span class="sxs-lookup"><span data-stu-id="fdf96-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="fdf96-174">Essa marcação Especifica que a variável fornecida deve ser adicionada à lista de variáveis uniformes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="fdf96-175">As variáveis uniformes usadas por um sombreador são comunicadas de volta para o aplicativo por meio da tabela constante.</span><span class="sxs-lookup"><span data-stu-id="fdf96-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="fdf96-176">A tabela constante é o nome da tabela de símbolos que define como as variáveis uniformes usadas por um sombreador se ajustam aos registros constantes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="fdf96-177">Os parâmetros de função uniforme aparecem na tabela de constantes precedidas por um cifrão ($), ao contrário das variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="fdf96-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="fdf96-178">O sinal de dólar é necessário para evitar colisões de nomes entre entradas uniformes locais e variáveis globais do mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="fdf96-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="fdf96-179">A tabela constante contém os locais de registro constante de todas as variáveis uniformes usadas pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="fdf96-180">A tabela também inclui as informações de tipo e o valor padrão, se especificado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="fdf96-181">Variantes de entradas e semânticas de sombreador</span><span class="sxs-lookup"><span data-stu-id="fdf96-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="fdf96-182">Os parâmetros de entrada variados (de uma função de sombreamento de nível superior) devem ser marcados com uma palavra-chave semântica ou uniforme indicando que o valor é constante para a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="fdf96-183">Se uma entrada de sombreador de nível superior não estiver marcada com uma palavra-chave semântica ou uniforme, o sombreador não será compilado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="fdf96-184">A semântica de entrada é um nome usado para vincular a entrada fornecida a uma saída da parte anterior do pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="fdf96-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="fdf96-185">Por exemplo, a semântica de entrada POSITION0 é usada pelos sombreadores de vértice para especificar onde os dados de posição do buffer de vértice devem ser vinculados.</span><span class="sxs-lookup"><span data-stu-id="fdf96-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="fdf96-186">Os sombreadores de pixel e vértice têm conjuntos diferentes de semântica de entrada devido às diferentes partes do pipeline de gráficos que são alimentadas em cada unidade de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="fdf96-187">A semântica de entrada do sombreador de vértice descreve as informações por vértice (por exemplo: posição, normal, coordenadas de textura, cor, tangente, binormal, etc.) a serem carregadas de um buffer de vértice em um formulário que pode ser consumido pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="fdf96-188">A semântica de entrada é mapeada diretamente para o uso da declaração de vértice e o índice de uso.</span><span class="sxs-lookup"><span data-stu-id="fdf96-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="fdf96-189">A semântica de entrada do sombreador de pixel descreve as informações fornecidas por pixel pela unidade de rasterização.</span><span class="sxs-lookup"><span data-stu-id="fdf96-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="fdf96-190">Os dados são gerados por interpolação entre saídas do sombreador de vértice para cada vértice do primitivo atual.</span><span class="sxs-lookup"><span data-stu-id="fdf96-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="fdf96-191">A semântica de entrada do sombreador de pixel básico vincula a cor de saída e as informações de coordenadas de textura a parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdf96-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="fdf96-192">A semântica de entrada pode ser atribuída à entrada de sombreador por dois métodos:</span><span class="sxs-lookup"><span data-stu-id="fdf96-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="fdf96-193">Acrescentar dois-pontos e o nome semântico à declaração de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fdf96-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="fdf96-194">Definição de uma estrutura de entrada com semântica de entrada atribuída a cada membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="fdf96-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="fdf96-195">Os sombreadores de vértice e pixel fornecem dados de saída para o estágio de pipeline de gráficos subsequente.</span><span class="sxs-lookup"><span data-stu-id="fdf96-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="fdf96-196">A semântica de saída é usada para especificar como os dados gerados pelo sombreador devem ser vinculados às entradas do próximo estágio.</span><span class="sxs-lookup"><span data-stu-id="fdf96-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="fdf96-197">Por exemplo, a semântica de saída para um sombreador de vértice é usada para vincular as saídas dos interpoladores no rasterizador para gerar os dados de entrada para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="fdf96-198">As saídas do sombreador de pixel são os valores fornecidos para a unidade de mesclagem alfa para cada um dos destinos de renderização ou o valor de profundidade gravado no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="fdf96-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="fdf96-199">A semântica de saída do sombreador de vértice é usada para vincular o sombreador ao sombreador de pixel e ao estágio do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="fdf96-200">Um sombreador de vértice que é consumido pelo rasterizador e não exposto ao sombreador de pixel deve gerar dados de posição como um mínimo.</span><span class="sxs-lookup"><span data-stu-id="fdf96-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="fdf96-201">Os sombreadores de vértice que geram coordenadas de textura e dados de cor fornecem esses dados para um sombreador de pixel após a conclusão da interpolação.</span><span class="sxs-lookup"><span data-stu-id="fdf96-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="fdf96-202">A semântica de saída do sombreador de pixel associa as cores de saída de um sombreador de pixel com o destino de renderização correto.</span><span class="sxs-lookup"><span data-stu-id="fdf96-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="fdf96-203">A cor de saída do sombreador de pixel é vinculada ao estágio Alpha Blend, que determina como os destinos de renderização de destino são modificados.</span><span class="sxs-lookup"><span data-stu-id="fdf96-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="fdf96-204">A saída de profundidade do sombreador de pixel pode ser usada para alterar os valores de profundidade de destino no local de varredura atual.</span><span class="sxs-lookup"><span data-stu-id="fdf96-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="fdf96-205">A saída de profundidade e vários destinos de renderização só têm suporte com alguns modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="fdf96-206">A sintaxe para a semântica de saída é idêntica à sintaxe para especificar a semântica de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdf96-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="fdf96-207">A semântica pode ser especificada diretamente em parâmetros declarados como parâmetros "out" ou atribuídas durante a definição de uma estrutura que é retornada como um parâmetro "out" ou o valor de retorno de uma função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="fdf96-208">A semântica identifica de onde vêm os dados.</span><span class="sxs-lookup"><span data-stu-id="fdf96-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="fdf96-209">A semântica são identificadores opcionais que identificam entradas e saídas de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="fdf96-210">A semântica aparece em um dos três locais:</span><span class="sxs-lookup"><span data-stu-id="fdf96-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="fdf96-211">Depois de um membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="fdf96-211">After a structure member.</span></span>
-   <span data-ttu-id="fdf96-212">Depois de um argumento na lista de argumentos de entrada de uma função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="fdf96-213">Após a lista de argumentos de entrada da função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-213">After the function's input argument list.</span></span>

<span data-ttu-id="fdf96-214">Este exemplo usa uma estrutura para fornecer uma ou mais entradas de sombreador de vértice e outra estrutura para fornecer uma ou mais saídas de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="fdf96-215">Cada um dos membros da estrutura usa uma semântica.</span><span class="sxs-lookup"><span data-stu-id="fdf96-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="fdf96-216">A estrutura de entrada identifica os dados do buffer de vértice que fornecerá as entradas do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="fdf96-217">Esse sombreador mapeia os dados dos elementos position, normal e blendweight do buffer de vértice em registros de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="fdf96-218">O tipo de dados de entrada não precisa corresponder exatamente ao tipo de dados de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="fdf96-219">Se não corresponder exatamente, os dados do vértice serão automaticamente convertidos no tipo de dados do HLSL quando forem gravados nos registros do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="fdf96-220">Por exemplo, se os dados normais foram definidos para serem do tipo UINT pelo aplicativo, ele seria convertido em um float3 quando lido pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="fdf96-221">Se os dados no fluxo de vértice contiverem menos componentes do que o tipo de dados do sombreador correspondente, os componentes ausentes serão inicializados como 0 (exceto para w, que é inicializado como 1).</span><span class="sxs-lookup"><span data-stu-id="fdf96-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="fdf96-222">A semântica de entrada é semelhante aos valores no [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="fdf96-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="fdf96-223">A estrutura de saída identifica os parâmetros de saída do sombreador de vértice de posição e cor.</span><span class="sxs-lookup"><span data-stu-id="fdf96-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="fdf96-224">Essas saídas serão usadas pelo pipeline para a rasterização de triângulo (no processamento primitivo).</span><span class="sxs-lookup"><span data-stu-id="fdf96-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="fdf96-225">A saída marcada como dados de posição denota a posição de um vértice no espaço homogêneo.</span><span class="sxs-lookup"><span data-stu-id="fdf96-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="fdf96-226">Como um mínimo, um sombreador de vértice deve gerar dados de posição.</span><span class="sxs-lookup"><span data-stu-id="fdf96-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="fdf96-227">A posição do espaço da tela é calculada após a conclusão do sombreador de vértice, dividindo a coordenada (x, y, z) por w.</span><span class="sxs-lookup"><span data-stu-id="fdf96-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="fdf96-228">No espaço da tela,-1 e 1 são os valores x e y mínimo e máximo dos limites do visor, enquanto z é usado para teste de buffer z.</span><span class="sxs-lookup"><span data-stu-id="fdf96-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="fdf96-229">A semântica de saída também é semelhante aos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="fdf96-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="fdf96-230">Em geral, uma estrutura de saída para um sombreador de vértice também pode ser usada como a estrutura de entrada para um sombreador de pixel, desde que o sombreador de pixel não leia nenhuma variável marcada com a posição, o tamanho do ponto ou a semântica de neblina.</span><span class="sxs-lookup"><span data-stu-id="fdf96-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="fdf96-231">Essas semânticas estão associadas a valores escalares por vértice que não são usados por um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="fdf96-232">Se esses valores forem necessários para o sombreador de pixel, eles poderão ser copiados em outra variável de saída que usa uma semântica de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="fdf96-233">Variáveis globais são atribuídas a registros automaticamente pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="fdf96-234">As variáveis globais também são chamadas de parâmetros uniformes porque o conteúdo da variável é o mesmo para todos os pixels processados cada vez que o sombreador é chamado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="fdf96-235">Os registros estão contidos na tabela de constantes, que pode ser lida usando a interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .</span><span class="sxs-lookup"><span data-stu-id="fdf96-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="fdf96-236">A semântica de entrada para sombreadores de pixel mapeia valores em registros de hardware específicos para transporte entre sombreadores de vértice e sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="fdf96-237">Cada tipo de registro tem propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="fdf96-237">Each register type has specific properties.</span></span> <span data-ttu-id="fdf96-238">Como atualmente há apenas duas semânticas para coordenadas de cor e textura, é comum que a maioria dos dados seja marcada como uma coordenada de textura mesmo quando não estiver.</span><span class="sxs-lookup"><span data-stu-id="fdf96-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="fdf96-239">Observe que a estrutura de saída do sombreador de vértice usou uma entrada com dados de posição, que não é usada pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="fdf96-240">O HLSL permite dados de saída válidos de um sombreador de vértice que não são dados de entrada válidos para um sombreador de pixel, desde que ele não seja referenciado no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="fdf96-241">Os argumentos de entrada também podem ser matrizes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="fdf96-242">A semântica é incrementada automaticamente pelo compilador para cada elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="fdf96-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="fdf96-243">Por exemplo, considere a seguinte declaração explícita:</span><span class="sxs-lookup"><span data-stu-id="fdf96-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="fdf96-244">A declaração explícita fornecida acima é equivalente à declaração a seguir que terá semânticas incrementadas automaticamente pelo compilador:</span><span class="sxs-lookup"><span data-stu-id="fdf96-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="fdf96-245">Assim como a semântica de entrada, a semântica de saída identifica o uso de dados para dados de saída do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="fdf96-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="fdf96-246">Muitos sombreadores de pixel gravam em apenas uma cor de saída.</span><span class="sxs-lookup"><span data-stu-id="fdf96-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="fdf96-247">Os sombreadores de pixel também podem gravar um valor de profundidade em um ou mais destinos de renderização múltiplos ao mesmo tempo (até quatro).</span><span class="sxs-lookup"><span data-stu-id="fdf96-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="fdf96-248">Como os sombreadores de vértice, os sombreadores de pixel usam uma estrutura para retornar mais de uma saída.</span><span class="sxs-lookup"><span data-stu-id="fdf96-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="fdf96-249">Esse sombreador grava 0 nos componentes de cor, bem como no componente de profundidade.</span><span class="sxs-lookup"><span data-stu-id="fdf96-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="fdf96-250">As cores de saída do sombreador de pixel devem ser do tipo FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="fdf96-251">Ao escrever várias cores, todas as cores de saída devem ser usadas de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="fdf96-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="fdf96-252">Em outras palavras, [COLOR1](dx-graphics-hlsl-semantics.md) não pode ser uma saída, a menos que [COLOR0](dx-graphics-hlsl-semantics.md) já tenha sido gravado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="fdf96-253">A saída de profundidade do sombreador de pixel deve ser do tipo float1.</span><span class="sxs-lookup"><span data-stu-id="fdf96-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="fdf96-254">Exemplos e objetos de textura</span><span class="sxs-lookup"><span data-stu-id="fdf96-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="fdf96-255">Um classificador contém o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="fdf96-255">A sampler contains sampler state.</span></span> <span data-ttu-id="fdf96-256">O estado de amostra especifica a textura a ser amostrada e controla a filtragem feita durante a amostragem.</span><span class="sxs-lookup"><span data-stu-id="fdf96-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="fdf96-257">Três coisas são necessárias para fazer amostras de uma textura:</span><span class="sxs-lookup"><span data-stu-id="fdf96-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="fdf96-258">Uma textura</span><span class="sxs-lookup"><span data-stu-id="fdf96-258">A texture</span></span>
-   <span data-ttu-id="fdf96-259">Uma amostra (com o estado de amostra)</span><span class="sxs-lookup"><span data-stu-id="fdf96-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="fdf96-260">Uma instrução de amostragem</span><span class="sxs-lookup"><span data-stu-id="fdf96-260">A sampling instruction</span></span>

<span data-ttu-id="fdf96-261">Os exemplos podem ser inicializados com texturas e estado de amostra, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="fdf96-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="fdf96-262">Aqui está um exemplo do código para exemplo de uma textura 2D:</span><span class="sxs-lookup"><span data-stu-id="fdf96-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="fdf96-263">A textura é declarada com uma variável de textura tex0.</span><span class="sxs-lookup"><span data-stu-id="fdf96-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="fdf96-264">Neste exemplo, uma variável de amostra chamada s \_ 2D é declarada.</span><span class="sxs-lookup"><span data-stu-id="fdf96-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="fdf96-265">O classificador contém o estado de amostra dentro de chaves.</span><span class="sxs-lookup"><span data-stu-id="fdf96-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="fdf96-266">Isso inclui a textura que será amostrada e, opcionalmente, o estado do filtro (ou seja, modos de encapsulamento, modos de filtro, etc.).</span><span class="sxs-lookup"><span data-stu-id="fdf96-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="fdf96-267">Se o estado de amostra for omitido, um estado de amostra padrão será aplicado especificando a filtragem linear e um modo de encapsulamento para as coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fdf96-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="fdf96-268">A função de amostra usa uma coordenada de textura de ponto flutuante de dois componentes e retorna uma cor de dois componentes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="fdf96-269">Isso é representado com o tipo de retorno float2 e representa dados nos componentes vermelho e verde.</span><span class="sxs-lookup"><span data-stu-id="fdf96-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="fdf96-270">Quatro tipos de amostra são definidos (consulte as [palavras-chave](dx-graphics-hlsl-appendix.md)) e as pesquisas de textura são executadas pelas funções intrínsecas [**: tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="fdf96-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="fdf96-271">Aqui está um exemplo de amostragem 3D:</span><span class="sxs-lookup"><span data-stu-id="fdf96-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="fdf96-272">Esta declaração de amostra usa o estado de amostra padrão para as configurações de filtro e o modo de endereço.</span><span class="sxs-lookup"><span data-stu-id="fdf96-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="fdf96-273">Este é o exemplo de amostragem de cubo correspondente:</span><span class="sxs-lookup"><span data-stu-id="fdf96-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="fdf96-274">E, finalmente, aqui está o exemplo de amostragem 1D:</span><span class="sxs-lookup"><span data-stu-id="fdf96-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="fdf96-275">Como o tempo de execução não dá suporte a texturas 1D, o compilador usará uma textura 2D com o conhecimento de que a coordenada y não é importante.</span><span class="sxs-lookup"><span data-stu-id="fdf96-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="fdf96-276">Como [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) é implementado como uma pesquisa de textura 2D, o compilador é livre para escolher o componente y de maneira eficiente.</span><span class="sxs-lookup"><span data-stu-id="fdf96-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="fdf96-277">Em alguns cenários raros, o compilador não pode escolher um componente y eficiente; nesse caso, ele emitirá um aviso.</span><span class="sxs-lookup"><span data-stu-id="fdf96-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="fdf96-278">Esse exemplo específico é ineficiente porque o compilador deve mover a coordenada de entrada para outro registro (porque uma pesquisa 1D é implementada como uma pesquisa 2D e a coordenada de textura é declarada como um float1).</span><span class="sxs-lookup"><span data-stu-id="fdf96-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="fdf96-279">Se o código for reescrito usando uma entrada float2 em vez de um float1, o compilador poderá usar a coordenada de textura de entrada porque sabe que y foi inicializada para algo.</span><span class="sxs-lookup"><span data-stu-id="fdf96-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="fdf96-280">Todas as pesquisas de textura podem ser acrescentadas com "bias" ou "proj" (ou seja, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span><span class="sxs-lookup"><span data-stu-id="fdf96-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="fdf96-281">Com o sufixo "proj", a coordenada de textura é dividida pelo componente w.</span><span class="sxs-lookup"><span data-stu-id="fdf96-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="fdf96-282">Com "tendência", o nível MIP é deslocado pelo componente w-.</span><span class="sxs-lookup"><span data-stu-id="fdf96-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="fdf96-283">Assim, todas as pesquisas de textura com um sufixo sempre usam uma entrada FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="fdf96-284">[**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) e [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignoram os componentes YZ e z, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fdf96-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="fdf96-285">Os exemplos também podem ser usados na matriz, embora nenhum back-end atualmente ofereça suporte ao acesso de matriz dinâmica de amostras.</span><span class="sxs-lookup"><span data-stu-id="fdf96-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="fdf96-286">Portanto, o seguinte é válido porque pode ser resolvido no momento da compilação:</span><span class="sxs-lookup"><span data-stu-id="fdf96-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="fdf96-287">No entanto, este exemplo não é válido.</span><span class="sxs-lookup"><span data-stu-id="fdf96-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="fdf96-288">O acesso dinâmico de amostras é útil principalmente para escrever programas com loops literais.</span><span class="sxs-lookup"><span data-stu-id="fdf96-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="fdf96-289">O código a seguir ilustra o acesso à matriz de amostras:</span><span class="sxs-lookup"><span data-stu-id="fdf96-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="fdf96-290">O uso do Microsoft Direct3D Debug Runtime pode ajudá-lo a detectar incompatibilidades entre o número de componentes em uma textura e uma amostra.</span><span class="sxs-lookup"><span data-stu-id="fdf96-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="fdf96-291">Gravando funções</span><span class="sxs-lookup"><span data-stu-id="fdf96-291">Writing Functions</span></span>

<span data-ttu-id="fdf96-292">As funções dividem tarefas grandes em partes menores.</span><span class="sxs-lookup"><span data-stu-id="fdf96-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="fdf96-293">Tarefas pequenas são mais fáceis de depurar e podem ser reutilizadas, uma vez comprovadas.</span><span class="sxs-lookup"><span data-stu-id="fdf96-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="fdf96-294">As funções podem ser usadas para ocultar detalhes de outras funções, o que torna um programa composto por funções mais fácil de seguir.</span><span class="sxs-lookup"><span data-stu-id="fdf96-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="fdf96-295">As funções HLSL são semelhantes às funções C de várias maneiras: elas contêm uma definição e um corpo de função e ambas declaram tipos de retorno e listas de argumentos.</span><span class="sxs-lookup"><span data-stu-id="fdf96-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="fdf96-296">Como as funções do C, a validação de HLSL faz a verificação de tipo nos argumentos, nos tipos de argumento e no valor de retorno durante a compilação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="fdf96-297">Ao contrário das funções de C, as funções de ponto de entrada HLSL usam a semântica para associar argumentos de função a entradas e saídas de sombreador (funções HLSL chamadas de semântica de ignorar internamente).</span><span class="sxs-lookup"><span data-stu-id="fdf96-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="fdf96-298">Isso facilita a vinculação de dados de buffer a um sombreador e a vinculação de saídas de sombreador a entradas de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="fdf96-299">Uma função contém uma declaração e um corpo, e a declaração deve preceder o corpo.</span><span class="sxs-lookup"><span data-stu-id="fdf96-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="fdf96-300">A declaração de função inclui tudo na frente das chaves:</span><span class="sxs-lookup"><span data-stu-id="fdf96-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="fdf96-301">Uma declaração de função contém:</span><span class="sxs-lookup"><span data-stu-id="fdf96-301">A function declaration contains:</span></span>

-   <span data-ttu-id="fdf96-302">Um tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="fdf96-302">A return type</span></span>
-   <span data-ttu-id="fdf96-303">Um nome de função</span><span class="sxs-lookup"><span data-stu-id="fdf96-303">A function name</span></span>
-   <span data-ttu-id="fdf96-304">Uma lista de argumentos (opcional)</span><span class="sxs-lookup"><span data-stu-id="fdf96-304">An argument list (optional)</span></span>
-   <span data-ttu-id="fdf96-305">Uma semântica de saída (opcional)</span><span class="sxs-lookup"><span data-stu-id="fdf96-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="fdf96-306">Uma anotação (opcional)</span><span class="sxs-lookup"><span data-stu-id="fdf96-306">An annotation (optional)</span></span>

<span data-ttu-id="fdf96-307">O tipo de retorno pode ser qualquer um dos tipos de dados básicos do HLSL, como um FLOAT4:</span><span class="sxs-lookup"><span data-stu-id="fdf96-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="fdf96-308">O tipo de retorno pode ser uma estrutura que já foi definida:</span><span class="sxs-lookup"><span data-stu-id="fdf96-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="fdf96-309">Se a função não retornar um valor, void poderá ser usado como o tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="fdf96-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="fdf96-310">O tipo de retorno sempre aparece primeiro em uma declaração de função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="fdf96-311">Uma lista de argumentos declara os argumentos de entrada para uma função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="fdf96-312">Ele também pode declarar valores que serão retornados.</span><span class="sxs-lookup"><span data-stu-id="fdf96-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="fdf96-313">Alguns argumentos são argumentos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="fdf96-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="fdf96-314">Aqui está um exemplo de um sombreador que usa quatro argumentos de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdf96-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="fdf96-315">Essa função retorna uma cor final, que é uma mistura de um exemplo de textura e a cor clara.</span><span class="sxs-lookup"><span data-stu-id="fdf96-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="fdf96-316">A função usa quatro entradas.</span><span class="sxs-lookup"><span data-stu-id="fdf96-316">The function takes four inputs.</span></span> <span data-ttu-id="fdf96-317">Duas entradas têm semântica: LightDir tem a semântica [TEXCOORD1](dx-graphics-hlsl-semantics.md) e texcrd tem a semântica [TEXCOORD0](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="fdf96-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="fdf96-318">A semântica significa que os dados dessas variáveis serão provenientes do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="fdf96-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="fdf96-319">Embora a variável LightDir tenha uma semântica [TEXCOORD1](dx-graphics-hlsl-semantics.md) , o parâmetro provavelmente não é uma coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="fdf96-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="fdf96-320">O tipo semântico de TEXCOORDn geralmente é usado para fornecer uma semântica para um tipo que não é predefinido (não há semântica de entrada de sombreador de vértice para uma direção clara).</span><span class="sxs-lookup"><span data-stu-id="fdf96-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="fdf96-321">As outras duas entradas LightColor e SAMP são rotuladas com a palavra-chave [uniforme](dx-graphics-hlsl-appendix.md) .</span><span class="sxs-lookup"><span data-stu-id="fdf96-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="fdf96-322">Essas são constantes uniformes que não serão alteradas entre chamadas de desenho.</span><span class="sxs-lookup"><span data-stu-id="fdf96-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="fdf96-323">Os valores para esses parâmetros vêm de variáveis globais do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="fdf96-324">Os argumentos podem ser rotulados como entradas com a palavra-chave in e os argumentos de saída com a palavra-chave out.</span><span class="sxs-lookup"><span data-stu-id="fdf96-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="fdf96-325">Os argumentos não podem ser passados por referência; no entanto, um argumento pode ser uma entrada e uma saída se ela for declarada com a palavra-chave InOut.</span><span class="sxs-lookup"><span data-stu-id="fdf96-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="fdf96-326">Os argumentos passados para uma função que são marcados com a palavra-chave Inout são considerados cópias do original até que a função seja retornada, e elas são copiadas de volta.</span><span class="sxs-lookup"><span data-stu-id="fdf96-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="fdf96-327">Veja um exemplo usando o Inout:</span><span class="sxs-lookup"><span data-stu-id="fdf96-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="fdf96-328">Essa função incrementa os valores em A e B e os retorna.</span><span class="sxs-lookup"><span data-stu-id="fdf96-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="fdf96-329">O corpo da função é todo o código após a declaração da função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="fdf96-330">O corpo consiste em instruções que estão entre chaves.</span><span class="sxs-lookup"><span data-stu-id="fdf96-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="fdf96-331">O corpo da função implementa toda a funcionalidade usando variáveis, literais, expressões e instruções.</span><span class="sxs-lookup"><span data-stu-id="fdf96-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="fdf96-332">O corpo do sombreador faz duas coisas: ele executa uma multiplicação de matriz e retorna um resultado de FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="fdf96-333">A multiplicação de matriz é realizada com a função [**Mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , que executa uma multiplicação de matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="fdf96-334">**Mul (DirectX HLSL)** é chamado de função intrínseca porque já está embutido na biblioteca HLSL de funções.</span><span class="sxs-lookup"><span data-stu-id="fdf96-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="fdf96-335">As funções intrínsecas serão abordadas com mais detalhes na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="fdf96-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="fdf96-336">A matriz multiplique combina um PDV de vetor de entrada e uma WorldViewProj de matriz composta.</span><span class="sxs-lookup"><span data-stu-id="fdf96-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="fdf96-337">O resultado é a posição dos dados transformados no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="fdf96-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="fdf96-338">Esse é o processamento mínimo de sombreador de vértice que podemos fazer.</span><span class="sxs-lookup"><span data-stu-id="fdf96-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="fdf96-339">Se estivesse usando o pipeline de função fixa em vez de um sombreador de vértice, os dados de vértice poderiam ser desenhados depois de fazer essa transformação.</span><span class="sxs-lookup"><span data-stu-id="fdf96-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="fdf96-340">A última instrução em um corpo de função é uma instrução return.</span><span class="sxs-lookup"><span data-stu-id="fdf96-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="fdf96-341">Assim como C, essa instrução retorna o controle da função para a instrução que chamou a função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="fdf96-342">Os tipos de retorno de função podem ser qualquer um dos tipos de dados simples definidos em HLSL, incluindo bool, Half int, float e Double.</span><span class="sxs-lookup"><span data-stu-id="fdf96-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="fdf96-343">Os tipos de retorno podem ser um dos tipos de dados complexos, como vetores e matrizes.</span><span class="sxs-lookup"><span data-stu-id="fdf96-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="fdf96-344">Os tipos HLSL que se referem a objetos não podem ser usados como tipos de retorno.</span><span class="sxs-lookup"><span data-stu-id="fdf96-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="fdf96-345">Isso inclui PixelShader, vertexshader, Texture e Sample.</span><span class="sxs-lookup"><span data-stu-id="fdf96-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="fdf96-346">Aqui está um exemplo de uma função que usa uma estrutura para um tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="fdf96-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="fdf96-347">O tipo de retorno FLOAT4 foi substituído pela estrutura VS \_ output, que agora contém um único membro FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="fdf96-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="fdf96-348">Uma instrução return sinaliza o final de uma função.</span><span class="sxs-lookup"><span data-stu-id="fdf96-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="fdf96-349">Essa é a instrução de retorno mais simples.</span><span class="sxs-lookup"><span data-stu-id="fdf96-349">This is the simplest return statement.</span></span> <span data-ttu-id="fdf96-350">Ele retorna o controle da função para o programa de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdf96-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="fdf96-351">Ele não retorna nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="fdf96-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="fdf96-352">Uma instrução return pode retornar um ou mais valores.</span><span class="sxs-lookup"><span data-stu-id="fdf96-352">A return statement can return one or more values.</span></span> <span data-ttu-id="fdf96-353">Este exemplo retorna um valor literal:</span><span class="sxs-lookup"><span data-stu-id="fdf96-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="fdf96-354">Este exemplo retorna o resultado escalar de uma expressão:</span><span class="sxs-lookup"><span data-stu-id="fdf96-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="fdf96-355">Este exemplo retorna um FLOAT4 construído a partir de uma variável local e um literal:</span><span class="sxs-lookup"><span data-stu-id="fdf96-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="fdf96-356">Este exemplo retorna um FLOAT4 que é construído a partir do resultado retornado de uma função intrínseca e alguns valores literais:</span><span class="sxs-lookup"><span data-stu-id="fdf96-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="fdf96-357">Este exemplo retorna uma estrutura que contém um ou mais membros:</span><span class="sxs-lookup"><span data-stu-id="fdf96-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="fdf96-358">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="fdf96-358">Flow Control</span></span>

<span data-ttu-id="fdf96-359">A maioria dos hardwares de vértice e de sombreador de pixel atual foi projetada para executar um sombreador linha por linha, executando cada instrução uma vez.</span><span class="sxs-lookup"><span data-stu-id="fdf96-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="fdf96-360">O HLSL dá suporte ao controle de fluxo, que inclui ramificação estática, instruções predicadas, loop estático, ramificação dinâmica e loop dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fdf96-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="fdf96-361">Anteriormente, o uso de uma instrução If resultou em um código de sombreador de linguagem de assembly que implementa tanto o lado If quanto o lado else do fluxo de código.</span><span class="sxs-lookup"><span data-stu-id="fdf96-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="fdf96-362">Aqui está um exemplo do código no HLSL que foi compilado para vs \_ 1 \_ 1:</span><span class="sxs-lookup"><span data-stu-id="fdf96-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="fdf96-363">E aqui está o código do assembly resultante:</span><span class="sxs-lookup"><span data-stu-id="fdf96-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="fdf96-364">Alguns hardwares permitem o loop estático ou dinâmico, mas a maioria exige execução linear.</span><span class="sxs-lookup"><span data-stu-id="fdf96-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="fdf96-365">Nos modelos que não dão suporte a looping, todos os loops devem ser não revertidos.</span><span class="sxs-lookup"><span data-stu-id="fdf96-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="fdf96-366">Um exemplo é a amostra de exemplo [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) que usa loops não acumulados até mesmo para os \_ \_ sombreadores PS 1 1.</span><span class="sxs-lookup"><span data-stu-id="fdf96-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="fdf96-367">O HLSL agora inclui suporte para cada um desses tipos de controle de fluxo:</span><span class="sxs-lookup"><span data-stu-id="fdf96-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="fdf96-368">ramificação estática</span><span class="sxs-lookup"><span data-stu-id="fdf96-368">static branching</span></span>
-   <span data-ttu-id="fdf96-369">instruções predicadas</span><span class="sxs-lookup"><span data-stu-id="fdf96-369">predicated instructions</span></span>
-   <span data-ttu-id="fdf96-370">loop estático</span><span class="sxs-lookup"><span data-stu-id="fdf96-370">static looping</span></span>
-   <span data-ttu-id="fdf96-371">ramificação dinâmica</span><span class="sxs-lookup"><span data-stu-id="fdf96-371">dynamic branching</span></span>
-   <span data-ttu-id="fdf96-372">loop dinâmico</span><span class="sxs-lookup"><span data-stu-id="fdf96-372">dynamic looping</span></span>

<span data-ttu-id="fdf96-373">A ramificação estática permite que blocos de código de sombreador sejam ativados ou desativados com base em uma constante de sombreador booliano.</span><span class="sxs-lookup"><span data-stu-id="fdf96-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="fdf96-374">Esse é um método conveniente para habilitar ou desabilitar caminhos de código com base no tipo de objeto que está sendo processado no momento.</span><span class="sxs-lookup"><span data-stu-id="fdf96-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="fdf96-375">Entre chamadas de desenho, você pode decidir quais recursos deseja dar suporte com o sombreador atual e, em seguida, definir os sinalizadores boolianos necessários para obter esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="fdf96-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="fdf96-376">Todas as instruções que são desabilitadas por uma constante booliana são ignoradas durante a execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdf96-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="fdf96-377">O suporte de ramificação mais familiar é a ramificação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="fdf96-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="fdf96-378">Com a ramificação dinâmica, a condição de comparação reside em uma variável, o que significa que a comparação é feita para cada vértice ou cada pixel em tempo de execução (ao contrário da comparação que ocorre no momento da compilação ou entre duas chamadas de desenho).</span><span class="sxs-lookup"><span data-stu-id="fdf96-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="fdf96-379">O impacto no desempenho é o custo da ramificação mais o custo das instruções no lado da ramificação obtidas.</span><span class="sxs-lookup"><span data-stu-id="fdf96-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="fdf96-380">A ramificação dinâmica é implementada no sombreador modelo 3 ou superior.</span><span class="sxs-lookup"><span data-stu-id="fdf96-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="fdf96-381">Otimizar os sombreadores que funcionam com esses modelos é semelhante a otimizar o código executado em uma CPU.</span><span class="sxs-lookup"><span data-stu-id="fdf96-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdf96-382">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf96-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf96-383">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="fdf96-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 