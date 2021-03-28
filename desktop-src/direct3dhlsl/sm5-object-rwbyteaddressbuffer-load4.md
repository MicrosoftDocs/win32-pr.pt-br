---
title: 'Função RWByteAddressBuffer:: Load4 (UINT)'
description: 'Obtém quatro valores. | Função RWByteAddressBuffer:: Load4 (UINT)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- HLSL da função Load4
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968531"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="fdd41-105">Função RWByteAddressBuffer:: Load4 (UINT)</span><span class="sxs-lookup"><span data-stu-id="fdd41-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="fdd41-106">Obtém quatro valores.</span><span class="sxs-lookup"><span data-stu-id="fdd41-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdd41-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="fdd41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdd41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd41-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fdd41-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd41-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fdd41-110">Type: **uint**</span></span>

<span data-ttu-id="fdd41-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="fdd41-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd41-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdd41-112">Return value</span></span>

<span data-ttu-id="fdd41-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="fdd41-113">Type: **uint4**</span></span>

<span data-ttu-id="fdd41-114">Quatro valores.</span><span class="sxs-lookup"><span data-stu-id="fdd41-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd41-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd41-115">Remarks</span></span>

<span data-ttu-id="fdd41-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fdd41-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fdd41-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="fdd41-117">Vertex</span></span> | <span data-ttu-id="fdd41-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="fdd41-118">Hull</span></span> | <span data-ttu-id="fdd41-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="fdd41-119">Domain</span></span> | <span data-ttu-id="fdd41-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="fdd41-120">Geometry</span></span> | <span data-ttu-id="fdd41-121">16x16</span><span class="sxs-lookup"><span data-stu-id="fdd41-121">Pixel</span></span> | <span data-ttu-id="fdd41-122">Computação</span><span class="sxs-lookup"><span data-stu-id="fdd41-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fdd41-123">x</span><span class="sxs-lookup"><span data-stu-id="fdd41-123">x</span></span>     | <span data-ttu-id="fdd41-124">x</span><span class="sxs-lookup"><span data-stu-id="fdd41-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fdd41-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdd41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd41-126">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="fdd41-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="fdd41-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fdd41-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




