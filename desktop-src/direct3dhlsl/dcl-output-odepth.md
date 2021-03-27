---
title: dcl_output oDepth (sm4-ASM)
description: '\_oDepth de saída DCL (sm4-ASM)'
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293598"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="8ab00-103">\_oDepth de saída DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8ab00-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="8ab00-104">Declara que um sombreador de pixel usará o registro de profundidade de saída.</span><span class="sxs-lookup"><span data-stu-id="8ab00-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="8ab00-105">oDepth de saída de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8ab00-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="8ab00-106">O valor no registro de profundidade de saída é usado durante uma comparação de profundidade (se a comparação de profundidade estiver habilitada).</span><span class="sxs-lookup"><span data-stu-id="8ab00-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="8ab00-107">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8ab00-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8ab00-108">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8ab00-108">Vertex Shader</span></span> | <span data-ttu-id="8ab00-109">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8ab00-109">Geometry Shader</span></span> | <span data-ttu-id="8ab00-110">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8ab00-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="8ab00-111">x</span><span class="sxs-lookup"><span data-stu-id="8ab00-111">x</span></span>            |



 

<span data-ttu-id="8ab00-112">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="8ab00-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="8ab00-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ab00-113">Example</span></span>

<span data-ttu-id="8ab00-114">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="8ab00-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8ab00-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8ab00-115">Minimum Shader Model</span></span>

<span data-ttu-id="8ab00-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ab00-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8ab00-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8ab00-117">Shader Model</span></span>                                              | <span data-ttu-id="8ab00-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8ab00-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8ab00-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8ab00-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8ab00-120">sim</span><span class="sxs-lookup"><span data-stu-id="8ab00-120">yes</span></span>       |
| [<span data-ttu-id="8ab00-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8ab00-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8ab00-122">sim</span><span class="sxs-lookup"><span data-stu-id="8ab00-122">yes</span></span>       |
| [<span data-ttu-id="8ab00-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8ab00-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8ab00-124">sim</span><span class="sxs-lookup"><span data-stu-id="8ab00-124">yes</span></span>       |
| [<span data-ttu-id="8ab00-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ab00-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8ab00-126">não</span><span class="sxs-lookup"><span data-stu-id="8ab00-126">no</span></span>        |
| [<span data-ttu-id="8ab00-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ab00-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8ab00-128">não</span><span class="sxs-lookup"><span data-stu-id="8ab00-128">no</span></span>        |
| [<span data-ttu-id="8ab00-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ab00-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8ab00-130">não</span><span class="sxs-lookup"><span data-stu-id="8ab00-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8ab00-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab00-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab00-132">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ab00-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




