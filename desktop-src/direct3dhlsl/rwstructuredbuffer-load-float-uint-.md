---
title: 'Função RWStructuredBuffer:: Load (int, uint)'
description: 'Lê os dados do buffer e retorna o status sobre a operação. | Função RWStructuredBuffer:: Load (int, uint)'
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
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
ms.openlocfilehash: 74a153d4b56ec16b80dec180287005666747d259
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968325"
---
# <a name="rwstructuredbufferloadintuint-function"></a><span data-ttu-id="b828f-105">Função RWStructuredBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="b828f-105">RWStructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="b828f-106">Lê os dados do buffer e retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="b828f-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b828f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b828f-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="b828f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b828f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b828f-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b828f-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b828f-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b828f-110">Type: **int**</span></span>

<span data-ttu-id="b828f-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="b828f-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b828f-112">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b828f-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b828f-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b828f-113">Type: **uint**</span></span>

<span data-ttu-id="b828f-114">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="b828f-114">The status of the operation.</span></span> <span data-ttu-id="b828f-115">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b828f-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b828f-116">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b828f-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b828f-117">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="b828f-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b828f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b828f-118">Return value</span></span>

<span data-ttu-id="b828f-119">Tipo:</span><span class="sxs-lookup"><span data-stu-id="b828f-119">Type:</span></span>

<span data-ttu-id="b828f-120">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b828f-120">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b828f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b828f-121">Remarks</span></span>

<span data-ttu-id="b828f-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b828f-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b828f-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="b828f-123">Vertex</span></span> | <span data-ttu-id="b828f-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b828f-124">Hull</span></span> | <span data-ttu-id="b828f-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="b828f-125">Domain</span></span> | <span data-ttu-id="b828f-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="b828f-126">Geometry</span></span> | <span data-ttu-id="b828f-127">16x16</span><span class="sxs-lookup"><span data-stu-id="b828f-127">Pixel</span></span> | <span data-ttu-id="b828f-128">Computação</span><span class="sxs-lookup"><span data-stu-id="b828f-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b828f-129">x</span><span class="sxs-lookup"><span data-stu-id="b828f-129">x</span></span>      | <span data-ttu-id="b828f-130">x</span><span class="sxs-lookup"><span data-stu-id="b828f-130">x</span></span>    | <span data-ttu-id="b828f-131">x</span><span class="sxs-lookup"><span data-stu-id="b828f-131">x</span></span>      | <span data-ttu-id="b828f-132">x</span><span class="sxs-lookup"><span data-stu-id="b828f-132">x</span></span>        | <span data-ttu-id="b828f-133">x</span><span class="sxs-lookup"><span data-stu-id="b828f-133">x</span></span>     | <span data-ttu-id="b828f-134">x</span><span class="sxs-lookup"><span data-stu-id="b828f-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b828f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b828f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b828f-136">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="b828f-136">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
