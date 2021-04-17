---
description: Verifica se um identificador de evento especificado é válido e se o evento de animação ainda não foi concluído.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'Método ID3DXAnimationController:: ValidateEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752755"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="0be5d-103">Método ID3DXAnimationController:: ValidateEvent</span><span class="sxs-lookup"><span data-stu-id="0be5d-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="0be5d-104">Verifica se um identificador de evento especificado é válido e se o evento de animação ainda não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="0be5d-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be5d-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="0be5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0be5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be5d-107">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0be5d-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be5d-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="0be5d-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="0be5d-109">Identificador de evento para um evento de animação.</span><span class="sxs-lookup"><span data-stu-id="0be5d-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be5d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0be5d-110">Return value</span></span>

<span data-ttu-id="0be5d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0be5d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0be5d-112">Retornará S \_ OK se o identificador de evento for válido e o evento ainda não tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="0be5d-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="0be5d-113">Retornará E \_ falhará se o manipulador de eventos for inválido e/ou se o evento tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="0be5d-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0be5d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0be5d-114">Remarks</span></span>

<span data-ttu-id="0be5d-115">O método indicará que um identificador de evento é válido mesmo se o evento estiver em execução, mas ainda não tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="0be5d-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be5d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be5d-116">Requirements</span></span>



| <span data-ttu-id="0be5d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be5d-117">Requirement</span></span> | <span data-ttu-id="0be5d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0be5d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0be5d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be5d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0be5d-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be5d-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0be5d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0be5d-121">Library</span></span><br/> | <dl> <span data-ttu-id="0be5d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0be5d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0be5d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be5d-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0be5d-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




