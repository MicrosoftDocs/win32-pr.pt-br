---
title: dcl_input vPrim (sm4-ASM)
description: '\_vPrim de entrada DCL (sm4-ASM)'
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365293"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="a2f30-103">\_vPrim de entrada DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a2f30-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="a2f30-104">Declara que um sombreador de geometria usa seu vPrim de registro de entrada escalar.</span><span class="sxs-lookup"><span data-stu-id="a2f30-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="a2f30-105">\_ *vPrim* de entrada DCL</span><span class="sxs-lookup"><span data-stu-id="a2f30-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="a2f30-106">Item</span><span class="sxs-lookup"><span data-stu-id="a2f30-106">Item</span></span>                                                                                       | <span data-ttu-id="a2f30-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2f30-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f30-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span><span class="sxs-lookup"><span data-stu-id="a2f30-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="a2f30-109">\[em \] um escalar de 32 bits, que pode ser aplicado a cada primitiva interior em um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="a2f30-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="a2f30-110">O escalar não pode ser aplicado a nenhum primitivo adjacente.</span><span class="sxs-lookup"><span data-stu-id="a2f30-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="a2f30-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a2f30-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a2f30-112">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a2f30-112">Vertex Shader</span></span> | <span data-ttu-id="a2f30-113">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="a2f30-113">Geometry Shader</span></span> | <span data-ttu-id="a2f30-114">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a2f30-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="a2f30-115">x</span><span class="sxs-lookup"><span data-stu-id="a2f30-115">x</span></span>               |              |



 

<span data-ttu-id="a2f30-116">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="a2f30-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="a2f30-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a2f30-117">Minimum Shader Model</span></span>

<span data-ttu-id="a2f30-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a2f30-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a2f30-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a2f30-119">Shader Model</span></span>                                              | <span data-ttu-id="a2f30-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a2f30-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a2f30-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a2f30-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a2f30-122">sim</span><span class="sxs-lookup"><span data-stu-id="a2f30-122">yes</span></span>       |
| [<span data-ttu-id="a2f30-123">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a2f30-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a2f30-124">sim</span><span class="sxs-lookup"><span data-stu-id="a2f30-124">yes</span></span>       |
| [<span data-ttu-id="a2f30-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a2f30-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a2f30-126">sim</span><span class="sxs-lookup"><span data-stu-id="a2f30-126">yes</span></span>       |
| [<span data-ttu-id="a2f30-127">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2f30-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a2f30-128">não</span><span class="sxs-lookup"><span data-stu-id="a2f30-128">no</span></span>        |
| [<span data-ttu-id="a2f30-129">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2f30-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a2f30-130">não</span><span class="sxs-lookup"><span data-stu-id="a2f30-130">no</span></span>        |
| [<span data-ttu-id="a2f30-131">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2f30-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a2f30-132">não</span><span class="sxs-lookup"><span data-stu-id="a2f30-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a2f30-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2f30-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f30-134">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2f30-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





