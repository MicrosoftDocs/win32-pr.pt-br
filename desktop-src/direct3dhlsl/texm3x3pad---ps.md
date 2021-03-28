---
title: texm3x3pad-PS
description: Executa a primeira ou segunda linha multiplicada por uma multiplicação de três linhas. Essa instrução deve ser usada em combinação com texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS ou texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365224"
---
# <a name="texm3x3pad---ps"></a><span data-ttu-id="590de-104">texm3x3pad-PS</span><span class="sxs-lookup"><span data-stu-id="590de-104">texm3x3pad - ps</span></span>

<span data-ttu-id="590de-105">Executa a primeira ou segunda linha multiplicada por uma multiplicação de três linhas.</span><span class="sxs-lookup"><span data-stu-id="590de-105">Performs the first or second row multiply of a three-row matrix multiply.</span></span> <span data-ttu-id="590de-106">Essa instrução deve ser usada em combinação com [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)ou [texm3x3tex-PS](texm3x3tex---ps.md).</span><span class="sxs-lookup"><span data-stu-id="590de-106">This instruction must be used in combination with [texm3x3 - ps](texm3x3---ps.md), [texm3x3spec - ps](texm3x3spec---ps.md), [texm3x3vspec - ps](texm3x3vspec---ps.md), or [texm3x3tex - ps](texm3x3tex---ps.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="590de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="590de-107">Syntax</span></span>



| <span data-ttu-id="590de-108">texm3x3pad DST, src</span><span class="sxs-lookup"><span data-stu-id="590de-108">texm3x3pad dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="590de-109">onde</span><span class="sxs-lookup"><span data-stu-id="590de-109">where</span></span>

-   <span data-ttu-id="590de-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="590de-110">dst is the destination register.</span></span>
-   <span data-ttu-id="590de-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="590de-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="590de-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="590de-112">Remarks</span></span>



| <span data-ttu-id="590de-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="590de-113">Pixel shader versions</span></span> | <span data-ttu-id="590de-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="590de-114">1\_1</span></span> | <span data-ttu-id="590de-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="590de-115">1\_2</span></span> | <span data-ttu-id="590de-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="590de-116">1\_3</span></span> | <span data-ttu-id="590de-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="590de-117">1\_4</span></span> | <span data-ttu-id="590de-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="590de-118">2\_0</span></span> | <span data-ttu-id="590de-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="590de-119">2\_x</span></span> | <span data-ttu-id="590de-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="590de-120">2\_sw</span></span> | <span data-ttu-id="590de-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="590de-121">3\_0</span></span> | <span data-ttu-id="590de-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="590de-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="590de-123">texm3x3pad</span><span class="sxs-lookup"><span data-stu-id="590de-123">texm3x3pad</span></span>            | <span data-ttu-id="590de-124">x</span><span class="sxs-lookup"><span data-stu-id="590de-124">x</span></span>    | <span data-ttu-id="590de-125">x</span><span class="sxs-lookup"><span data-stu-id="590de-125">x</span></span>    | <span data-ttu-id="590de-126">x</span><span class="sxs-lookup"><span data-stu-id="590de-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="590de-127">Essa instrução não pode ser usada por si só.</span><span class="sxs-lookup"><span data-stu-id="590de-127">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="590de-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="590de-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="590de-129">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="590de-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




