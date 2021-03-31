---
description: Retorna um identificador de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Método ID3DXAnimationController:: GetUpcomingTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930550"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="8b22f-103">Método ID3DXAnimationController:: GetUpcomingTrackEvent</span><span class="sxs-lookup"><span data-stu-id="8b22f-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="8b22f-104">Retorna um identificador de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.</span><span class="sxs-lookup"><span data-stu-id="8b22f-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b22f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b22f-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="8b22f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b22f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b22f-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b22f-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b22f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b22f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b22f-109">Identificador de faixa.</span><span class="sxs-lookup"><span data-stu-id="8b22f-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8b22f-110">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b22f-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b22f-111">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8b22f-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8b22f-112">Identificador de evento para um evento especificado após o qual procurar um evento a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b22f-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="8b22f-113">Se definido como **NULL**, o método retornará o próximo evento agendado.</span><span class="sxs-lookup"><span data-stu-id="8b22f-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b22f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b22f-114">Return value</span></span>

<span data-ttu-id="8b22f-115">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8b22f-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8b22f-116">Identificador de evento para o próximo evento agendado para execução na faixa especificada. **NULL** será retornado se nenhum evento novo estiver agendado.</span><span class="sxs-lookup"><span data-stu-id="8b22f-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b22f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b22f-117">Remarks</span></span>

<span data-ttu-id="8b22f-118">Esse método pode ser usado iterativamente para localizar um evento desejado, passando repetidamente em **NULL** para hEvent.</span><span class="sxs-lookup"><span data-stu-id="8b22f-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="8b22f-119">Não iterar mais após o método ter retornado **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8b22f-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b22f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b22f-120">Requirements</span></span>



| <span data-ttu-id="8b22f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b22f-121">Requirement</span></span> | <span data-ttu-id="8b22f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8b22f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b22f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b22f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8b22f-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b22f-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8b22f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b22f-125">Library</span></span><br/> | <dl> <span data-ttu-id="8b22f-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b22f-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b22f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b22f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b22f-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8b22f-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
