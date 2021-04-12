---
description: Define uma chave de evento que habilita ou desabilita uma faixa de animação.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'Método ID3DXAnimationController:: KeyTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298500"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="f58c5-103">Método ID3DXAnimationController:: KeyTrackEnable</span><span class="sxs-lookup"><span data-stu-id="f58c5-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="f58c5-104">Define uma chave de evento que habilita ou desabilita uma faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="f58c5-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="f58c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f58c5-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="f58c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f58c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f58c5-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f58c5-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f58c5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f58c5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f58c5-109">Identificador da faixa de animação a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="f58c5-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="f58c5-110">*NewEnable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f58c5-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f58c5-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f58c5-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f58c5-112">Habilitar sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f58c5-112">Enable flag.</span></span> <span data-ttu-id="f58c5-113">Defina como **true** para habilitar a faixa de animação ou para **false** para desabilitar a faixa.</span><span class="sxs-lookup"><span data-stu-id="f58c5-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="f58c5-114">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f58c5-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f58c5-115">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f58c5-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f58c5-116">Chave de tempo global.</span><span class="sxs-lookup"><span data-stu-id="f58c5-116">Global time key.</span></span> <span data-ttu-id="f58c5-117">Especifica a hora global em que a alteração ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="f58c5-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f58c5-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f58c5-118">Return value</span></span>

<span data-ttu-id="f58c5-119">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f58c5-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f58c5-120">Identificador de evento para o evento de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="f58c5-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="f58c5-121">**NULL** será retornado se Track for inválido.</span><span class="sxs-lookup"><span data-stu-id="f58c5-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f58c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f58c5-122">Requirements</span></span>



| <span data-ttu-id="f58c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f58c5-123">Requirement</span></span> | <span data-ttu-id="f58c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f58c5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f58c5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f58c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f58c5-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f58c5-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f58c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f58c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="f58c5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f58c5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f58c5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f58c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f58c5-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f58c5-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
