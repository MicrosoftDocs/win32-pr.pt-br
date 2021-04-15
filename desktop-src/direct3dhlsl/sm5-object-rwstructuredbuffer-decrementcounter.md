---
title: 'RWStructuredBuffer: função ecrementCounter do:D (Httpserv. h)'
description: Decrementa o contador oculto do objeto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- HLSL da função DecrementCounter
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968644"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="16e67-104">Função DecrementCounter</span><span class="sxs-lookup"><span data-stu-id="16e67-104">DecrementCounter function</span></span>

<span data-ttu-id="16e67-105">Decrementa o contador oculto do objeto.</span><span class="sxs-lookup"><span data-stu-id="16e67-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e67-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e67-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="16e67-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16e67-107">Parameters</span></span>

<span data-ttu-id="16e67-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="16e67-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16e67-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="16e67-109">Return value</span></span>

<span data-ttu-id="16e67-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="16e67-110">Type: **uint**</span></span>

<span data-ttu-id="16e67-111">O valor do contador de pós-decrementado.</span><span class="sxs-lookup"><span data-stu-id="16e67-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e67-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="16e67-112">Remarks</span></span>

<span data-ttu-id="16e67-113">O modo de exibição de acesso não ordenado associado deve ter o [**\_ \_ \_ \_ contador de sinalizador UAV de buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) definido durante a creationfor desse método funcionar.</span><span class="sxs-lookup"><span data-stu-id="16e67-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="16e67-114">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="16e67-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="16e67-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="16e67-115">Vertex</span></span> | <span data-ttu-id="16e67-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="16e67-116">Hull</span></span> | <span data-ttu-id="16e67-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="16e67-117">Domain</span></span> | <span data-ttu-id="16e67-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="16e67-118">Geometry</span></span> | <span data-ttu-id="16e67-119">16x16</span><span class="sxs-lookup"><span data-stu-id="16e67-119">Pixel</span></span> | <span data-ttu-id="16e67-120">Computação</span><span class="sxs-lookup"><span data-stu-id="16e67-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="16e67-121">x</span><span class="sxs-lookup"><span data-stu-id="16e67-121">x</span></span>     | <span data-ttu-id="16e67-122">x</span><span class="sxs-lookup"><span data-stu-id="16e67-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="16e67-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16e67-123">Requirements</span></span>



| <span data-ttu-id="16e67-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e67-124">Requirement</span></span> | <span data-ttu-id="16e67-125">Valor</span><span class="sxs-lookup"><span data-stu-id="16e67-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16e67-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16e67-126">Header</span></span><br/> | <dl> <span data-ttu-id="16e67-127"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e67-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e67-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="16e67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e67-129">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="16e67-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="16e67-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="16e67-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

