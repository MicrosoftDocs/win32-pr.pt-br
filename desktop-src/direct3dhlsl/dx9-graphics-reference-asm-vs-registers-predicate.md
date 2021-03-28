---
title: Registro de predicado (referência de HLSL VS)
description: Este registro de saída do sombreador de vértice contém um valor booliano por canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104006940"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="50b15-103">Registro de predicado (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="50b15-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="50b15-104">Este registro de saída do sombreador de vértice contém um valor booliano por canal.</span><span class="sxs-lookup"><span data-stu-id="50b15-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="50b15-105">Um registro de predicado tem suporte nas seguintes versões.</span><span class="sxs-lookup"><span data-stu-id="50b15-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="50b15-106">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="50b15-106">Vertex shader versions</span></span> | <span data-ttu-id="50b15-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="50b15-107">1\_1</span></span> | <span data-ttu-id="50b15-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="50b15-108">2\_0</span></span> | <span data-ttu-id="50b15-109">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="50b15-109">2\_sw</span></span> | <span data-ttu-id="50b15-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="50b15-110">2\_x</span></span> | <span data-ttu-id="50b15-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="50b15-111">3\_0</span></span> | <span data-ttu-id="50b15-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="50b15-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="50b15-113">registro de predicado</span><span class="sxs-lookup"><span data-stu-id="50b15-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="50b15-114">x</span><span class="sxs-lookup"><span data-stu-id="50b15-114">x</span></span>    | <span data-ttu-id="50b15-115">x</span><span class="sxs-lookup"><span data-stu-id="50b15-115">x</span></span>    | <span data-ttu-id="50b15-116">x</span><span class="sxs-lookup"><span data-stu-id="50b15-116">x</span></span>     |



 

<span data-ttu-id="50b15-117">Aqui estão as propriedades do registro.</span><span class="sxs-lookup"><span data-stu-id="50b15-117">Here are the register properties.</span></span>



| <span data-ttu-id="50b15-118">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="50b15-118">Register type</span></span> | <span data-ttu-id="50b15-119">Contagem</span><span class="sxs-lookup"><span data-stu-id="50b15-119">Count</span></span> | <span data-ttu-id="50b15-120">R/W</span><span class="sxs-lookup"><span data-stu-id="50b15-120">R/W</span></span> | <span data-ttu-id="50b15-121">\# Portas de leitura</span><span class="sxs-lookup"><span data-stu-id="50b15-121">\# Read ports</span></span> | <span data-ttu-id="50b15-122">\# Leituras/InStr</span><span class="sxs-lookup"><span data-stu-id="50b15-122">\# Reads/inst</span></span> | <span data-ttu-id="50b15-123">Dimensão</span><span class="sxs-lookup"><span data-stu-id="50b15-123">Dimension</span></span> | <span data-ttu-id="50b15-124">RelAddr</span><span class="sxs-lookup"><span data-stu-id="50b15-124">RelAddr</span></span> | <span data-ttu-id="50b15-125">Padrões</span><span class="sxs-lookup"><span data-stu-id="50b15-125">Defaults</span></span> | <span data-ttu-id="50b15-126">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="50b15-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="50b15-127">Predicado (p)</span><span class="sxs-lookup"><span data-stu-id="50b15-127">Predicate(p)</span></span>  | <span data-ttu-id="50b15-128">1</span><span class="sxs-lookup"><span data-stu-id="50b15-128">1</span></span>     | <span data-ttu-id="50b15-129">R/W</span><span class="sxs-lookup"><span data-stu-id="50b15-129">R/W</span></span> | <span data-ttu-id="50b15-130">1</span><span class="sxs-lookup"><span data-stu-id="50b15-130">1</span></span>             | <span data-ttu-id="50b15-131">1</span><span class="sxs-lookup"><span data-stu-id="50b15-131">1</span></span>             | <span data-ttu-id="50b15-132">4</span><span class="sxs-lookup"><span data-stu-id="50b15-132">4</span></span>         | <span data-ttu-id="50b15-133">N/D</span><span class="sxs-lookup"><span data-stu-id="50b15-133">N/A</span></span>     | <span data-ttu-id="50b15-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="50b15-134">None</span></span>     | <span data-ttu-id="50b15-135">N</span><span class="sxs-lookup"><span data-stu-id="50b15-135">N</span></span>            |



 

<span data-ttu-id="50b15-136">O registro de predicado pode ser modificado com [setp \_ comp-vs](setp-comp---vs.md). Não há valores padrão para esse registro, um aplicativo precisa definir o registro antes de ser usado.</span><span class="sxs-lookup"><span data-stu-id="50b15-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50b15-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50b15-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b15-138">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="50b15-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




