---
title: Vinculação de Sombreador de Efeito
description: O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104297999"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="7cdde-103">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="7cdde-103">Effect Shader Linking</span></span>

<span data-ttu-id="7cdde-104">O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.</span><span class="sxs-lookup"><span data-stu-id="7cdde-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="7cdde-105">Visão geral da vinculação de sombreador de efeito</span><span class="sxs-lookup"><span data-stu-id="7cdde-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="7cdde-106">Usando vinculação de sombreador de efeito</span><span class="sxs-lookup"><span data-stu-id="7cdde-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="7cdde-107">Criando um efeito personalizado compatível com vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="7cdde-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="7cdde-108">Sombreador de efeito de exemplo compatível com vinculação</span><span class="sxs-lookup"><span data-stu-id="7cdde-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="7cdde-109">Compilando um sombreador compatível com vinculação</span><span class="sxs-lookup"><span data-stu-id="7cdde-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="7cdde-110">Etapa 1: compilar a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="7cdde-111">Etapa 2: compilar o sombreador completo e inserir a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="7cdde-112">Exportar especificações de função</span><span class="sxs-lookup"><span data-stu-id="7cdde-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="7cdde-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdde-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="7cdde-114">Visão geral da vinculação de sombreador de efeito</span><span class="sxs-lookup"><span data-stu-id="7cdde-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="7cdde-115">O efeito que as otimizações de vinculação do sombreador se baseia na vinculação do sombreador HLSL, um recurso do Direct3D 11,2 que permite que os sombreadores de pixel e vértice sejam gerados em tempo de execução por meio da vinculação de funções de sombreador pré-compilados.</span><span class="sxs-lookup"><span data-stu-id="7cdde-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="7cdde-116">As figuras a seguir ilustram o conceito de vinculação de sombreador de efeito em um grafo de efeito.</span><span class="sxs-lookup"><span data-stu-id="7cdde-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="7cdde-117">A primeira figura mostra um grafo típico de efeito de Direct2D com quatro transformações de renderização.</span><span class="sxs-lookup"><span data-stu-id="7cdde-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="7cdde-118">Sem vinculação de sombreador, cada transformação consome uma passagem de renderização e requer uma superfície intermediária; no total, esse grafo requer 4 passagens e 3 intermediários.</span><span class="sxs-lookup"><span data-stu-id="7cdde-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformação de grafo sem vinculação de sombreador: 4 passagens e 3 intermediários.](images/shader-transform-graph.png) |



 

<span data-ttu-id="7cdde-120">A segunda figura mostra o mesmo grafo de efeito em que cada transformação de renderização foi substituída por uma versão de função vinculável.</span><span class="sxs-lookup"><span data-stu-id="7cdde-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="7cdde-121">O Direct2D é capaz de vincular todo o grafo e executá-lo em uma passagem sem exigir nenhum intermediário.</span><span class="sxs-lookup"><span data-stu-id="7cdde-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="7cdde-122">Isso pode proporcionar uma diminuição significativa no tempo de execução da GPU e na redução do consumo máximo de memória da GPU.</span><span class="sxs-lookup"><span data-stu-id="7cdde-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![Grafo de transformação com vinculação de sombreador: 1 passagem, 0 intermediários.](images/shader-linking-graph.png) |



 

<span data-ttu-id="7cdde-124">A vinculação do sombreador de efeito opera em transformações individuais dentro de um efeito; Isso significa que até mesmo um grafo com um único efeito pode se beneficiar da vinculação de sombreador se esse efeito tiver várias transformações válidas.</span><span class="sxs-lookup"><span data-stu-id="7cdde-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="7cdde-125">Usando vinculação de sombreador de efeito</span><span class="sxs-lookup"><span data-stu-id="7cdde-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="7cdde-126">Se você estiver criando um aplicativo Direct2D que usa efeitos, não precisará fazer nada para tirar proveito da vinculação de sombreador de efeito.</span><span class="sxs-lookup"><span data-stu-id="7cdde-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="7cdde-127">O Direct2D analisa automaticamente o grafo de efeito para determinar a maneira mais adequada de vincular cada transformação.</span><span class="sxs-lookup"><span data-stu-id="7cdde-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="7cdde-128">Os autores de efeito são responsáveis por implementar seu efeito de forma que dê suporte à vinculação de sombreador de efeito; para obter mais informações, consulte a seção [criando um efeito personalizado compatível com vinculação de sombreador](#authoring-a-shader-linking-compatible-custom-effect) abaixo.</span><span class="sxs-lookup"><span data-stu-id="7cdde-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="7cdde-129">Todos os efeitos internos dão suporte à vinculação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="7cdde-130">Direct2D vinculará somente as transformações de renderização adjacentes em situações em que é benéfico.</span><span class="sxs-lookup"><span data-stu-id="7cdde-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="7cdde-131">Leva em consideração vários fatores ao determinar se deve vincular duas transformações.</span><span class="sxs-lookup"><span data-stu-id="7cdde-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="7cdde-132">Por exemplo, a vinculação de sombreador não é executada se uma das transformações usa um vértice ou sombreadores de computação, pois somente os sombreadores de pixel podem ser vinculados.</span><span class="sxs-lookup"><span data-stu-id="7cdde-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="7cdde-133">Além disso, se um efeito não foi criado para ser compatível com a vinculação de sombreador, as transformações ao redor não serão vinculadas a ele.</span><span class="sxs-lookup"><span data-stu-id="7cdde-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="7cdde-134">No caso de um risco de vinculação como esse existe, o Direct2D não vinculará nenhuma transformação adjacente ao risco, mas ainda tentará vincular o restante do grafo.</span><span class="sxs-lookup"><span data-stu-id="7cdde-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformação de grafo com um risco de vinculação: 2 passagens, 1 intermediário.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="7cdde-136">Criando um efeito personalizado compatível com vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="7cdde-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="7cdde-137">Se você estiver criando seu próprio efeito de Direct2D personalizado, precisará garantir que suas transformações ofereçam suporte à vinculação de sombreador de efeito.</span><span class="sxs-lookup"><span data-stu-id="7cdde-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="7cdde-138">Isso requer algumas pequenas alterações de como os efeitos personalizados anteriores foram implementados.</span><span class="sxs-lookup"><span data-stu-id="7cdde-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="7cdde-139">Se uma transformação dentro de seu efeito personalizado não oferecer suporte à vinculação de sombreador, Direct2D não a vinculará a nenhuma transformação adjacente a ela no grafo de efeito.</span><span class="sxs-lookup"><span data-stu-id="7cdde-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="7cdde-140">Como autor de um efeito personalizado, você deve estar ciente de vários conceitos e requisitos principais:</span><span class="sxs-lookup"><span data-stu-id="7cdde-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="7cdde-141">**Nenhuma alteração para afetar as implementações de interface**</span><span class="sxs-lookup"><span data-stu-id="7cdde-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="7cdde-142">Você não precisa modificar nenhum código que implemente as várias interfaces de efeito, como [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span><span class="sxs-lookup"><span data-stu-id="7cdde-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="7cdde-143">**Fornecer uma versão de função completa e de exportação dos sombreadores**</span><span class="sxs-lookup"><span data-stu-id="7cdde-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="7cdde-144">Você deve fornecer uma versão da função de exportação dos sombreadores do seu efeito que são vinculáveis por Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7cdde-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="7cdde-145">Além disso, você também deve continuar a fornecer o sombreador completo original; Isso ocorre porque Direct2D seleciona em tempo de execução a versão correta do sombreador, dependendo se a vinculação do sombreador deve ser aplicada a um link específico no grafo.</span><span class="sxs-lookup"><span data-stu-id="7cdde-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="7cdde-146">Se uma transformação fornecer apenas o blob de sombreador de pixel completo (via [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), ela não será vinculada a transformações adjacentes.</span><span class="sxs-lookup"><span data-stu-id="7cdde-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="7cdde-147">**Funções auxiliares**</span><span class="sxs-lookup"><span data-stu-id="7cdde-147">**Helper functions**</span></span>

    <span data-ttu-id="7cdde-148">O Direct2D fornece [funções auxiliares de HLSL](hlsl-helpers.md) e macros que irão gerar automaticamente as versões de função completa e de exportação de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="7cdde-149">Esses auxiliares podem ser encontrados em d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="7cdde-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="7cdde-150">Além disso, o compilador HLSL (FXC) permite que você insira o sombreador da função de exportação em um campo particular no sombreador completo.</span><span class="sxs-lookup"><span data-stu-id="7cdde-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="7cdde-151">Dessa forma, você só precisa criar um sombreador uma vez e passar as duas versões para Direct2D simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="7cdde-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="7cdde-152">Ambos os d2d1effecthelpers. hlsli e o compilador FXC são incluídos como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7cdde-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="7cdde-153">As funções auxiliares:</span><span class="sxs-lookup"><span data-stu-id="7cdde-153">The helper functions:</span></span>

  - [<span data-ttu-id="7cdde-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="7cdde-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="7cdde-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="7cdde-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="7cdde-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="7cdde-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="7cdde-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="7cdde-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="7cdde-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="7cdde-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="7cdde-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="7cdde-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="7cdde-160">\_Entrada do PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="7cdde-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="7cdde-161">Você também pode criar manualmente duas versões de cada sombreador e compilá-las duas vezes, contanto que as especificações descritas abaixo nas [especificações da função de exportação](#export-function-specifications) sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="7cdde-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="7cdde-162">**Somente sombreadores de pixel**</span><span class="sxs-lookup"><span data-stu-id="7cdde-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="7cdde-163">Direct2D não dá suporte à vinculação de sombreadores de computação ou de vértice.</span><span class="sxs-lookup"><span data-stu-id="7cdde-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="7cdde-164">No entanto, se o efeito usar um vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.</span><span class="sxs-lookup"><span data-stu-id="7cdde-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="7cdde-165">**Amostragem simples versus complexa**</span><span class="sxs-lookup"><span data-stu-id="7cdde-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="7cdde-166">A vinculação da função de sombreador funciona conectando a saída de um sombreador de pixel passado para a entrada de uma passagem de sombreador de pixel subsequente.</span><span class="sxs-lookup"><span data-stu-id="7cdde-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="7cdde-167">Isso só é possível quando o sombreador de pixel de consumo requer apenas um único valor de entrada para executar sua computação; Esse valor normalmente seria proveniente da amostragem de uma textura de entrada na coordenada de textura emitida pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="7cdde-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="7cdde-168">Esse sombreador de pixel é dito para executar uma amostragem simples.</span><span class="sxs-lookup"><span data-stu-id="7cdde-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![conversão em escala de cinza é um exemplo de amostragem simples.](images/simple-sampling.png) |

    

     

    <span data-ttu-id="7cdde-171">Alguns sombreadores de pixel, como um desfoque gaussiano, computam a saída de vários exemplos de entrada em vez de apenas um único exemplo.</span><span class="sxs-lookup"><span data-stu-id="7cdde-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="7cdde-172">Esse sombreador de pixel é dito para executar uma amostragem complexa.</span><span class="sxs-lookup"><span data-stu-id="7cdde-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![Desfoque Gaussiano é um exemplo de amostragem complexa.](images/complex-sampling.png) |

    

     

    <span data-ttu-id="7cdde-175">Somente as funções de sombreador com entradas simples podem ter sua entrada fornecida por outra função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="7cdde-176">As funções de sombreador com entradas complexas devem ser fornecidas com uma textura de entrada para amostra.</span><span class="sxs-lookup"><span data-stu-id="7cdde-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="7cdde-177">Isso significa que o Direct2D não vinculará um sombreador com entradas complexas ao seu antecessor.</span><span class="sxs-lookup"><span data-stu-id="7cdde-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="7cdde-178">Ao usar os [auxiliares do DIRECT2D HLSL](hlsl-helpers.md), você deve indicar no HLSL se um sombreador usa entradas complexas ou simples.</span><span class="sxs-lookup"><span data-stu-id="7cdde-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="7cdde-179">Sombreador de efeito de exemplo compatível com vinculação</span><span class="sxs-lookup"><span data-stu-id="7cdde-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="7cdde-180">Usando os auxiliares do D2D, o seguinte trecho de código representa um sombreador simples de efeito compatível com vinculação:</span><span class="sxs-lookup"><span data-stu-id="7cdde-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="7cdde-181">Neste exemplo curto, observe que nenhum parâmetro de função é declarado, que o número de entradas e o tipo de cada entrada é declarado antes da função de entrada, a entrada é recuperada chamando [D2DGetInput](d2dgetinput.md)e as diretivas de pré-processador devem ser definidas antes de o arquivo auxiliar ser incluído.</span><span class="sxs-lookup"><span data-stu-id="7cdde-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="7cdde-182">Um sombreador compatível com vinculação deve fornecer um sombreador de pixel de passagem simples regular e uma função de sombreador de exportação.</span><span class="sxs-lookup"><span data-stu-id="7cdde-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="7cdde-183">A macro de [ \_ \_ entrada do PS D2D](d2d-ps-entry.md) permite que cada um deles seja gerado a partir do mesmo código, quando usado em conjunto com o script de compilação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="7cdde-184">Ao compilar um sombreador completo, as macros são expandidas no código a seguir, que tem uma assinatura de entrada compatível com efeitos de D2D.</span><span class="sxs-lookup"><span data-stu-id="7cdde-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="7cdde-185">Ao compilar uma versão de função de exportação do mesmo código, o código a seguir é gerado:</span><span class="sxs-lookup"><span data-stu-id="7cdde-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="7cdde-186">Observe que a entrada de textura, normalmente recuperada por amostragem de um Texture2D, foi substituída por uma entrada de função (input0).</span><span class="sxs-lookup"><span data-stu-id="7cdde-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="7cdde-187">Para ver uma descrição completa e passo a passo do que você precisa fazer para escrever um efeito compatível com a vinculação, consulte o [tutorial de efeitos personalizados](custom-effects.md) e o [exemplo de efeitos de imagem personalizada do Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="7cdde-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="7cdde-188">Compilando um sombreador compatível com vinculação</span><span class="sxs-lookup"><span data-stu-id="7cdde-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="7cdde-189">Para ser vinculável, o blob do sombreador de pixel passado para D2D deve conter as versões de função completa e de exportação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="7cdde-190">Isso é feito inserindo-se a função de exportação compilada \_ na \_ área de dados particulares do blob do D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="7cdde-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="7cdde-191">Quando os sombreadores são criados com as funções auxiliares D2D, um destino de compilação D2D deve ser definido no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="7cdde-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="7cdde-192">Os tipos de destino de compilação são D2D \_ Full \_ Shader e D2D \_ Function.</span><span class="sxs-lookup"><span data-stu-id="7cdde-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="7cdde-193">A compilação de um sombreador de efeito compatível com vinculação é um processo de duas etapas:</span><span class="sxs-lookup"><span data-stu-id="7cdde-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="7cdde-194">Compilar a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="7cdde-195">Compilar o sombreador completo e inserir a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="7cdde-196">Ao compilar um efeito usando o Visual Studio, você deve criar um arquivo em lotes que execute ambos os comandos FXC e executar esse arquivo em lotes como uma etapa de compilação personalizada que é executada antes da etapa de compilação.</span><span class="sxs-lookup"><span data-stu-id="7cdde-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="7cdde-197">Etapa 1: compilar a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="7cdde-198">Para compilar a versão da função de exportação do sombreador, você deve passar os seguintes sinalizadores para FXC.</span><span class="sxs-lookup"><span data-stu-id="7cdde-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdde-199">**Sinalizador**</span><span class="sxs-lookup"><span data-stu-id="7cdde-199">**Flag**</span></span>                       | <span data-ttu-id="7cdde-200">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7cdde-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="7cdde-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="7cdde-201">/T <ShaderModel></span></span>         | <span data-ttu-id="7cdde-202">Defina <ShaderModel> como o perfil do sombreador de pixel apropriado, conforme definido na [sintaxe FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="7cdde-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="7cdde-203">Deve ser um dos perfis listados em "vinculação de sombreador HLSL".</span><span class="sxs-lookup"><span data-stu-id="7cdde-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="7cdde-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="7cdde-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="7cdde-205">Defina <MyShaderFile> como o nome do arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="7cdde-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="7cdde-206">/D \_ função D2D</span><span class="sxs-lookup"><span data-stu-id="7cdde-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="7cdde-207">Essa definição instrui o FXC a compilar a versão da função de exportação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="7cdde-208">/D \_ entrada D2D =<entry></span><span class="sxs-lookup"><span data-stu-id="7cdde-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="7cdde-209">Defina <entry> como o nome do ponto de entrada HLSL que você definiu dentro da macro de [ \_ \_ entrada do D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="7cdde-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="7cdde-210">/FL <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="7cdde-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="7cdde-211">Defina <MyShaderfile> como onde você deseja armazenar a versão da função de exportação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="7cdde-212">Observe que a extensão. fxlib é apenas para facilidade de identificação.</span><span class="sxs-lookup"><span data-stu-id="7cdde-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="7cdde-213">Etapa 2: compilar o sombreador completo e inserir a função de exportação</span><span class="sxs-lookup"><span data-stu-id="7cdde-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="7cdde-214">Para compilar a versão completa do sombreador com a versão de exportação inserida, você deve passar os seguintes sinalizadores para FXC.</span><span class="sxs-lookup"><span data-stu-id="7cdde-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdde-215">**Sinalizador**</span><span class="sxs-lookup"><span data-stu-id="7cdde-215">**Flag**</span></span>                               | <span data-ttu-id="7cdde-216">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7cdde-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7cdde-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="7cdde-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="7cdde-218">Defina <ShaderModel> como o perfil do sombreador de pixel apropriado, conforme definido na [sintaxe FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="7cdde-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="7cdde-219">Este deve ser o perfil do sombreador de pixel correspondente ao perfil de vinculação especificado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="7cdde-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="7cdde-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="7cdde-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="7cdde-221">Defina <MyShaderFile> como o nome do arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="7cdde-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="7cdde-222">/D D2D \_ Full \_ Shader</span><span class="sxs-lookup"><span data-stu-id="7cdde-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="7cdde-223">Essa definição instrui o FXC a compilar a versão completa do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="7cdde-224">/D \_ entrada D2D =<entry></span><span class="sxs-lookup"><span data-stu-id="7cdde-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="7cdde-225">Defina <entry> como o nome do ponto de entrada do HLSL que você definiu dentro da \_ \_ macro de entrada () do D2D PS.</span><span class="sxs-lookup"><span data-stu-id="7cdde-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="7cdde-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="7cdde-226">/E <entry></span></span>                       | <span data-ttu-id="7cdde-227">Defina <entry> como o nome do ponto de entrada do HLSL que você definiu dentro da \_ \_ macro de entrada () do D2D PS.</span><span class="sxs-lookup"><span data-stu-id="7cdde-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="7cdde-228">/SetPrivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="7cdde-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="7cdde-229">Esse argumento instrui o FXC a inserir o sombreador da função de exportação gerado na etapa 1 \_ na \_ área de dados particulares do blob do D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="7cdde-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="7cdde-230">/Fo <MyShader> . CSO</span><span class="sxs-lookup"><span data-stu-id="7cdde-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="7cdde-231">Defina <MyShader> como onde você deseja armazenar o sombreador compilado final e combinado.</span><span class="sxs-lookup"><span data-stu-id="7cdde-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="7cdde-232">/FH <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="7cdde-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="7cdde-233">Defina <MyShader> como onde você deseja armazenar o cabeçalho final combinado.</span><span class="sxs-lookup"><span data-stu-id="7cdde-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="7cdde-234">Exportar especificações de função</span><span class="sxs-lookup"><span data-stu-id="7cdde-234">Export function specifications</span></span>

<span data-ttu-id="7cdde-235">É possível – embora não seja recomendado – criar um sombreador de efeito compatível sem usar os auxiliares fornecidos pelo D2D.</span><span class="sxs-lookup"><span data-stu-id="7cdde-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="7cdde-236">Deve-se ter cuidado para garantir que as assinaturas de entrada do sombreador completo e da função de exportação estejam de acordo com as especificações de D2D.</span><span class="sxs-lookup"><span data-stu-id="7cdde-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="7cdde-237">As especificações para sombreadores completos são as mesmas que as versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="7cdde-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="7cdde-238">Resumidamente, os parâmetros de entrada do sombreador de pixel devem ser a posição da VA \_ , a posição da cena \_ e uma TEXCOORD por entrada de efeito.</span><span class="sxs-lookup"><span data-stu-id="7cdde-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="7cdde-239">Para a função de exportação, a função deve retornar um FLOAT4 e suas entradas devem ser um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="7cdde-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="7cdde-240">Entrada simples</span><span class="sxs-lookup"><span data-stu-id="7cdde-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="7cdde-241">Para entradas simples, o D2D inserirá uma função de exemplo entre a textura de entrada e a função de sombreador, ou a entrada será fornecida pela saída de outra função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="7cdde-242">Entrada complexa</span><span class="sxs-lookup"><span data-stu-id="7cdde-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="7cdde-243">Para entradas complexas, o D2D passará apenas por uma coordenada de textura, conforme descrito na documentação do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cdde-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="7cdde-244">Local de saída</span><span class="sxs-lookup"><span data-stu-id="7cdde-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="7cdde-245">Somente uma entrada de posição de cena \_ pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="7cdde-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="7cdde-246">Esse parâmetro só deve ser incluído quando necessário, já que apenas uma função por sombreador vinculado pode utilizar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7cdde-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="7cdde-247">A semântica deve ser definida como acima, pois o D2D inspecionará a semântica para decidir como vincular funções juntas.</span><span class="sxs-lookup"><span data-stu-id="7cdde-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="7cdde-248">Se qualquer entrada de função não corresponder a um dos tipos acima, a função será rejeitada para vinculação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7cdde-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cdde-249">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdde-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdde-250">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="7cdde-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="7cdde-251">Interface ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="7cdde-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="7cdde-252">Interface ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="7cdde-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 