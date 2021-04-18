---
description: Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Método ID3DXAnimationController:: KeyTrackSpeed (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814133"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="6a6a1-103">Método ID3DXAnimationController:: KeyTrackSpeed</span><span class="sxs-lookup"><span data-stu-id="6a6a1-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="6a6a1-104">Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a6a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a6a1-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="6a6a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a6a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a6a1-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6a1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6a1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a6a1-109">Identificador da faixa a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="6a6a1-110">*NewSpeed* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6a1-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6a1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a6a1-112">Nova velocidade da faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="6a6a1-113">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6a1-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6a1-114">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a6a1-115">Chave de tempo global.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-115">Global time key.</span></span> <span data-ttu-id="6a6a1-116">Especifica a hora global em que a alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="6a6a1-117">*Duração* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6a1-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6a1-118">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a6a1-119">Tempo de transição, que especifica por quanto tempo a transição suave levará para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="6a6a1-120">*Transição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a6a1-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a6a1-121">Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="6a6a1-122">Especifica o tipo de transição usado para fazer a transição entre velocidades.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="6a6a1-123">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="6a6a1-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a6a1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a6a1-124">Return value</span></span>

<span data-ttu-id="6a6a1-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="6a6a1-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="6a6a1-126">Identificador de evento para o evento de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="6a6a1-127">**NULL** será retornado se um ou mais dos parâmetros de entrada forem inválidos ou se nenhum evento gratuito estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="6a6a1-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a6a1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a6a1-128">Requirements</span></span>



| <span data-ttu-id="6a6a1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a6a1-129">Requirement</span></span> | <span data-ttu-id="6a6a1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6a6a1-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6a1-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a6a1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6a6a1-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a6a1-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6a6a1-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a6a1-133">Library</span></span><br/> | <dl> <span data-ttu-id="6a6a1-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a6a1-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a6a1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a6a1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a6a1-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="6a6a1-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
