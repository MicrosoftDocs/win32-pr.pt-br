---
description: As expressões são instruções matemáticas ou lógicas que são usadas no lado direito de um sinal de igual. Há muitos tipos de expressões.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expressões (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757342"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="f41ad-104">Expressões (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f41ad-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="f41ad-105">As expressões são instruções matemáticas ou lógicas que são usadas no lado direito de um sinal de igual.</span><span class="sxs-lookup"><span data-stu-id="f41ad-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="f41ad-106">Há muitos tipos de expressões.</span><span class="sxs-lookup"><span data-stu-id="f41ad-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="f41ad-107">Expressões</span><span class="sxs-lookup"><span data-stu-id="f41ad-107">Expressions</span></span>

1.  <span data-ttu-id="f41ad-108">Referência de variável</span><span class="sxs-lookup"><span data-stu-id="f41ad-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="f41ad-109">Escalar numérico</span><span class="sxs-lookup"><span data-stu-id="f41ad-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="f41ad-110">Expressão numérica</span><span class="sxs-lookup"><span data-stu-id="f41ad-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="f41ad-111">Todas as expressões HLL numéricas padrão têm suporte aqui.</span><span class="sxs-lookup"><span data-stu-id="f41ad-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="f41ad-112">Construtor</span><span class="sxs-lookup"><span data-stu-id="f41ad-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="f41ad-113">Lista de inicializadores</span><span class="sxs-lookup"><span data-stu-id="f41ad-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="f41ad-114">Os escalares devem ser valores escalares literais.</span><span class="sxs-lookup"><span data-stu-id="f41ad-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="f41ad-115">O número de inicializadores deve ser compatível com a variável (estado) no lado esquerdo do sinal de igual.</span><span class="sxs-lookup"><span data-stu-id="f41ad-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="f41ad-116">Expressão OR</span><span class="sxs-lookup"><span data-stu-id="f41ad-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="f41ad-117">Os tokens devem ser compatíveis com a variável (estado) no lado esquerdo do sinal de igual.</span><span class="sxs-lookup"><span data-stu-id="f41ad-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="f41ad-118">Os tokens não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f41ad-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="f41ad-119">NULO</span><span class="sxs-lookup"><span data-stu-id="f41ad-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="f41ad-120">NULL só pode ser atribuído a um sombreador, amostra ou objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f41ad-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="f41ad-121">Bloco de assembly</span><span class="sxs-lookup"><span data-stu-id="f41ad-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="f41ad-122">Os blocos de assembly do PS devem ser atribuídos ao estado PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="f41ad-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="f41ad-123">Os blocos de assembly do VS devem ser atribuídos ao estado VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="f41ad-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="f41ad-124">Bloco de estado de amostra</span><span class="sxs-lookup"><span data-stu-id="f41ad-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="f41ad-125">Os blocos de estado de amostra são sequências de estado de estágio de amostra não indexado ou atribuições de textura.</span><span class="sxs-lookup"><span data-stu-id="f41ad-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="f41ad-126">Os blocos de estado de amostra devem ser atribuídos ao estado de efeito de amostra.</span><span class="sxs-lookup"><span data-stu-id="f41ad-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="f41ad-127">Bloco de estado do estado de efeito</span><span class="sxs-lookup"><span data-stu-id="f41ad-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="f41ad-128">Os blocos de estado são sequências de estado geral.</span><span class="sxs-lookup"><span data-stu-id="f41ad-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="f41ad-129">Os blocos de estado podem ser aninhados, mas não podem conter referências circulares.</span><span class="sxs-lookup"><span data-stu-id="f41ad-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="f41ad-130">Os blocos de estado devem ser atribuídos ao estado de efeito STATEBLOCK.</span><span class="sxs-lookup"><span data-stu-id="f41ad-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="f41ad-131">HLSL compilar</span><span class="sxs-lookup"><span data-stu-id="f41ad-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="f41ad-132">O destino do sombreador de vértice vs \_ m \_ n indica a \_ versão do sombreador de vértice da versão D3DVS (m, n).</span><span class="sxs-lookup"><span data-stu-id="f41ad-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="f41ad-133">O destino do pixel shader PS \_ m \_ n Target indica a \_ versão do sombreador de pixel da versão D3DPS (m, n).</span><span class="sxs-lookup"><span data-stu-id="f41ad-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="f41ad-134">As expressões de compilação de linguagem de alto nível do sombreador de vértice só podem ser atribuídas ao estado de efeito VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="f41ad-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="f41ad-135">As expressões de compilação de linguagem de alto nível do sombreador de pixel só podem ser atribuídas ao estado de efeito PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="f41ad-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f41ad-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f41ad-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f41ad-137">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="f41ad-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



