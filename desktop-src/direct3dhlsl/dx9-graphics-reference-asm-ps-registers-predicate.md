---
title: Registro de predicado (referência do HLSL PS)
description: O registro de saída do sombreador de pixel contém um valor booliano por canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638912"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="8dab0-103">Registro de predicado (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="8dab0-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="8dab0-104">O registro de saída do sombreador de pixel contém um valor booliano por canal.</span><span class="sxs-lookup"><span data-stu-id="8dab0-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="8dab0-105">Um registro de predicado tem suporte nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="8dab0-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="8dab0-106">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8dab0-106">Pixel shader versions</span></span> | <span data-ttu-id="8dab0-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="8dab0-107">1\_1</span></span> | <span data-ttu-id="8dab0-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="8dab0-108">1\_2</span></span> | <span data-ttu-id="8dab0-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8dab0-109">1\_3</span></span> | <span data-ttu-id="8dab0-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="8dab0-110">1\_4</span></span> | <span data-ttu-id="8dab0-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8dab0-111">2\_0</span></span> | <span data-ttu-id="8dab0-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8dab0-112">2\_sw</span></span> | <span data-ttu-id="8dab0-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8dab0-113">2\_x</span></span> | <span data-ttu-id="8dab0-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8dab0-114">3\_0</span></span> | <span data-ttu-id="8dab0-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8dab0-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="8dab0-116">registro de predicado</span><span class="sxs-lookup"><span data-stu-id="8dab0-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="8dab0-117">x</span><span class="sxs-lookup"><span data-stu-id="8dab0-117">x</span></span>    | <span data-ttu-id="8dab0-118">x</span><span class="sxs-lookup"><span data-stu-id="8dab0-118">x</span></span>    | <span data-ttu-id="8dab0-119">x</span><span class="sxs-lookup"><span data-stu-id="8dab0-119">x</span></span>     |



 

<span data-ttu-id="8dab0-120">Aqui estão as propriedades do registro.</span><span class="sxs-lookup"><span data-stu-id="8dab0-120">Here are the register properties.</span></span>



| <span data-ttu-id="8dab0-121">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="8dab0-121">Register type</span></span> | <span data-ttu-id="8dab0-122">Contagem</span><span class="sxs-lookup"><span data-stu-id="8dab0-122">Count</span></span> | <span data-ttu-id="8dab0-123">R/W</span><span class="sxs-lookup"><span data-stu-id="8dab0-123">R/W</span></span> | <span data-ttu-id="8dab0-124">\# Portas de leitura</span><span class="sxs-lookup"><span data-stu-id="8dab0-124">\# Read ports</span></span> | <span data-ttu-id="8dab0-125">\# Leituras/InStr</span><span class="sxs-lookup"><span data-stu-id="8dab0-125">\# Reads/inst</span></span> | <span data-ttu-id="8dab0-126">Dimensão</span><span class="sxs-lookup"><span data-stu-id="8dab0-126">Dimension</span></span> | <span data-ttu-id="8dab0-127">RelAddr</span><span class="sxs-lookup"><span data-stu-id="8dab0-127">RelAddr</span></span> | <span data-ttu-id="8dab0-128">Padrões</span><span class="sxs-lookup"><span data-stu-id="8dab0-128">Defaults</span></span> | <span data-ttu-id="8dab0-129">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="8dab0-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="8dab0-130">Predicado (p)</span><span class="sxs-lookup"><span data-stu-id="8dab0-130">Predicate(p)</span></span>  | <span data-ttu-id="8dab0-131">1</span><span class="sxs-lookup"><span data-stu-id="8dab0-131">1</span></span>     | <span data-ttu-id="8dab0-132">R/W</span><span class="sxs-lookup"><span data-stu-id="8dab0-132">R/W</span></span> | <span data-ttu-id="8dab0-133">1</span><span class="sxs-lookup"><span data-stu-id="8dab0-133">1</span></span>             | <span data-ttu-id="8dab0-134">1</span><span class="sxs-lookup"><span data-stu-id="8dab0-134">1</span></span>             | <span data-ttu-id="8dab0-135">4</span><span class="sxs-lookup"><span data-stu-id="8dab0-135">4</span></span>         | <span data-ttu-id="8dab0-136">N/D</span><span class="sxs-lookup"><span data-stu-id="8dab0-136">N/A</span></span>     | <span data-ttu-id="8dab0-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8dab0-137">None</span></span>     | <span data-ttu-id="8dab0-138">N</span><span class="sxs-lookup"><span data-stu-id="8dab0-138">N</span></span>            |



 

<span data-ttu-id="8dab0-139">O registro de predicado pode ser modificado com [setp \_ comp-PS](setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="8dab0-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="8dab0-140">Não há valores padrão para este registro; um aplicativo precisa definir o registro antes que ele seja usado.</span><span class="sxs-lookup"><span data-stu-id="8dab0-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dab0-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dab0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dab0-142">Register</span><span class="sxs-lookup"><span data-stu-id="8dab0-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




