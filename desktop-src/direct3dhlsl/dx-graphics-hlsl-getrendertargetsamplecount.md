---
title: GetRenderTargetSampleCount
description: Obtém o número de amostras de um destino de renderização.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453785"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="2d869-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="2d869-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="2d869-105">Obtém o número de amostras de um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="2d869-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="2d869-106">*Uint* GetRenderTargetSampleCount()</span><span class="sxs-lookup"><span data-stu-id="2d869-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2d869-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d869-107">Parameters</span></span>



| <span data-ttu-id="2d869-108">Item</span><span class="sxs-lookup"><span data-stu-id="2d869-108">Item</span></span>                                                                                 | <span data-ttu-id="2d869-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d869-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="2d869-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="2d869-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="2d869-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2d869-111">Return Value</span></span>

<span data-ttu-id="2d869-112">O número de amostras.</span><span class="sxs-lookup"><span data-stu-id="2d869-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d869-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d869-113">Remarks</span></span>

<span data-ttu-id="2d869-114">Use essa função e [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) para descobrir o número e a posição dos locais de amostragem para um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="2d869-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2d869-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2d869-115">Minimum Shader Model</span></span>

<span data-ttu-id="2d869-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d869-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2d869-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2d869-117">Shader Model</span></span>                                                        | <span data-ttu-id="2d869-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2d869-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="2d869-119">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="2d869-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="2d869-120">sim</span><span class="sxs-lookup"><span data-stu-id="2d869-120">yes</span></span>       |
| [<span data-ttu-id="2d869-121">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d869-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="2d869-122">não</span><span class="sxs-lookup"><span data-stu-id="2d869-122">no</span></span>        |
| [<span data-ttu-id="2d869-123">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d869-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="2d869-124">não</span><span class="sxs-lookup"><span data-stu-id="2d869-124">no</span></span>        |
| [<span data-ttu-id="2d869-125">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d869-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="2d869-126">não</span><span class="sxs-lookup"><span data-stu-id="2d869-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="2d869-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d869-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d869-128">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2d869-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





