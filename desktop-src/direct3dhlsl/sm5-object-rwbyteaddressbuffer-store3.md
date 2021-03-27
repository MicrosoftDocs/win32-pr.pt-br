---
title: 'Função RWByteAddressBuffer:: Store3'
description: Define três valores.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- HLSL da função Store3
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293461"
---
# <a name="store3-function"></a><span data-ttu-id="b611d-104">Função Store3</span><span class="sxs-lookup"><span data-stu-id="b611d-104">Store3 function</span></span>

<span data-ttu-id="b611d-105">Define três valores.</span><span class="sxs-lookup"><span data-stu-id="b611d-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b611d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b611d-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="b611d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b611d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b611d-108">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b611d-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b611d-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b611d-109">Type: **uint**</span></span>

<span data-ttu-id="b611d-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="b611d-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="b611d-111">*valores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b611d-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b611d-112">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="b611d-112">Type: **uint3**</span></span>

<span data-ttu-id="b611d-113">Três valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="b611d-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b611d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b611d-114">Return value</span></span>

<span data-ttu-id="b611d-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b611d-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b611d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b611d-116">Remarks</span></span>

<span data-ttu-id="b611d-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b611d-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b611d-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="b611d-118">Vertex</span></span> | <span data-ttu-id="b611d-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b611d-119">Hull</span></span> | <span data-ttu-id="b611d-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="b611d-120">Domain</span></span> | <span data-ttu-id="b611d-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="b611d-121">Geometry</span></span> | <span data-ttu-id="b611d-122">16x16</span><span class="sxs-lookup"><span data-stu-id="b611d-122">Pixel</span></span> | <span data-ttu-id="b611d-123">Computação</span><span class="sxs-lookup"><span data-stu-id="b611d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b611d-124">x</span><span class="sxs-lookup"><span data-stu-id="b611d-124">x</span></span>     | <span data-ttu-id="b611d-125">x</span><span class="sxs-lookup"><span data-stu-id="b611d-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b611d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b611d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b611d-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="b611d-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="b611d-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b611d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




