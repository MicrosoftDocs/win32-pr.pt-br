---
description: Define uma chave de evento que altera o peso de uma faixa de animação. O peso é usado como um multiplicador ao combinar várias faixas juntas.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'Método ID3DXAnimationController:: KeyTrackWeight (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780700"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="db40c-103">Método ID3DXAnimationController:: KeyTrackWeight</span><span class="sxs-lookup"><span data-stu-id="db40c-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="db40c-104">Define uma chave de evento que altera o peso de uma faixa de animação. O peso é usado como um multiplicador ao combinar várias faixas juntas.</span><span class="sxs-lookup"><span data-stu-id="db40c-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="db40c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db40c-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="db40c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db40c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db40c-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db40c-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db40c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db40c-109">Identificador da faixa a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="db40c-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="db40c-110">*NewWeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db40c-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db40c-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db40c-112">Novo peso da faixa.</span><span class="sxs-lookup"><span data-stu-id="db40c-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="db40c-113">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db40c-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db40c-114">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db40c-115">Chave de tempo global.</span><span class="sxs-lookup"><span data-stu-id="db40c-115">Global time key.</span></span> <span data-ttu-id="db40c-116">Especifica a hora global em que a alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="db40c-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="db40c-117">*Duração* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db40c-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db40c-118">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db40c-119">Tempo de transição, que especifica por quanto tempo a transição suave levará para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="db40c-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="db40c-120">*Transição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db40c-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db40c-121">Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="db40c-122">Especifica o tipo de transição usado para fazer a transição entre pesos.</span><span class="sxs-lookup"><span data-stu-id="db40c-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="db40c-123">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="db40c-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db40c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db40c-124">Return value</span></span>

<span data-ttu-id="db40c-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="db40c-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="db40c-126">Identificador de evento para o evento de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="db40c-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="db40c-127">**NULL** será retornado se um ou mais dos parâmetros de entrada forem inválidos ou se nenhum evento gratuito estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="db40c-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="db40c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="db40c-128">Remarks</span></span>

<span data-ttu-id="db40c-129">O peso é usado como um multiplicador para determinar a quantidade desse controle a ser combinada com outras faixas.</span><span class="sxs-lookup"><span data-stu-id="db40c-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="db40c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db40c-130">Requirements</span></span>



| <span data-ttu-id="db40c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="db40c-131">Requirement</span></span> | <span data-ttu-id="db40c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="db40c-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db40c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db40c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="db40c-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="db40c-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="db40c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db40c-135">Library</span></span><br/> | <dl> <span data-ttu-id="db40c-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db40c-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db40c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="db40c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db40c-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="db40c-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
