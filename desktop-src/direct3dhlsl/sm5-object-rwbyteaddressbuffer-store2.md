---
title: 'Função RWByteAddressBuffer:: Store2'
description: Define dois valores.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- HLSL da função Store2
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006788"
---
# <a name="store2-function"></a><span data-ttu-id="68e98-104">Função Store2</span><span class="sxs-lookup"><span data-stu-id="68e98-104">Store2 function</span></span>

<span data-ttu-id="68e98-105">Define dois valores.</span><span class="sxs-lookup"><span data-stu-id="68e98-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e98-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68e98-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="68e98-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68e98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e98-108">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68e98-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e98-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="68e98-109">Type: **uint**</span></span>

<span data-ttu-id="68e98-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="68e98-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="68e98-111">*valores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="68e98-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e98-112">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="68e98-112">Type: **uint2**</span></span>

<span data-ttu-id="68e98-113">Dois valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="68e98-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e98-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68e98-114">Return value</span></span>

<span data-ttu-id="68e98-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="68e98-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e98-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="68e98-116">Remarks</span></span>

<span data-ttu-id="68e98-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="68e98-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="68e98-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="68e98-118">Vertex</span></span> | <span data-ttu-id="68e98-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="68e98-119">Hull</span></span> | <span data-ttu-id="68e98-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="68e98-120">Domain</span></span> | <span data-ttu-id="68e98-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="68e98-121">Geometry</span></span> | <span data-ttu-id="68e98-122">16x16</span><span class="sxs-lookup"><span data-stu-id="68e98-122">Pixel</span></span> | <span data-ttu-id="68e98-123">Computação</span><span class="sxs-lookup"><span data-stu-id="68e98-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="68e98-124">x</span><span class="sxs-lookup"><span data-stu-id="68e98-124">x</span></span>     | <span data-ttu-id="68e98-125">x</span><span class="sxs-lookup"><span data-stu-id="68e98-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="68e98-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="68e98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e98-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="68e98-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="68e98-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="68e98-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




