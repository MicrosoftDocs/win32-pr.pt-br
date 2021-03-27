---
title: 'Função ByteAddressBuffer:: Load (int)'
description: 'Obtém um valor. | Função ByteAddressBuffer:: Load (int)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989159"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="1118c-105">Função ByteAddressBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="1118c-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="1118c-106">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="1118c-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1118c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1118c-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="1118c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1118c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1118c-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1118c-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1118c-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1118c-110">Type: **int**</span></span>

<span data-ttu-id="1118c-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="1118c-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1118c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1118c-112">Return value</span></span>

<span data-ttu-id="1118c-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1118c-113">Type: **uint**</span></span>

<span data-ttu-id="1118c-114">Um valor.</span><span class="sxs-lookup"><span data-stu-id="1118c-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1118c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1118c-115">Remarks</span></span>

<span data-ttu-id="1118c-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1118c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1118c-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="1118c-117">Vertex</span></span> | <span data-ttu-id="1118c-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1118c-118">Hull</span></span> | <span data-ttu-id="1118c-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="1118c-119">Domain</span></span> | <span data-ttu-id="1118c-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="1118c-120">Geometry</span></span> | <span data-ttu-id="1118c-121">16x16</span><span class="sxs-lookup"><span data-stu-id="1118c-121">Pixel</span></span> | <span data-ttu-id="1118c-122">Computação</span><span class="sxs-lookup"><span data-stu-id="1118c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1118c-123">x</span><span class="sxs-lookup"><span data-stu-id="1118c-123">x</span></span>      | <span data-ttu-id="1118c-124">x</span><span class="sxs-lookup"><span data-stu-id="1118c-124">x</span></span>    | <span data-ttu-id="1118c-125">x</span><span class="sxs-lookup"><span data-stu-id="1118c-125">x</span></span>      | <span data-ttu-id="1118c-126">x</span><span class="sxs-lookup"><span data-stu-id="1118c-126">x</span></span>        | <span data-ttu-id="1118c-127">x</span><span class="sxs-lookup"><span data-stu-id="1118c-127">x</span></span>     | <span data-ttu-id="1118c-128">x</span><span class="sxs-lookup"><span data-stu-id="1118c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1118c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1118c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1118c-130">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="1118c-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="1118c-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1118c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




