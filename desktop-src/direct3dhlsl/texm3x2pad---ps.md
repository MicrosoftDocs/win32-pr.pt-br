---
title: texm3x2pad-PS
description: Executa a primeira multiplicação de linha de uma multiplicação de duas linhas. Essa instrução deve ser combinada com texm3x2tex-PS ou texm3x2depth-PS. Consulte uma destas instruções para obter detalhes sobre como usar o texmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823454"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="69f80-105">texm3x2pad-PS</span><span class="sxs-lookup"><span data-stu-id="69f80-105">texm3x2pad - ps</span></span>

<span data-ttu-id="69f80-106">Executa a primeira multiplicação de linha de uma multiplicação de duas linhas.</span><span class="sxs-lookup"><span data-stu-id="69f80-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="69f80-107">Essa instrução deve ser combinada com [texm3x2tex-PS](texm3x2tex---ps.md) ou [texm3x2depth-PS](texm3x2depth---ps.md).</span><span class="sxs-lookup"><span data-stu-id="69f80-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="69f80-108">Consulte uma destas instruções para obter detalhes sobre como usar o texmpad.</span><span class="sxs-lookup"><span data-stu-id="69f80-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f80-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f80-109">Syntax</span></span>



| <span data-ttu-id="69f80-110">tex3x2pad DST, src</span><span class="sxs-lookup"><span data-stu-id="69f80-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="69f80-111">onde</span><span class="sxs-lookup"><span data-stu-id="69f80-111">where</span></span>

-   <span data-ttu-id="69f80-112">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="69f80-112">dst is the destination register.</span></span>
-   <span data-ttu-id="69f80-113">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="69f80-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f80-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="69f80-114">Remarks</span></span>



| <span data-ttu-id="69f80-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="69f80-115">Pixel shader versions</span></span> | <span data-ttu-id="69f80-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="69f80-116">1\_1</span></span> | <span data-ttu-id="69f80-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="69f80-117">1\_2</span></span> | <span data-ttu-id="69f80-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="69f80-118">1\_3</span></span> | <span data-ttu-id="69f80-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="69f80-119">1\_4</span></span> | <span data-ttu-id="69f80-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69f80-120">2\_0</span></span> | <span data-ttu-id="69f80-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="69f80-121">2\_x</span></span> | <span data-ttu-id="69f80-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69f80-122">2\_sw</span></span> | <span data-ttu-id="69f80-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69f80-123">3\_0</span></span> | <span data-ttu-id="69f80-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69f80-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="69f80-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="69f80-125">texm3x2pad</span></span>            | <span data-ttu-id="69f80-126">x</span><span class="sxs-lookup"><span data-stu-id="69f80-126">x</span></span>    | <span data-ttu-id="69f80-127">x</span><span class="sxs-lookup"><span data-stu-id="69f80-127">x</span></span>    | <span data-ttu-id="69f80-128">x</span><span class="sxs-lookup"><span data-stu-id="69f80-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="69f80-129">Essa instrução não pode ser usada por si só.</span><span class="sxs-lookup"><span data-stu-id="69f80-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69f80-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69f80-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f80-131">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="69f80-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




