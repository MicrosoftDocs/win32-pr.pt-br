---
title: 'Função RWStructuredBuffer:: IncrementCounter (Httpserv. h)'
description: Incrementa o contador oculto do objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- HLSL da função IncrementCounter
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298748"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="afa21-104">Função IncrementCounter</span><span class="sxs-lookup"><span data-stu-id="afa21-104">IncrementCounter function</span></span>

<span data-ttu-id="afa21-105">Incrementa o contador oculto do objeto.</span><span class="sxs-lookup"><span data-stu-id="afa21-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa21-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afa21-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="afa21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afa21-107">Parameters</span></span>

<span data-ttu-id="afa21-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="afa21-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afa21-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="afa21-109">Return value</span></span>

<span data-ttu-id="afa21-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="afa21-110">Type: **uint**</span></span>

<span data-ttu-id="afa21-111">O valor do contador incrementado previamente.</span><span class="sxs-lookup"><span data-stu-id="afa21-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="afa21-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="afa21-112">Remarks</span></span>

<span data-ttu-id="afa21-113">O modo de exibição de acesso não ordenado associado deve ter o [**\_ \_ \_ \_ contador de sinalizador UAV de buffer de D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) definido durante a criação para que esse método funcione.</span><span class="sxs-lookup"><span data-stu-id="afa21-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="afa21-114">Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.</span><span class="sxs-lookup"><span data-stu-id="afa21-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="afa21-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="afa21-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="afa21-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="afa21-116">Vertex</span></span> | <span data-ttu-id="afa21-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="afa21-117">Hull</span></span> | <span data-ttu-id="afa21-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="afa21-118">Domain</span></span> | <span data-ttu-id="afa21-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="afa21-119">Geometry</span></span> | <span data-ttu-id="afa21-120">16x16</span><span class="sxs-lookup"><span data-stu-id="afa21-120">Pixel</span></span> | <span data-ttu-id="afa21-121">Computação</span><span class="sxs-lookup"><span data-stu-id="afa21-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="afa21-122">x</span><span class="sxs-lookup"><span data-stu-id="afa21-122">x</span></span>     | <span data-ttu-id="afa21-123">x</span><span class="sxs-lookup"><span data-stu-id="afa21-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="afa21-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afa21-124">Requirements</span></span>



| <span data-ttu-id="afa21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa21-125">Requirement</span></span> | <span data-ttu-id="afa21-126">Valor</span><span class="sxs-lookup"><span data-stu-id="afa21-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afa21-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="afa21-127">Header</span></span><br/> | <dl> <span data-ttu-id="afa21-128"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa21-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa21-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="afa21-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa21-130">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="afa21-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="afa21-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="afa21-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

