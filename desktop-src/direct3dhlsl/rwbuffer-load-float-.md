---
title: 'Função RWBuffer:: Load (int)'
description: 'Lê dados de buffer. | Função RWBuffer:: Load (int)'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663886"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="8a20a-105">Função RWBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="8a20a-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="8a20a-106">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="8a20a-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a20a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a20a-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="8a20a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a20a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a20a-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8a20a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a20a-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="8a20a-110">Type: **int**</span></span>

<span data-ttu-id="8a20a-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="8a20a-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a20a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a20a-112">Return value</span></span>

<span data-ttu-id="8a20a-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="8a20a-113">Type:</span></span>

<span data-ttu-id="8a20a-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8a20a-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a20a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a20a-115">Remarks</span></span>

<span data-ttu-id="8a20a-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8a20a-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8a20a-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="8a20a-117">Vertex</span></span> | <span data-ttu-id="8a20a-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8a20a-118">Hull</span></span> | <span data-ttu-id="8a20a-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="8a20a-119">Domain</span></span> | <span data-ttu-id="8a20a-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="8a20a-120">Geometry</span></span> | <span data-ttu-id="8a20a-121">16x16</span><span class="sxs-lookup"><span data-stu-id="8a20a-121">Pixel</span></span> | <span data-ttu-id="8a20a-122">Computação</span><span class="sxs-lookup"><span data-stu-id="8a20a-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8a20a-123">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-123">x</span></span>      | <span data-ttu-id="8a20a-124">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-124">x</span></span>    | <span data-ttu-id="8a20a-125">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-125">x</span></span>      | <span data-ttu-id="8a20a-126">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-126">x</span></span>        | <span data-ttu-id="8a20a-127">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-127">x</span></span>     | <span data-ttu-id="8a20a-128">x</span><span class="sxs-lookup"><span data-stu-id="8a20a-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8a20a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a20a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a20a-130">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="8a20a-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




