---
title: 'Função RWByteAddressBuffer:: Store4'
description: Define quatro valores.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- HLSL da função Store4
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104365091"
---
# <a name="store4-function"></a><span data-ttu-id="8dcc5-104">Função Store4</span><span class="sxs-lookup"><span data-stu-id="8dcc5-104">Store4 function</span></span>

<span data-ttu-id="8dcc5-105">Define quatro valores.</span><span class="sxs-lookup"><span data-stu-id="8dcc5-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dcc5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dcc5-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="8dcc5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dcc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dcc5-108">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8dcc5-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcc5-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8dcc5-109">Type: **uint**</span></span>

<span data-ttu-id="8dcc5-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="8dcc5-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="8dcc5-111">*valores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="8dcc5-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcc5-112">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="8dcc5-112">Type: **uint4**</span></span>

<span data-ttu-id="8dcc5-113">Quatro valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dcc5-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dcc5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dcc5-114">Return value</span></span>

<span data-ttu-id="8dcc5-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8dcc5-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dcc5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dcc5-116">Remarks</span></span>

<span data-ttu-id="8dcc5-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8dcc5-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8dcc5-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="8dcc5-118">Vertex</span></span> | <span data-ttu-id="8dcc5-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8dcc5-119">Hull</span></span> | <span data-ttu-id="8dcc5-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="8dcc5-120">Domain</span></span> | <span data-ttu-id="8dcc5-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="8dcc5-121">Geometry</span></span> | <span data-ttu-id="8dcc5-122">16x16</span><span class="sxs-lookup"><span data-stu-id="8dcc5-122">Pixel</span></span> | <span data-ttu-id="8dcc5-123">Computação</span><span class="sxs-lookup"><span data-stu-id="8dcc5-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8dcc5-124">x</span><span class="sxs-lookup"><span data-stu-id="8dcc5-124">x</span></span>     | <span data-ttu-id="8dcc5-125">x</span><span class="sxs-lookup"><span data-stu-id="8dcc5-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8dcc5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dcc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcc5-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="8dcc5-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="8dcc5-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8dcc5-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




