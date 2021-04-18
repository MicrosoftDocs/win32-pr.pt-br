---
description: Descreve uma faixa de animação e especifica o peso, a velocidade e a posição de mesclagem para a faixa em um determinado momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Estrutura de D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802053"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="65b07-103">\_Estrutura desc de D3DXTRACK</span><span class="sxs-lookup"><span data-stu-id="65b07-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="65b07-104">Descreve uma faixa de animação e especifica o peso, a velocidade e a posição de mesclagem para a faixa em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="65b07-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65b07-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="65b07-106">Membros</span><span class="sxs-lookup"><span data-stu-id="65b07-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65b07-107">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="65b07-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="65b07-108">Tipo: **[ **\_ tipo de D3DXPRIORITY**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="65b07-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65b07-109">Tipo de prioridade, conforme definido [**no \_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="65b07-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="65b07-110">**Weight**</span><span class="sxs-lookup"><span data-stu-id="65b07-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="65b07-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65b07-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65b07-112">Valor de peso.</span><span class="sxs-lookup"><span data-stu-id="65b07-112">Weight value.</span></span> <span data-ttu-id="65b07-113">O peso determina a proporção dessa faixa para misturar com outras faixas.</span><span class="sxs-lookup"><span data-stu-id="65b07-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-114">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="65b07-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="65b07-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65b07-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65b07-116">Valor de velocidade.</span><span class="sxs-lookup"><span data-stu-id="65b07-116">Speed value.</span></span> <span data-ttu-id="65b07-117">Isso é usado da mesma forma que um multiplicador para dimensionar o período da faixa.</span><span class="sxs-lookup"><span data-stu-id="65b07-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-118">**Posição**</span><span class="sxs-lookup"><span data-stu-id="65b07-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="65b07-119">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65b07-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65b07-120">Posição de hora da faixa, no período de tempo local do conjunto de animações atual.</span><span class="sxs-lookup"><span data-stu-id="65b07-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="65b07-121">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="65b07-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="65b07-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65b07-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="65b07-123">Controle habilitar/desabilitar.</span><span class="sxs-lookup"><span data-stu-id="65b07-123">Track enable/disable.</span></span> <span data-ttu-id="65b07-124">Para habilitar, defina como **true**.</span><span class="sxs-lookup"><span data-stu-id="65b07-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="65b07-125">Para desabilitar, defina como **false**.</span><span class="sxs-lookup"><span data-stu-id="65b07-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65b07-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="65b07-126">Remarks</span></span>

<span data-ttu-id="65b07-127">As faixas com a mesma prioridade são mescladas e os dois valores resultantes são mesclados usando o fator de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="65b07-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="65b07-128">Uma faixa deve ter uma animação definida (armazenada separadamente) associada a ela.</span><span class="sxs-lookup"><span data-stu-id="65b07-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b07-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b07-129">Requirements</span></span>



| <span data-ttu-id="65b07-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b07-130">Requirement</span></span> | <span data-ttu-id="65b07-131">Valor</span><span class="sxs-lookup"><span data-stu-id="65b07-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b07-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65b07-132">Header</span></span><br/> | <dl> <span data-ttu-id="65b07-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b07-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b07-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="65b07-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b07-135">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="65b07-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
