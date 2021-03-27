---
title: clip
description: Descarta o pixel atual se o valor especificado for menor que zero.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- HLSL de clipe
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967192"
---
# <a name="clip"></a><span data-ttu-id="bee8b-104">clip</span><span class="sxs-lookup"><span data-stu-id="bee8b-104">clip</span></span>

<span data-ttu-id="bee8b-105">Descarta o pixel atual se o valor especificado for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="bee8b-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="bee8b-106">clipe (*x*)</span><span class="sxs-lookup"><span data-stu-id="bee8b-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="bee8b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bee8b-107">Parameters</span></span>



| <span data-ttu-id="bee8b-108">Item</span><span class="sxs-lookup"><span data-stu-id="bee8b-108">Item</span></span>                                                   | <span data-ttu-id="bee8b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bee8b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="bee8b-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="bee8b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bee8b-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="bee8b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bee8b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bee8b-112">Return Value</span></span>

<span data-ttu-id="bee8b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bee8b-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bee8b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bee8b-114">Remarks</span></span>

<span data-ttu-id="bee8b-115">Use a função intrínseca de **clip** HLSL para simular planos de recorte se cada componente do parâmetro *x* representar a distância de um plano.</span><span class="sxs-lookup"><span data-stu-id="bee8b-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="bee8b-116">Além disso, use a função **clip** para testar o comportamento alfa, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="bee8b-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="bee8b-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="bee8b-117">Type Description</span></span>



| <span data-ttu-id="bee8b-118">Name</span><span class="sxs-lookup"><span data-stu-id="bee8b-118">Name</span></span> | [<span data-ttu-id="bee8b-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="bee8b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bee8b-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="bee8b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bee8b-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bee8b-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="bee8b-122">*x*</span><span class="sxs-lookup"><span data-stu-id="bee8b-122">*x*</span></span>  | <span data-ttu-id="bee8b-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="bee8b-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bee8b-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="bee8b-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bee8b-125">any</span><span class="sxs-lookup"><span data-stu-id="bee8b-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bee8b-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bee8b-126">Minimum Shader Model</span></span>

<span data-ttu-id="bee8b-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bee8b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bee8b-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bee8b-128">Shader Model</span></span>                                              | <span data-ttu-id="bee8b-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bee8b-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="bee8b-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bee8b-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bee8b-131">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="bee8b-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="bee8b-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bee8b-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bee8b-133">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="bee8b-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="bee8b-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bee8b-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bee8b-135">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="bee8b-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="bee8b-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bee8b-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bee8b-137">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="bee8b-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bee8b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bee8b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee8b-139">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bee8b-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

