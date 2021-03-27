---
title: Otimizando sombreadores HLSL
description: Esta seção descreve estratégias de finalidade geral que você pode usar para otimizar seus sombreadores. Você pode aplicar essas estratégias a sombreadores que são escritos em qualquer linguagem, em qualquer plataforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- linguagem de sombreamento de alto nível
- HLSL, desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005906"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="ac981-106">Otimizando sombreadores HLSL</span><span class="sxs-lookup"><span data-stu-id="ac981-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="ac981-107">Esta seção descreve estratégias de finalidade geral que você pode usar para otimizar seus sombreadores.</span><span class="sxs-lookup"><span data-stu-id="ac981-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="ac981-108">Você pode aplicar essas estratégias a sombreadores que são escritos em qualquer linguagem, em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="ac981-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="ac981-109">Saiba onde executar cálculos de sombreador</span><span class="sxs-lookup"><span data-stu-id="ac981-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="ac981-110">Ignorar instruções desnecessárias</span><span class="sxs-lookup"><span data-stu-id="ac981-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="ac981-111">Variáveis de pacote e Interpolants</span><span class="sxs-lookup"><span data-stu-id="ac981-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="ac981-112">Reduzir a complexidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="ac981-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="ac981-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac981-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="ac981-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac981-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="ac981-115">Saiba onde executar cálculos de sombreador</span><span class="sxs-lookup"><span data-stu-id="ac981-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="ac981-116">Os sombreadores de vértice executam operações que incluem a busca de vértices e a execução de transformação de matriz de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="ac981-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="ac981-117">Normalmente, os sombreadores de vértice são executados uma vez por vértice.</span><span class="sxs-lookup"><span data-stu-id="ac981-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="ac981-118">Sombreadores de pixel executam operações que incluem a busca de dados de textura e a execução de cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="ac981-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="ac981-119">Normalmente, os sombreadores de pixel são executados uma vez por pixel para uma determinada parte da geometria.</span><span class="sxs-lookup"><span data-stu-id="ac981-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="ac981-120">Normalmente, pixels ultrapassam vértices em uma cena, portanto, sombreadores de pixel são executados com mais frequência do que os sombreadores de vértice.</span><span class="sxs-lookup"><span data-stu-id="ac981-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="ac981-121">Ao criar algoritmos de sombreador, tenha em mente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ac981-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="ac981-122">Faça cálculos no sombreador de vértice, se possível.</span><span class="sxs-lookup"><span data-stu-id="ac981-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="ac981-123">Um cálculo que é executado em um sombreador de pixel é muito mais caro do que um cálculo que é executado em um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="ac981-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="ac981-124">Considere o uso de cálculos por vértice para melhorar o desempenho em situações como malhas densas.</span><span class="sxs-lookup"><span data-stu-id="ac981-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="ac981-125">Para malhas densas, os cálculos por vértice podem produzir resultados que são visualmente indistinguíveis dos resultados produzidos com cálculos por pixel.</span><span class="sxs-lookup"><span data-stu-id="ac981-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="ac981-126">Ignorar instruções desnecessárias</span><span class="sxs-lookup"><span data-stu-id="ac981-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="ac981-127">No HLSL, a ramificação dinâmica fornece a capacidade de limitar o número de instruções executadas.</span><span class="sxs-lookup"><span data-stu-id="ac981-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="ac981-128">Portanto, a ramificação dinâmica pode ajudar a acelerar o tempo de execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac981-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="ac981-129">Se a geometria ou os pixels não forem exibidos, use a ramificação dinâmica para sair do sombreador ou para limitar as instruções.</span><span class="sxs-lookup"><span data-stu-id="ac981-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="ac981-130">Por exemplo, se um pixel não estiver aceso, não haverá nenhum ponto na execução do algoritmo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="ac981-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="ac981-131">A tabela a seguir lista alguns casos em que você pode testar condições em seu sombreador e usar a ramificação dinâmica para ignorar instruções desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="ac981-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="ac981-132">A tabela não é abrangente.</span><span class="sxs-lookup"><span data-stu-id="ac981-132">The table not comprehensive.</span></span> <span data-ttu-id="ac981-133">Em vez disso, ele é destinado a fornecer ideias para otimizar seu código.</span><span class="sxs-lookup"><span data-stu-id="ac981-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="ac981-134">Condição a ser verificada</span><span class="sxs-lookup"><span data-stu-id="ac981-134">Condition to Check</span></span>                                    | <span data-ttu-id="ac981-135">Resposta no sombreador</span><span class="sxs-lookup"><span data-stu-id="ac981-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="ac981-136">A seleção alfa determina que um pixel não será visto.</span><span class="sxs-lookup"><span data-stu-id="ac981-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="ac981-137">Ignore o restante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac981-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="ac981-138">O pixel ou a geometria é totalmente fogged.</span><span class="sxs-lookup"><span data-stu-id="ac981-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="ac981-139">Ignore o restante do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac981-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="ac981-140">Os pesos da capa são zero.</span><span class="sxs-lookup"><span data-stu-id="ac981-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="ac981-141">Ignorar Bones.</span><span class="sxs-lookup"><span data-stu-id="ac981-141">Skip bones.</span></span>                  |
| <span data-ttu-id="ac981-142">A atenuação de luz é zero.</span><span class="sxs-lookup"><span data-stu-id="ac981-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="ac981-143">Ignorar iluminação.</span><span class="sxs-lookup"><span data-stu-id="ac981-143">Skip lighting.</span></span>               |
| <span data-ttu-id="ac981-144">Termo Lambertian não positivo.</span><span class="sxs-lookup"><span data-stu-id="ac981-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="ac981-145">Ignorar iluminação.</span><span class="sxs-lookup"><span data-stu-id="ac981-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="ac981-146">Variáveis de pacote e Interpolants</span><span class="sxs-lookup"><span data-stu-id="ac981-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="ac981-147">Lembre-se do espaço necessário para dados do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac981-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="ac981-148">Empacotar a quantidade de informações em uma variável ou interpolação o mais possível.</span><span class="sxs-lookup"><span data-stu-id="ac981-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="ac981-149">Às vezes, as informações de duas variáveis podem ser incluídas no espaço de memória de uma única variável.</span><span class="sxs-lookup"><span data-stu-id="ac981-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="ac981-150">Reduzir a complexidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="ac981-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="ac981-151">Mantenha seus sombreadores pequenos e simples.</span><span class="sxs-lookup"><span data-stu-id="ac981-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="ac981-152">Em geral, os sombreadores com menos instruções são executados mais rapidamente do que os sombreadores com mais instruções.</span><span class="sxs-lookup"><span data-stu-id="ac981-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="ac981-153">Também é mais fácil depurar e otimizar sombreadores menores e menos complexos.</span><span class="sxs-lookup"><span data-stu-id="ac981-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac981-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac981-154">Related Topics</span></span>

[<span data-ttu-id="ac981-155">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="ac981-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="ac981-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac981-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac981-157">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="ac981-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




