---
title: 'Função ByteAddressBuffer:: Load4 (UINT)'
description: 'Obtém quatro valores. | Função ByteAddressBuffer:: Load4 (UINT)'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968494"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="6df0e-105">Função ByteAddressBuffer:: Load4 (UINT)</span><span class="sxs-lookup"><span data-stu-id="6df0e-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="6df0e-106">Obtém quatro valores.</span><span class="sxs-lookup"><span data-stu-id="6df0e-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df0e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df0e-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="6df0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df0e-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6df0e-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df0e-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6df0e-110">Type: **uint**</span></span>

<span data-ttu-id="6df0e-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="6df0e-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df0e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6df0e-112">Return value</span></span>

<span data-ttu-id="6df0e-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="6df0e-113">Type: **uint4**</span></span>

<span data-ttu-id="6df0e-114">Quatro valores.</span><span class="sxs-lookup"><span data-stu-id="6df0e-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df0e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6df0e-115">Remarks</span></span>

<span data-ttu-id="6df0e-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6df0e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6df0e-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="6df0e-117">Vertex</span></span> | <span data-ttu-id="6df0e-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6df0e-118">Hull</span></span> | <span data-ttu-id="6df0e-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="6df0e-119">Domain</span></span> | <span data-ttu-id="6df0e-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="6df0e-120">Geometry</span></span> | <span data-ttu-id="6df0e-121">16x16</span><span class="sxs-lookup"><span data-stu-id="6df0e-121">Pixel</span></span> | <span data-ttu-id="6df0e-122">Computação</span><span class="sxs-lookup"><span data-stu-id="6df0e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6df0e-123">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-123">x</span></span>      | <span data-ttu-id="6df0e-124">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-124">x</span></span>    | <span data-ttu-id="6df0e-125">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-125">x</span></span>      | <span data-ttu-id="6df0e-126">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-126">x</span></span>        | <span data-ttu-id="6df0e-127">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-127">x</span></span>     | <span data-ttu-id="6df0e-128">x</span><span class="sxs-lookup"><span data-stu-id="6df0e-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6df0e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6df0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df0e-130">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="6df0e-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="6df0e-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6df0e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




