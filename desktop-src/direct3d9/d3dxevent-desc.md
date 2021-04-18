---
description: Descreve um evento de animação.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Estrutura de D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796116"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="d7d43-103">\_Estrutura desc de D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="d7d43-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="d7d43-104">Descreve um evento de animação.</span><span class="sxs-lookup"><span data-stu-id="d7d43-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7d43-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="d7d43-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d7d43-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7d43-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7d43-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-108">Tipo: **[ **\_ tipo de D3DXEVENT**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-109">Tipo de evento, conforme definido [**no \_ tipo D3DXEVENT**](./d3dxevent-type.md).</span><span class="sxs-lookup"><span data-stu-id="d7d43-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-110">**Rastrear**</span><span class="sxs-lookup"><span data-stu-id="d7d43-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-112">Identificador de faixa de eventos.</span><span class="sxs-lookup"><span data-stu-id="d7d43-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="d7d43-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-114">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-115">Hora de início do evento em tempo global.</span><span class="sxs-lookup"><span data-stu-id="d7d43-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-116">**Duration**</span><span class="sxs-lookup"><span data-stu-id="d7d43-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-117">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-118">Duração do evento em tempo global.</span><span class="sxs-lookup"><span data-stu-id="d7d43-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-119">**Transição**</span><span class="sxs-lookup"><span data-stu-id="d7d43-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-120">Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-121">Estilo de transição do evento, conforme definido no [**\_ tipo D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="d7d43-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-122">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d7d43-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-124">Controle o peso do evento.</span><span class="sxs-lookup"><span data-stu-id="d7d43-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-125">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="d7d43-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-127">Controlar a velocidade do evento.</span><span class="sxs-lookup"><span data-stu-id="d7d43-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-128">**Posição**</span><span class="sxs-lookup"><span data-stu-id="d7d43-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-129">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-130">Posição da faixa para o evento.</span><span class="sxs-lookup"><span data-stu-id="d7d43-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="d7d43-131">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="d7d43-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="d7d43-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7d43-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7d43-133">Habilitar sinalizador.</span><span class="sxs-lookup"><span data-stu-id="d7d43-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7d43-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7d43-134">Requirements</span></span>



| <span data-ttu-id="d7d43-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d43-135">Requirement</span></span> | <span data-ttu-id="d7d43-136">Valor</span><span class="sxs-lookup"><span data-stu-id="d7d43-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d43-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7d43-137">Header</span></span><br/> | <dl> <span data-ttu-id="d7d43-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d43-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d43-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7d43-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d43-140">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="d7d43-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
