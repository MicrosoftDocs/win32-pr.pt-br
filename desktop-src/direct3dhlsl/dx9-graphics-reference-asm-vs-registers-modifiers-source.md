---
title: Modificadores de registro de origem do sombreador de vértice
description: Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364210"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="3e8dd-103">Modificadores de registro de origem do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8dd-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="3e8dd-104">Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="3e8dd-105">Negar</span><span class="sxs-lookup"><span data-stu-id="3e8dd-105">Negate</span></span>

<span data-ttu-id="3e8dd-106">Negar o conteúdo do registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="3e8dd-107">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="3e8dd-107">Component modifier</span></span> | <span data-ttu-id="3e8dd-108">Description</span><span class="sxs-lookup"><span data-stu-id="3e8dd-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="3e8dd-109">\- d</span><span class="sxs-lookup"><span data-stu-id="3e8dd-109">\- r</span></span>               | <span data-ttu-id="3e8dd-110">Negação de origem</span><span class="sxs-lookup"><span data-stu-id="3e8dd-110">Source negation</span></span> |



 

<span data-ttu-id="3e8dd-111">O modificador de negação não pode ser usado no segundo registro de origem dessas instruções: [M3X2-vs](m3x2---vs.md), [m3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [m4x4-vs](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="3e8dd-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="3e8dd-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8dd-112">Vertex shader versions</span></span> | <span data-ttu-id="3e8dd-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="3e8dd-113">1\_1</span></span> | <span data-ttu-id="3e8dd-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8dd-114">2\_0</span></span> | <span data-ttu-id="3e8dd-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-115">2\_x</span></span> | <span data-ttu-id="3e8dd-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8dd-116">2\_sw</span></span> | <span data-ttu-id="3e8dd-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8dd-117">3\_0</span></span> | <span data-ttu-id="3e8dd-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8dd-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="3e8dd-119">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-119">x</span></span>    | <span data-ttu-id="3e8dd-120">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-120">x</span></span>    | <span data-ttu-id="3e8dd-121">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-121">x</span></span>    | <span data-ttu-id="3e8dd-122">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-122">x</span></span>     | <span data-ttu-id="3e8dd-123">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-123">x</span></span>    | <span data-ttu-id="3e8dd-124">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="3e8dd-125">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="3e8dd-125">Absolute Value</span></span>

<span data-ttu-id="3e8dd-126">Pegue o valor absoluto do registro.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="3e8dd-127">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8dd-127">Vertex shader versions</span></span> | <span data-ttu-id="3e8dd-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="3e8dd-128">1\_1</span></span> | <span data-ttu-id="3e8dd-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8dd-129">2\_0</span></span> | <span data-ttu-id="3e8dd-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-130">2\_x</span></span> | <span data-ttu-id="3e8dd-131">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8dd-131">2\_sw</span></span> | <span data-ttu-id="3e8dd-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8dd-132">3\_0</span></span> | <span data-ttu-id="3e8dd-133">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8dd-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3e8dd-134">abs</span><span class="sxs-lookup"><span data-stu-id="3e8dd-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="3e8dd-135">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-135">x</span></span>    | <span data-ttu-id="3e8dd-136">x</span><span class="sxs-lookup"><span data-stu-id="3e8dd-136">x</span></span>     |



 

<span data-ttu-id="3e8dd-137">Se qualquer sombreador da versão 3 ler um ou mais registros de flutuação constante (c \# ), um dos seguintes deve ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="3e8dd-138">Todos os registros constantes de ponto flutuante devem usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="3e8dd-139">Nenhum dos registros constantes de ponto flutuante pode usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="3e8dd-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e8dd-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8dd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e8dd-141">Modificadores de registro do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8dd-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




