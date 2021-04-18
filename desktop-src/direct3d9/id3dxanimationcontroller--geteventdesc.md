---
description: Obtém uma descrição de um evento de animação especificado.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'Método ID3DXAnimationController:: GetEventDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807942"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="17806-103">Método ID3DXAnimationController:: GetEventDesc</span><span class="sxs-lookup"><span data-stu-id="17806-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="17806-104">Obtém uma descrição de um evento de animação especificado.</span><span class="sxs-lookup"><span data-stu-id="17806-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="17806-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17806-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="17806-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17806-107">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17806-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17806-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="17806-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="17806-109">Identificador de evento para um evento de animação a ser descrito.</span><span class="sxs-lookup"><span data-stu-id="17806-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="17806-110">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17806-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17806-111">Tipo: **[ **LPD3DXEVENT \_ desc**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="17806-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="17806-112">Ponteiro para uma [**estrutura \_ desc de D3DXEVENT**](d3dxevent-desc.md) que contém uma descrição do evento de animação.</span><span class="sxs-lookup"><span data-stu-id="17806-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17806-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17806-113">Return value</span></span>

<span data-ttu-id="17806-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17806-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17806-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17806-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="17806-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17806-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17806-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17806-117">Requirements</span></span>



| <span data-ttu-id="17806-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17806-118">Requirement</span></span> | <span data-ttu-id="17806-119">Valor</span><span class="sxs-lookup"><span data-stu-id="17806-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17806-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17806-120">Header</span></span><br/>  | <dl> <span data-ttu-id="17806-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="17806-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="17806-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17806-122">Library</span></span><br/> | <dl> <span data-ttu-id="17806-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17806-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17806-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="17806-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17806-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="17806-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




