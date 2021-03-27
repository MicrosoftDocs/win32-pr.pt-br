---
title: dcl_function_body (SM5-ASM)
description: Declare um corpo de função.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084279"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="e3ceb-103">\_corpo da função DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e3ceb-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="e3ceb-104">Declare um corpo de função.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-104">Declare a function body.</span></span>



| <span data-ttu-id="e3ceb-105">\_corpo da função DCL \_ FB\#</span><span class="sxs-lookup"><span data-stu-id="e3ceb-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="e3ceb-106">Item</span><span class="sxs-lookup"><span data-stu-id="e3ceb-106">Item</span></span>                                                          | <span data-ttu-id="e3ceb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3ceb-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="e3ceb-108"><span id="fb_"></span><span id="FB_"></span>*FB\#*</span><span class="sxs-lookup"><span data-stu-id="e3ceb-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="e3ceb-109">\[no \] rótulo do local onde a função será exibida.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3ceb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3ceb-110">Remarks</span></span>

<span data-ttu-id="e3ceb-111">Essa instrução declara um corpo de função exclusivo cujo código será exibido posteriormente no programa no rótulo FB \# .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="e3ceb-112">Os corpos de função são usados em declarações de tabela de funções.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="e3ceb-113">Para obter mais informações, [consulte \_ \_ tabela de funções DCL](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="e3ceb-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="e3ceb-114">No sombreador envoltória e no sombreador de domínio, em que há várias fases (fase de ponto de controle, fase de bifurcação e fase de junção), todos os corpos de função (rótulo FB \# ) aparecem depois de todas as fases, em vez de serem agrupados por fase.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="e3ceb-115">Não há nenhum limite para quantos corpos de função podem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="e3ceb-116">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e3ceb-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e3ceb-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="e3ceb-117">Vertex</span></span> | <span data-ttu-id="e3ceb-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e3ceb-118">Hull</span></span> | <span data-ttu-id="e3ceb-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="e3ceb-119">Domain</span></span> | <span data-ttu-id="e3ceb-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="e3ceb-120">Geometry</span></span> | <span data-ttu-id="e3ceb-121">16x16</span><span class="sxs-lookup"><span data-stu-id="e3ceb-121">Pixel</span></span> | <span data-ttu-id="e3ceb-122">Computação</span><span class="sxs-lookup"><span data-stu-id="e3ceb-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e3ceb-123">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-123">X</span></span>      | <span data-ttu-id="e3ceb-124">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-124">X</span></span>    | <span data-ttu-id="e3ceb-125">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-125">X</span></span>      | <span data-ttu-id="e3ceb-126">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-126">X</span></span>        | <span data-ttu-id="e3ceb-127">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-127">X</span></span>     | <span data-ttu-id="e3ceb-128">X</span><span class="sxs-lookup"><span data-stu-id="e3ceb-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3ceb-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e3ceb-129">Minimum Shader Model</span></span>

<span data-ttu-id="e3ceb-130">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e3ceb-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e3ceb-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e3ceb-131">Shader Model</span></span>                                              | <span data-ttu-id="e3ceb-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e3ceb-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e3ceb-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e3ceb-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e3ceb-134">sim</span><span class="sxs-lookup"><span data-stu-id="e3ceb-134">yes</span></span>       |
| [<span data-ttu-id="e3ceb-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e3ceb-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e3ceb-136">não</span><span class="sxs-lookup"><span data-stu-id="e3ceb-136">no</span></span>        |
| [<span data-ttu-id="e3ceb-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e3ceb-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e3ceb-138">não</span><span class="sxs-lookup"><span data-stu-id="e3ceb-138">no</span></span>        |
| [<span data-ttu-id="e3ceb-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3ceb-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e3ceb-140">não</span><span class="sxs-lookup"><span data-stu-id="e3ceb-140">no</span></span>        |
| [<span data-ttu-id="e3ceb-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3ceb-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e3ceb-142">não</span><span class="sxs-lookup"><span data-stu-id="e3ceb-142">no</span></span>        |
| [<span data-ttu-id="e3ceb-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3ceb-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e3ceb-144">não</span><span class="sxs-lookup"><span data-stu-id="e3ceb-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e3ceb-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3ceb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ceb-146">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3ceb-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





