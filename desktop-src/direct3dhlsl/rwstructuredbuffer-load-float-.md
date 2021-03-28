---
title: 'Função RWStructuredBuffer:: Load (int)'
description: 'Lê dados de buffer. | Função RWStructuredBuffer:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
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
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989154"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="245f9-105">Função RWStructuredBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="245f9-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="245f9-106">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="245f9-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="245f9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="245f9-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="245f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="245f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="245f9-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="245f9-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="245f9-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="245f9-110">Type: **int**</span></span>

<span data-ttu-id="245f9-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="245f9-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="245f9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="245f9-112">Return value</span></span>

<span data-ttu-id="245f9-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="245f9-113">Type:</span></span>

<span data-ttu-id="245f9-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="245f9-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="245f9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="245f9-115">Remarks</span></span>

<span data-ttu-id="245f9-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="245f9-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="245f9-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="245f9-117">Vertex</span></span> | <span data-ttu-id="245f9-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="245f9-118">Hull</span></span> | <span data-ttu-id="245f9-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="245f9-119">Domain</span></span> | <span data-ttu-id="245f9-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="245f9-120">Geometry</span></span> | <span data-ttu-id="245f9-121">16x16</span><span class="sxs-lookup"><span data-stu-id="245f9-121">Pixel</span></span> | <span data-ttu-id="245f9-122">Computação</span><span class="sxs-lookup"><span data-stu-id="245f9-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="245f9-123">x</span><span class="sxs-lookup"><span data-stu-id="245f9-123">x</span></span>      | <span data-ttu-id="245f9-124">x</span><span class="sxs-lookup"><span data-stu-id="245f9-124">x</span></span>    | <span data-ttu-id="245f9-125">x</span><span class="sxs-lookup"><span data-stu-id="245f9-125">x</span></span>      | <span data-ttu-id="245f9-126">x</span><span class="sxs-lookup"><span data-stu-id="245f9-126">x</span></span>        | <span data-ttu-id="245f9-127">x</span><span class="sxs-lookup"><span data-stu-id="245f9-127">x</span></span>     | <span data-ttu-id="245f9-128">x</span><span class="sxs-lookup"><span data-stu-id="245f9-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="245f9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="245f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245f9-130">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="245f9-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




