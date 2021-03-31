---
description: Retorna um identificador de evento para o próximo evento de mesclagem de prioridade agendado para ocorrer após um evento especificado.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Método ID3DXAnimationController:: GetUpcomingPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370918"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="a16df-103">Método ID3DXAnimationController:: GetUpcomingPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="a16df-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="a16df-104">Retorna um identificador de evento para o próximo evento de mesclagem de prioridade agendado para ocorrer após um evento especificado.</span><span class="sxs-lookup"><span data-stu-id="a16df-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a16df-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="a16df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a16df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16df-107">*hEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a16df-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a16df-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="a16df-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="a16df-109">Identificador de evento para um evento especificado após o qual procurar um evento de mesclagem de prioridade a seguir.</span><span class="sxs-lookup"><span data-stu-id="a16df-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="a16df-110">Se definido como **NULL**, o método retornará o próximo evento de mesclagem de prioridade agendado.</span><span class="sxs-lookup"><span data-stu-id="a16df-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16df-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a16df-111">Return value</span></span>

<span data-ttu-id="a16df-112">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="a16df-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="a16df-113">Identificador de evento para o próximo evento de mesclagem de prioridade agendado.</span><span class="sxs-lookup"><span data-stu-id="a16df-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="a16df-114">**NULL** será retornado se nenhum evento de mesclagem de prioridade novo estiver agendado.</span><span class="sxs-lookup"><span data-stu-id="a16df-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a16df-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a16df-115">Remarks</span></span>

<span data-ttu-id="a16df-116">Esse método pode ser usado iterativamente para localizar um evento de mesclagem de prioridade desejado, passando repetidamente em **NULL** para hEvent.</span><span class="sxs-lookup"><span data-stu-id="a16df-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="a16df-117">Não iterar mais após o método ter retornado **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a16df-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a16df-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a16df-118">Requirements</span></span>



| <span data-ttu-id="a16df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16df-119">Requirement</span></span> | <span data-ttu-id="a16df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a16df-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16df-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a16df-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a16df-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16df-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a16df-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a16df-123">Library</span></span><br/> | <dl> <span data-ttu-id="a16df-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a16df-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a16df-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a16df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16df-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a16df-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




