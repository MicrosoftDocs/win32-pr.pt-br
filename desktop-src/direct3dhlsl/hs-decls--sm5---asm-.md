---
title: hs_decls (SM5-ASM)
description: Inicie a fase de declarações em um sombreador envoltória.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084273"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="4e1dd-103">HS \_ decls (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e1dd-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="4e1dd-104">Inicie a fase de declarações em um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="4e1dd-105">HS \_ decls</span><span class="sxs-lookup"><span data-stu-id="4e1dd-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="4e1dd-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e1dd-106">Remarks</span></span>

<span data-ttu-id="4e1dd-107">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e1dd-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e1dd-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e1dd-108">Vertex</span></span> | <span data-ttu-id="4e1dd-109">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e1dd-109">Hull</span></span> | <span data-ttu-id="4e1dd-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e1dd-110">Domain</span></span> | <span data-ttu-id="4e1dd-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e1dd-111">Geometry</span></span> | <span data-ttu-id="4e1dd-112">16x16</span><span class="sxs-lookup"><span data-stu-id="4e1dd-112">Pixel</span></span> | <span data-ttu-id="4e1dd-113">Computação</span><span class="sxs-lookup"><span data-stu-id="4e1dd-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4e1dd-114">X</span><span class="sxs-lookup"><span data-stu-id="4e1dd-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e1dd-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e1dd-115">Minimum Shader Model</span></span>

<span data-ttu-id="4e1dd-116">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e1dd-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4e1dd-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e1dd-117">Shader Model</span></span>                                              | <span data-ttu-id="4e1dd-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1dd-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e1dd-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4e1dd-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e1dd-120">sim</span><span class="sxs-lookup"><span data-stu-id="4e1dd-120">yes</span></span>       |
| [<span data-ttu-id="4e1dd-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4e1dd-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e1dd-122">não</span><span class="sxs-lookup"><span data-stu-id="4e1dd-122">no</span></span>        |
| [<span data-ttu-id="4e1dd-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4e1dd-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e1dd-124">não</span><span class="sxs-lookup"><span data-stu-id="4e1dd-124">no</span></span>        |
| [<span data-ttu-id="4e1dd-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e1dd-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e1dd-126">não</span><span class="sxs-lookup"><span data-stu-id="4e1dd-126">no</span></span>        |
| [<span data-ttu-id="4e1dd-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e1dd-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e1dd-128">não</span><span class="sxs-lookup"><span data-stu-id="4e1dd-128">no</span></span>        |
| [<span data-ttu-id="4e1dd-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e1dd-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e1dd-130">não</span><span class="sxs-lookup"><span data-stu-id="4e1dd-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e1dd-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e1dd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e1dd-132">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e1dd-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




