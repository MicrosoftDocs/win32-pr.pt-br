---
title: GetRenderTargetSamplePosition
description: Obtém a posição de amostragem (x,y) para um determinado índice de exemplo.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120571"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="fbbc1-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="fbbc1-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="fbbc1-105">Obtém a posição de amostragem (x,y) para um determinado índice de exemplo.</span><span class="sxs-lookup"><span data-stu-id="fbbc1-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="fbbc1-106">float<2> GetRenderTargetSamplePosition( int<1> Index</span><span class="sxs-lookup"><span data-stu-id="fbbc1-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="fbbc1-107">);</span><span class="sxs-lookup"><span data-stu-id="fbbc1-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="fbbc1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbbc1-108">Parameters</span></span>



| <span data-ttu-id="fbbc1-109">Item</span><span class="sxs-lookup"><span data-stu-id="fbbc1-109">Item</span></span>                                                                                       | <span data-ttu-id="fbbc1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbbc1-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="fbbc1-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Índice*</span><span class="sxs-lookup"><span data-stu-id="fbbc1-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="fbbc1-112">\[em \] Um índice de exemplo baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="fbbc1-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fbbc1-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fbbc1-113">Return Value</span></span>

<span data-ttu-id="fbbc1-114">A posição (x,y) do exemplo determinado.</span><span class="sxs-lookup"><span data-stu-id="fbbc1-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbbc1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbbc1-115">Remarks</span></span>

<span data-ttu-id="fbbc1-116">Use essa função e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) para descobrir o número e a posição dos locais de amostragem para um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="fbbc1-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fbbc1-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fbbc1-117">Minimum Shader Model</span></span>

<span data-ttu-id="fbbc1-118">Essa função tem suporte nos modelos de sombreador a seguir.</span><span class="sxs-lookup"><span data-stu-id="fbbc1-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fbbc1-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fbbc1-119">Shader Model</span></span>                                                        | <span data-ttu-id="fbbc1-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="fbbc1-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="fbbc1-121">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior</span><span class="sxs-lookup"><span data-stu-id="fbbc1-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="fbbc1-122">yes</span><span class="sxs-lookup"><span data-stu-id="fbbc1-122">yes</span></span>       |
| [<span data-ttu-id="fbbc1-123">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fbbc1-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="fbbc1-124">não</span><span class="sxs-lookup"><span data-stu-id="fbbc1-124">no</span></span>        |
| [<span data-ttu-id="fbbc1-125">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fbbc1-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="fbbc1-126">não</span><span class="sxs-lookup"><span data-stu-id="fbbc1-126">no</span></span>        |
| [<span data-ttu-id="fbbc1-127">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fbbc1-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="fbbc1-128">não</span><span class="sxs-lookup"><span data-stu-id="fbbc1-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="fbbc1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbbc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbc1-130">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fbbc1-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





