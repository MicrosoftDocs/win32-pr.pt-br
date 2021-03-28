---
title: 'Função ByteAddressBuffer:: GetDimensions'
description: 'Obtém o comprimento do buffer. | Função ByteAddressBuffer:: GetDimensions'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989136"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="4bdf9-105">Função ByteAddressBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="4bdf9-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="4bdf9-106">Obtém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdf9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bdf9-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="4bdf9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bdf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdf9-109">*esmaecer* \[\]</span><span class="sxs-lookup"><span data-stu-id="4bdf9-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdf9-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-110">Type: **uint**</span></span>

<span data-ttu-id="4bdf9-111">O comprimento, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdf9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4bdf9-112">Return value</span></span>

<span data-ttu-id="4bdf9-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bdf9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4bdf9-114">Remarks</span></span>

<span data-ttu-id="4bdf9-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4bdf9-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4bdf9-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="4bdf9-116">Vertex</span></span> | <span data-ttu-id="4bdf9-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4bdf9-117">Hull</span></span> | <span data-ttu-id="4bdf9-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="4bdf9-118">Domain</span></span> | <span data-ttu-id="4bdf9-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="4bdf9-119">Geometry</span></span> | <span data-ttu-id="4bdf9-120">16x16</span><span class="sxs-lookup"><span data-stu-id="4bdf9-120">Pixel</span></span> | <span data-ttu-id="4bdf9-121">Computação</span><span class="sxs-lookup"><span data-stu-id="4bdf9-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4bdf9-122">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-122">x</span></span>      | <span data-ttu-id="4bdf9-123">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-123">x</span></span>    | <span data-ttu-id="4bdf9-124">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-124">x</span></span>      | <span data-ttu-id="4bdf9-125">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-125">x</span></span>        | <span data-ttu-id="4bdf9-126">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-126">x</span></span>     | <span data-ttu-id="4bdf9-127">x</span><span class="sxs-lookup"><span data-stu-id="4bdf9-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4bdf9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4bdf9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdf9-129">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="4bdf9-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4bdf9-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




