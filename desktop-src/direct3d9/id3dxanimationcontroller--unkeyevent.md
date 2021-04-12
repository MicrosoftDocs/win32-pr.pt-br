---
description: Remove um evento especificado de uma faixa de animação, impedindo a execução do evento.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'Método ID3DXAnimationController:: UnkeyEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298838"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="1df97-103">Método ID3DXAnimationController:: UnkeyEvent</span><span class="sxs-lookup"><span data-stu-id="1df97-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="1df97-104">Remove um evento especificado de uma faixa de animação, impedindo a execução do evento.</span><span class="sxs-lookup"><span data-stu-id="1df97-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1df97-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="1df97-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1df97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df97-107">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1df97-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df97-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="1df97-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="1df97-109">Identificador de evento para o evento a ser removido da faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="1df97-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df97-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1df97-110">Return value</span></span>

<span data-ttu-id="1df97-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1df97-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1df97-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1df97-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1df97-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1df97-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df97-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1df97-114">Requirements</span></span>



| <span data-ttu-id="1df97-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df97-115">Requirement</span></span> | <span data-ttu-id="1df97-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1df97-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1df97-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1df97-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1df97-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df97-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1df97-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1df97-119">Library</span></span><br/> | <dl> <span data-ttu-id="1df97-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1df97-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1df97-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1df97-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df97-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1df97-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




