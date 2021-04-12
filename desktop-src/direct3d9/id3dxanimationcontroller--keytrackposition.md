---
description: Define uma chave de evento que altera a hora local de uma faixa de animação.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Método ID3DXAnimationController:: KeyTrackPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298751"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="42dba-103">Método ID3DXAnimationController:: KeyTrackPosition</span><span class="sxs-lookup"><span data-stu-id="42dba-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="42dba-104">Define uma chave de evento que altera a hora local de uma faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="42dba-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42dba-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="42dba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42dba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dba-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42dba-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42dba-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42dba-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42dba-109">Identificador da faixa a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="42dba-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="42dba-110">*NewPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42dba-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42dba-111">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42dba-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42dba-112">Nova hora local da faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="42dba-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="42dba-113">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42dba-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42dba-114">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42dba-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42dba-115">Chave de tempo global.</span><span class="sxs-lookup"><span data-stu-id="42dba-115">Global time key.</span></span> <span data-ttu-id="42dba-116">Especifica a hora global em que a alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="42dba-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dba-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42dba-117">Return value</span></span>

<span data-ttu-id="42dba-118">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="42dba-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="42dba-119">Identificador de evento para o evento de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="42dba-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="42dba-120">**NULL** será retornado se Track for inválido ou se nenhum evento gratuito estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="42dba-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="42dba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42dba-121">Requirements</span></span>



| <span data-ttu-id="42dba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="42dba-122">Requirement</span></span> | <span data-ttu-id="42dba-123">Valor</span><span class="sxs-lookup"><span data-stu-id="42dba-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42dba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42dba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="42dba-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="42dba-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="42dba-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42dba-126">Library</span></span><br/> | <dl> <span data-ttu-id="42dba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42dba-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42dba-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="42dba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dba-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="42dba-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
