---
description: Retorna um identificador de evento para um evento de combinação de prioridade que está em execução no momento.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'Método ID3DXAnimationController:: GetCurrentPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298808"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="ce6e2-103">Método ID3DXAnimationController:: GetCurrentPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="ce6e2-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="ce6e2-104">Retorna um identificador de evento para um evento de combinação de prioridade que está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce6e2-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="ce6e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce6e2-106">Parameters</span></span>

<span data-ttu-id="ce6e2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce6e2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce6e2-108">Return value</span></span>

<span data-ttu-id="ce6e2-109">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="ce6e2-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="ce6e2-110">Identificador de evento para o evento de combinação de prioridade em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="ce6e2-111">**NULL** será retornado se nenhum evento de prioridade de combinação estiver em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6e2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6e2-112">Requirements</span></span>



| <span data-ttu-id="ce6e2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6e2-113">Requirement</span></span> | <span data-ttu-id="ce6e2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ce6e2-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6e2-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce6e2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ce6e2-116"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6e2-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ce6e2-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce6e2-117">Library</span></span><br/> | <dl> <span data-ttu-id="ce6e2-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce6e2-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce6e2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce6e2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6e2-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ce6e2-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




