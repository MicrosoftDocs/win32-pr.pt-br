---
title: dcl_immediateConstantBuffer (sm4-ASM)
description: DCL \_ immediateConstantBuffer (sm4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293602"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="85d4f-103">DCL \_ immediateConstantBuffer (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="85d4f-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="85d4f-104">Declara um buffer de constante de sombreador imediato.</span><span class="sxs-lookup"><span data-stu-id="85d4f-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="85d4f-105">\_ *valor (es) de immediateConstantBuffer de* DCL</span><span class="sxs-lookup"><span data-stu-id="85d4f-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="85d4f-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*valor (es)*</span><span class="sxs-lookup"><span data-stu-id="85d4f-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="85d4f-107">\[no \] buffer deve conter pelo menos um valor, mas não mais de 4096 valores.</span><span class="sxs-lookup"><span data-stu-id="85d4f-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="85d4f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="85d4f-108">Remarks</span></span>

<span data-ttu-id="85d4f-109">Um sombreador é permitido para um buffer de constante imediata.</span><span class="sxs-lookup"><span data-stu-id="85d4f-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="85d4f-110">Um buffer de constante imediata é acessado exatamente como um buffer constante com indexação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="85d4f-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="85d4f-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="85d4f-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="85d4f-112">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="85d4f-112">Vertex Shader</span></span> | <span data-ttu-id="85d4f-113">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="85d4f-113">Geometry Shader</span></span> | <span data-ttu-id="85d4f-114">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="85d4f-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="85d4f-115">x</span><span class="sxs-lookup"><span data-stu-id="85d4f-115">x</span></span>             | <span data-ttu-id="85d4f-116">x</span><span class="sxs-lookup"><span data-stu-id="85d4f-116">x</span></span>               | <span data-ttu-id="85d4f-117">x</span><span class="sxs-lookup"><span data-stu-id="85d4f-117">x</span></span>            |



 

<span data-ttu-id="85d4f-118">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="85d4f-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="85d4f-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="85d4f-119">Minimum Shader Model</span></span>

<span data-ttu-id="85d4f-120">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="85d4f-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85d4f-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="85d4f-121">Shader Model</span></span>                                              | <span data-ttu-id="85d4f-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="85d4f-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="85d4f-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="85d4f-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="85d4f-124">sim</span><span class="sxs-lookup"><span data-stu-id="85d4f-124">yes</span></span>       |
| [<span data-ttu-id="85d4f-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="85d4f-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="85d4f-126">sim</span><span class="sxs-lookup"><span data-stu-id="85d4f-126">yes</span></span>       |
| [<span data-ttu-id="85d4f-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="85d4f-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="85d4f-128">sim</span><span class="sxs-lookup"><span data-stu-id="85d4f-128">yes</span></span>       |
| [<span data-ttu-id="85d4f-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85d4f-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="85d4f-130">não</span><span class="sxs-lookup"><span data-stu-id="85d4f-130">no</span></span>        |
| [<span data-ttu-id="85d4f-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85d4f-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="85d4f-132">não</span><span class="sxs-lookup"><span data-stu-id="85d4f-132">no</span></span>        |
| [<span data-ttu-id="85d4f-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85d4f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="85d4f-134">não</span><span class="sxs-lookup"><span data-stu-id="85d4f-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="85d4f-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85d4f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85d4f-136">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85d4f-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




