---
title: 'Função RWByteAddressBuffer:: Load3 (UINT)'
description: 'Obtém três valores. | Função RWByteAddressBuffer:: Load3 (UINT)'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- HLSL da função Load3
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968534"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="1ad5d-105">Função RWByteAddressBuffer:: Load3 (UINT)</span><span class="sxs-lookup"><span data-stu-id="1ad5d-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="1ad5d-106">Obtém três valores.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad5d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ad5d-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="1ad5d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ad5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad5d-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ad5d-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad5d-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1ad5d-110">Type: **uint**</span></span>

<span data-ttu-id="1ad5d-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad5d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ad5d-112">Return value</span></span>

<span data-ttu-id="1ad5d-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="1ad5d-113">Type: **uint3**</span></span>

<span data-ttu-id="1ad5d-114">Três valores.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad5d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ad5d-115">Remarks</span></span>

<span data-ttu-id="1ad5d-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1ad5d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1ad5d-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="1ad5d-117">Vertex</span></span> | <span data-ttu-id="1ad5d-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1ad5d-118">Hull</span></span> | <span data-ttu-id="1ad5d-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="1ad5d-119">Domain</span></span> | <span data-ttu-id="1ad5d-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="1ad5d-120">Geometry</span></span> | <span data-ttu-id="1ad5d-121">16x16</span><span class="sxs-lookup"><span data-stu-id="1ad5d-121">Pixel</span></span> | <span data-ttu-id="1ad5d-122">Computação</span><span class="sxs-lookup"><span data-stu-id="1ad5d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1ad5d-123">x</span><span class="sxs-lookup"><span data-stu-id="1ad5d-123">x</span></span>     | <span data-ttu-id="1ad5d-124">x</span><span class="sxs-lookup"><span data-stu-id="1ad5d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1ad5d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ad5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad5d-126">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="1ad5d-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="1ad5d-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1ad5d-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




