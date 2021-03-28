---
title: Formato de efeito (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Saiba mais sobre: formato de efeito (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164011"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="58d75-103">Formato de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="58d75-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="58d75-104">Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito.</span><span class="sxs-lookup"><span data-stu-id="58d75-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="58d75-105">O estado do efeito pode ser basicamente dividido em três categorias:</span><span class="sxs-lookup"><span data-stu-id="58d75-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="58d75-106">[Variáveis](d3d11-effect-variable-syntax.md), que geralmente são declaradas na parte superior de um efeito.</span><span class="sxs-lookup"><span data-stu-id="58d75-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="58d75-107">[Funções](d3d11-effect-function-syntax.md), que implementam o código de sombreador ou são usadas como funções auxiliares por outras funções.</span><span class="sxs-lookup"><span data-stu-id="58d75-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="58d75-108">[Técnicas](d3d11-effect-technique-syntax.md), que podem ser organizadas em grupos de efeito e implementam sequências de renderização usando um ou mais efeitos aprovados.</span><span class="sxs-lookup"><span data-stu-id="58d75-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="58d75-109">Cada passagem define um ou mais [grupos de Estados](d3d11-effect-states.md) e chama funções de sombreador.</span><span class="sxs-lookup"><span data-stu-id="58d75-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![diagrama das categorias de declarações para efeitos, incluindo variáveis na parte superior, funções no meio e técnicas na parte inferior](images/d3d10-effect-intro.png)

<span data-ttu-id="58d75-111">O diagrama anterior mostra as categorias de estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="58d75-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="58d75-112">A definição do formato binário de efeito pode ser encontrada em \\ EffectBinaryFormat. h binário no código-fonte de efeitos.</span><span class="sxs-lookup"><span data-stu-id="58d75-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="58d75-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="58d75-113">In this section</span></span>



| <span data-ttu-id="58d75-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="58d75-114">Topic</span></span>                                                                   | <span data-ttu-id="58d75-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="58d75-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58d75-116">Sintaxe da variável de efeito</span><span class="sxs-lookup"><span data-stu-id="58d75-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="58d75-117">Uma variável de efeito é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58d75-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="58d75-118">Sintaxe da anotação</span><span class="sxs-lookup"><span data-stu-id="58d75-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="58d75-119">Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58d75-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="58d75-120">Sintaxe da função de efeito</span><span class="sxs-lookup"><span data-stu-id="58d75-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="58d75-121">Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58d75-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="58d75-122">Sintaxe da técnica de efeito</span><span class="sxs-lookup"><span data-stu-id="58d75-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="58d75-123">Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58d75-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="58d75-124">Grupos de estado de efeito</span><span class="sxs-lookup"><span data-stu-id="58d75-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="58d75-125">Os Estados de efeito são pares de valor de nome na forma de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="58d75-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="58d75-126">Sintaxe do grupo de efeitos</span><span class="sxs-lookup"><span data-stu-id="58d75-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="58d75-127">Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="58d75-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="58d75-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58d75-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d75-129">Referência dos efeitos 11</span><span class="sxs-lookup"><span data-stu-id="58d75-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





