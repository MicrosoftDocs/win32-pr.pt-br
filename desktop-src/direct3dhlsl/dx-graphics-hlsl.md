---
title: HLSL (linguagem do sombreador de alto nível)
description: HLSL é a linguagem de sombreador de alto nível C como a que você usa com sombreadores programáveis no DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104968273"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="4c287-103">HLSL (linguagem do sombreador de alto nível)</span><span class="sxs-lookup"><span data-stu-id="4c287-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="4c287-104">HLSL é a linguagem de sombreador de alto nível C como a que você usa com sombreadores programáveis no DirectX.</span><span class="sxs-lookup"><span data-stu-id="4c287-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="4c287-105">Por exemplo, você pode usar HLSL para escrever um [sombreador de vértice](../direct3d11/vertex-shader-stage.md)ou um [sombreador de pixel](../direct3d11/pixel-shader-stage.md)e usar esses sombreadores na implementação do renderizador em seu aplicativo [Direct3D](../direct3d12/directx-12-programming-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="4c287-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="4c287-106">Ou você pode usar HLSL para escrever um sombreador de computação, talvez para implementar uma simulação física.</span><span class="sxs-lookup"><span data-stu-id="4c287-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="4c287-107">No entanto, se, por exemplo, você estiver inclinado a escrever seu próprio operador de convolução (para o processamento de imagens) como HLSL em um sombreador de computação, você obterá um melhor desempenho nesse cenário se usar o [Direct Machine Learning (DirectML)](../direct3d12/dml.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4c287-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="4c287-108">O HLSL foi criado (começando com o DirectX 9) para configurar o [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programável.</span><span class="sxs-lookup"><span data-stu-id="4c287-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="4c287-109">Você pode programar todo o pipeline com instruções de HLSL.</span><span class="sxs-lookup"><span data-stu-id="4c287-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="4c287-110">Onde ir em seguida</span><span class="sxs-lookup"><span data-stu-id="4c287-110">Where to go next</span></span>

* [<span data-ttu-id="4c287-111">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="4c287-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="4c287-112">Referência para HLSL</span><span class="sxs-lookup"><span data-stu-id="4c287-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="4c287-113">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="4c287-113">Programming guide for HLSL</span></span>

<span data-ttu-id="4c287-114">Para obter uma introdução conceitual ao HLSL, consulte o [Guia de programação para HLSL](./dx-graphics-hlsl-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="4c287-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="4c287-115">O guia de programação aborda os diferentes tipos de estágios de sombreador e como criar, compilar, otimizar, associar e vincular sombreadores.</span><span class="sxs-lookup"><span data-stu-id="4c287-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="4c287-116">Lá você também encontrará visões gerais de, e notas de versão sobre, as gerações sucessivas da versão do modelo do sombreador que foram lançadas, voltando até o modelo de sombreador HLSL 5.</span><span class="sxs-lookup"><span data-stu-id="4c287-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="4c287-117">Referência para HLSL</span><span class="sxs-lookup"><span data-stu-id="4c287-117">Reference for HLSL</span></span>

<span data-ttu-id="4c287-118">Para obter a documentação de referência do HLSL, consulte a [referência para HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4c287-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="4c287-119">A seção de referência tem uma lista completa da sintaxe de linguagem e das funções intrínsecas criadas no HLSL para simplificar os requisitos de codificação.</span><span class="sxs-lookup"><span data-stu-id="4c287-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="4c287-120">Além disso, você encontrará uma discussão sobre os modelos de sombreador versus perfis, e o conteúdo de referência do modelo de sombreamento indo até o modelo de sombreador HLSL 1.</span><span class="sxs-lookup"><span data-stu-id="4c287-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="4c287-121">Também há conteúdo abrangendo instruções de assembly, a ferramenta D3DCompiler e informações sobre os erros e avisos que um sombreador pode retornar.</span><span class="sxs-lookup"><span data-stu-id="4c287-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>