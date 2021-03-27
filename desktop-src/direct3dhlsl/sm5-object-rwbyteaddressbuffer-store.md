---
title: 'Função RWByteAddressBuffer:: Store'
description: Define um valor.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Função de armazenamento HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104967069"
---
# <a name="store-function"></a><span data-ttu-id="87685-104">Função Store</span><span class="sxs-lookup"><span data-stu-id="87685-104">Store function</span></span>

<span data-ttu-id="87685-105">Define um valor.</span><span class="sxs-lookup"><span data-stu-id="87685-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="87685-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87685-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="87685-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87685-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87685-108">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87685-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87685-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="87685-109">Type: **uint**</span></span>

<span data-ttu-id="87685-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="87685-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="87685-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="87685-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87685-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="87685-112">Type: **uint**</span></span>

<span data-ttu-id="87685-113">Um valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="87685-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87685-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87685-114">Return value</span></span>

<span data-ttu-id="87685-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="87685-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87685-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="87685-116">Remarks</span></span>

<span data-ttu-id="87685-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="87685-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="87685-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="87685-118">Vertex</span></span> | <span data-ttu-id="87685-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="87685-119">Hull</span></span> | <span data-ttu-id="87685-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="87685-120">Domain</span></span> | <span data-ttu-id="87685-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="87685-121">Geometry</span></span> | <span data-ttu-id="87685-122">16x16</span><span class="sxs-lookup"><span data-stu-id="87685-122">Pixel</span></span> | <span data-ttu-id="87685-123">Computação</span><span class="sxs-lookup"><span data-stu-id="87685-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="87685-124">x</span><span class="sxs-lookup"><span data-stu-id="87685-124">x</span></span>     | <span data-ttu-id="87685-125">x</span><span class="sxs-lookup"><span data-stu-id="87685-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="87685-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="87685-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87685-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="87685-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="87685-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="87685-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




