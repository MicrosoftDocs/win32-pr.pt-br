---
description: Retorna um identificador de evento para o evento em execução no momento na faixa de animação especificada.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Método ID3DXAnimationController:: GetCurrentTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789404"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="3a2c4-103">Método ID3DXAnimationController:: GetCurrentTrackEvent</span><span class="sxs-lookup"><span data-stu-id="3a2c4-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="3a2c4-104">Retorna um identificador de evento para o evento em execução no momento na faixa de animação especificada.</span><span class="sxs-lookup"><span data-stu-id="3a2c4-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a2c4-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="3a2c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a2c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2c4-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a2c4-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2c4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a2c4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a2c4-109">Identificador de faixa.</span><span class="sxs-lookup"><span data-stu-id="3a2c4-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3a2c4-110">*EventType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a2c4-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2c4-111">Tipo: **[ **\_ tipo de D3DXEVENT**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3a2c4-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="3a2c4-112">Tipo de evento a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="3a2c4-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2c4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a2c4-113">Return value</span></span>

<span data-ttu-id="3a2c4-114">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="3a2c4-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="3a2c4-115">Identificador de evento para o evento em execução no momento na faixa especificada. **NULL** será retornado se nenhum evento estiver em execução na faixa especificada.</span><span class="sxs-lookup"><span data-stu-id="3a2c4-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2c4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2c4-116">Requirements</span></span>



| <span data-ttu-id="3a2c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2c4-117">Requirement</span></span> | <span data-ttu-id="3a2c4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3a2c4-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2c4-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a2c4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3a2c4-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a2c4-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3a2c4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a2c4-121">Library</span></span><br/> | <dl> <span data-ttu-id="3a2c4-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a2c4-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a2c4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a2c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2c4-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="3a2c4-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
