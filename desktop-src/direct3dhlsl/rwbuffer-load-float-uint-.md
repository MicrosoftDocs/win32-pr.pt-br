---
title: 'Função RWBuffer:: Load (int, uint)'
description: 'Lê os dados de buffer e retorna o status da operação. | Função RWBuffer:: Load (int, uint)'
ms.assetid: 90C9ECE8-2068-47C7-B87A-941B2D4F221D
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
ms.openlocfilehash: 81d23d67b0d02ed375e07f310089067d6a7bbd67
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091905"
---
# <a name="rwbufferloadintuint-function"></a><span data-ttu-id="17e14-105">Função RWBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="17e14-105">RWBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="17e14-106">Lê os dados de buffer e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="17e14-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17e14-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="17e14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17e14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e14-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="17e14-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e14-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="17e14-110">Type: **int**</span></span>

<span data-ttu-id="17e14-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="17e14-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="17e14-112">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="17e14-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17e14-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="17e14-113">Type: **uint**</span></span>

<span data-ttu-id="17e14-114">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="17e14-114">The status of the operation.</span></span> <span data-ttu-id="17e14-115">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="17e14-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="17e14-116">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="17e14-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="17e14-117">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="17e14-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e14-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17e14-118">Return value</span></span>

<span data-ttu-id="17e14-119">Tipo:</span><span class="sxs-lookup"><span data-stu-id="17e14-119">Type:</span></span>

<span data-ttu-id="17e14-120">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="17e14-120">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e14-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="17e14-121">Remarks</span></span>

<span data-ttu-id="17e14-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="17e14-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="17e14-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="17e14-123">Vertex</span></span> | <span data-ttu-id="17e14-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="17e14-124">Hull</span></span> | <span data-ttu-id="17e14-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="17e14-125">Domain</span></span> | <span data-ttu-id="17e14-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="17e14-126">Geometry</span></span> | <span data-ttu-id="17e14-127">16x16</span><span class="sxs-lookup"><span data-stu-id="17e14-127">Pixel</span></span> | <span data-ttu-id="17e14-128">Computação</span><span class="sxs-lookup"><span data-stu-id="17e14-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="17e14-129">x</span><span class="sxs-lookup"><span data-stu-id="17e14-129">x</span></span>      | <span data-ttu-id="17e14-130">x</span><span class="sxs-lookup"><span data-stu-id="17e14-130">x</span></span>    | <span data-ttu-id="17e14-131">x</span><span class="sxs-lookup"><span data-stu-id="17e14-131">x</span></span>      | <span data-ttu-id="17e14-132">x</span><span class="sxs-lookup"><span data-stu-id="17e14-132">x</span></span>        | <span data-ttu-id="17e14-133">x</span><span class="sxs-lookup"><span data-stu-id="17e14-133">x</span></span>     | <span data-ttu-id="17e14-134">x</span><span class="sxs-lookup"><span data-stu-id="17e14-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="17e14-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="17e14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e14-136">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="17e14-136">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 
