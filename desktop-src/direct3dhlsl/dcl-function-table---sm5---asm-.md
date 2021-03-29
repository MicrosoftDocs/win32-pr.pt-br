---
title: dcl_function_table (SM5-ASM)
description: Declare uma tabela de funções.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988626"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="255eb-103">\_ \_ tabela de funções DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="255eb-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="255eb-104">Declare uma tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="255eb-104">Declare a function table.</span></span>



| <span data-ttu-id="255eb-105">\_ \_ tabela de função DCL ft \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="255eb-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="255eb-106">Item</span><span class="sxs-lookup"><span data-stu-id="255eb-106">Item</span></span>                                                      | <span data-ttu-id="255eb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="255eb-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="255eb-108"><span id="ft"></span><span id="FT"></span>*ft*</span><span class="sxs-lookup"><span data-stu-id="255eb-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="255eb-109">\[nas \] entradas da tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="255eb-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="255eb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="255eb-110">Remarks</span></span>

<span data-ttu-id="255eb-111">Essa função declara uma tabela de funções como um conjunto de corpos de função que foram declarados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="255eb-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="255eb-112">Isso é como um C++ vtable, exceto que há uma entrada por site de chamada para uma interface em vez de por método.</span><span class="sxs-lookup"><span data-stu-id="255eb-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="255eb-113">Não há nenhum limite para quantos corpos de função podem ser listados em uma tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="255eb-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="255eb-114">É válido para um determinado corpo de função FB \# ser referenciado várias vezes em uma ou mais tabelas de função, como um modo de compartilhar código comum.</span><span class="sxs-lookup"><span data-stu-id="255eb-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="255eb-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="255eb-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="255eb-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="255eb-116">Vertex</span></span> | <span data-ttu-id="255eb-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="255eb-117">Hull</span></span> | <span data-ttu-id="255eb-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="255eb-118">Domain</span></span> | <span data-ttu-id="255eb-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="255eb-119">Geometry</span></span> | <span data-ttu-id="255eb-120">16x16</span><span class="sxs-lookup"><span data-stu-id="255eb-120">Pixel</span></span> | <span data-ttu-id="255eb-121">Computação</span><span class="sxs-lookup"><span data-stu-id="255eb-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="255eb-122">X</span><span class="sxs-lookup"><span data-stu-id="255eb-122">X</span></span>      | <span data-ttu-id="255eb-123">X</span><span class="sxs-lookup"><span data-stu-id="255eb-123">X</span></span>    | <span data-ttu-id="255eb-124">X</span><span class="sxs-lookup"><span data-stu-id="255eb-124">X</span></span>      | <span data-ttu-id="255eb-125">X</span><span class="sxs-lookup"><span data-stu-id="255eb-125">X</span></span>        | <span data-ttu-id="255eb-126">X</span><span class="sxs-lookup"><span data-stu-id="255eb-126">X</span></span>     | <span data-ttu-id="255eb-127">X</span><span class="sxs-lookup"><span data-stu-id="255eb-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="255eb-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="255eb-128">Minimum Shader Model</span></span>

<span data-ttu-id="255eb-129">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="255eb-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="255eb-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="255eb-130">Shader Model</span></span>                                              | <span data-ttu-id="255eb-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="255eb-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="255eb-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="255eb-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="255eb-133">sim</span><span class="sxs-lookup"><span data-stu-id="255eb-133">yes</span></span>       |
| [<span data-ttu-id="255eb-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="255eb-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="255eb-135">não</span><span class="sxs-lookup"><span data-stu-id="255eb-135">no</span></span>        |
| [<span data-ttu-id="255eb-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="255eb-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="255eb-137">não</span><span class="sxs-lookup"><span data-stu-id="255eb-137">no</span></span>        |
| [<span data-ttu-id="255eb-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="255eb-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="255eb-139">não</span><span class="sxs-lookup"><span data-stu-id="255eb-139">no</span></span>        |
| [<span data-ttu-id="255eb-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="255eb-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="255eb-141">não</span><span class="sxs-lookup"><span data-stu-id="255eb-141">no</span></span>        |
| [<span data-ttu-id="255eb-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="255eb-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="255eb-143">não</span><span class="sxs-lookup"><span data-stu-id="255eb-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="255eb-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="255eb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="255eb-145">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="255eb-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





