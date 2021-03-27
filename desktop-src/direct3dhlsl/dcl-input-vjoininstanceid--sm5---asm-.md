---
title: dcl_input vJoinInstanceID (SM5-ASM)
description: Declare a ID da instância em uma fase de junção do sombreador envoltória.
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916888"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="82dce-103">\_vJoinInstanceID de entrada DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="82dce-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="82dce-104">Declare a ID da instância em uma fase de junção do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="82dce-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="82dce-105">\_vJoinInstanceID de entrada DCL</span><span class="sxs-lookup"><span data-stu-id="82dce-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="82dce-106">Item</span><span class="sxs-lookup"><span data-stu-id="82dce-106">Item</span></span>                                                                                                                               | <span data-ttu-id="82dce-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="82dce-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="82dce-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span><span class="sxs-lookup"><span data-stu-id="82dce-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="82dce-109">\[na \] ID da instância.</span><span class="sxs-lookup"><span data-stu-id="82dce-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82dce-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="82dce-110">Remarks</span></span>

<span data-ttu-id="82dce-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="82dce-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="82dce-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="82dce-112">Vertex</span></span> | <span data-ttu-id="82dce-113">Envoltória</span><span class="sxs-lookup"><span data-stu-id="82dce-113">Hull</span></span> | <span data-ttu-id="82dce-114">Domínio</span><span class="sxs-lookup"><span data-stu-id="82dce-114">Domain</span></span> | <span data-ttu-id="82dce-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="82dce-115">Geometry</span></span> | <span data-ttu-id="82dce-116">16x16</span><span class="sxs-lookup"><span data-stu-id="82dce-116">Pixel</span></span> | <span data-ttu-id="82dce-117">Computação</span><span class="sxs-lookup"><span data-stu-id="82dce-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="82dce-118">X</span><span class="sxs-lookup"><span data-stu-id="82dce-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82dce-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="82dce-119">Minimum Shader Model</span></span>

<span data-ttu-id="82dce-120">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="82dce-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="82dce-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="82dce-121">Shader Model</span></span>                                              | <span data-ttu-id="82dce-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="82dce-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="82dce-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="82dce-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="82dce-124">sim</span><span class="sxs-lookup"><span data-stu-id="82dce-124">yes</span></span>       |
| [<span data-ttu-id="82dce-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="82dce-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="82dce-126">não</span><span class="sxs-lookup"><span data-stu-id="82dce-126">no</span></span>        |
| [<span data-ttu-id="82dce-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="82dce-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82dce-128">não</span><span class="sxs-lookup"><span data-stu-id="82dce-128">no</span></span>        |
| [<span data-ttu-id="82dce-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82dce-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82dce-130">não</span><span class="sxs-lookup"><span data-stu-id="82dce-130">no</span></span>        |
| [<span data-ttu-id="82dce-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82dce-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82dce-132">não</span><span class="sxs-lookup"><span data-stu-id="82dce-132">no</span></span>        |
| [<span data-ttu-id="82dce-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82dce-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82dce-134">não</span><span class="sxs-lookup"><span data-stu-id="82dce-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="82dce-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82dce-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82dce-136">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82dce-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





