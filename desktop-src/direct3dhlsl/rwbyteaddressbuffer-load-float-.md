---
title: 'Função RWByteAddressBuffer:: Load (int)'
description: 'Obtém um valor. | Função RWByteAddressBuffer:: Load (int)'
ms.assetid: C95C865E-E44D-46DC-A076-BD2903758432
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
ms.openlocfilehash: 6efff2363f844e6940b489dd2dda48cbdc0c6b75
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968344"
---
# <a name="rwbyteaddressbufferloadint-function"></a><span data-ttu-id="ad9e0-105">Função RWByteAddressBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="ad9e0-105">RWByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="ad9e0-106">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="ad9e0-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad9e0-107">Syntax</span></span>


``` syntax
uint Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="ad9e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad9e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9e0-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad9e0-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9e0-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ad9e0-110">Type: **int**</span></span>

<span data-ttu-id="ad9e0-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="ad9e0-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9e0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad9e0-112">Return value</span></span>

<span data-ttu-id="ad9e0-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ad9e0-113">Type: **uint**</span></span>

<span data-ttu-id="ad9e0-114">Um valor.</span><span class="sxs-lookup"><span data-stu-id="ad9e0-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9e0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad9e0-115">Remarks</span></span>

<span data-ttu-id="ad9e0-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ad9e0-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ad9e0-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="ad9e0-117">Vertex</span></span> | <span data-ttu-id="ad9e0-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ad9e0-118">Hull</span></span> | <span data-ttu-id="ad9e0-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="ad9e0-119">Domain</span></span> | <span data-ttu-id="ad9e0-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="ad9e0-120">Geometry</span></span> | <span data-ttu-id="ad9e0-121">16x16</span><span class="sxs-lookup"><span data-stu-id="ad9e0-121">Pixel</span></span> | <span data-ttu-id="ad9e0-122">Computação</span><span class="sxs-lookup"><span data-stu-id="ad9e0-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ad9e0-123">x</span><span class="sxs-lookup"><span data-stu-id="ad9e0-123">x</span></span>     | <span data-ttu-id="ad9e0-124">x</span><span class="sxs-lookup"><span data-stu-id="ad9e0-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ad9e0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad9e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9e0-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="ad9e0-126">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 




