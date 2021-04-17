---
description: Ocorre quando um usuário clica no controle InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. Click (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784178"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="756ff-103">Evento InkEdit. Click</span><span class="sxs-lookup"><span data-stu-id="756ff-103">InkEdit.Click event</span></span>

<span data-ttu-id="756ff-104">Ocorre quando um usuário clica no controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="756ff-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="756ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="756ff-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="756ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="756ff-106">Parameters</span></span>

<span data-ttu-id="756ff-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="756ff-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="756ff-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="756ff-108">Return value</span></span>

<span data-ttu-id="756ff-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="756ff-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="756ff-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="756ff-110">Remarks</span></span>

<span data-ttu-id="756ff-111">Clicar em um controle gera eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) além do evento de clique.</span><span class="sxs-lookup"><span data-stu-id="756ff-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="756ff-112">Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="756ff-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="756ff-113">Se houver código no evento de **clique** , o evento [**DblClick**](inkedit-dblclick.md) nunca será disparado, pois o evento de **clique** é o primeiro evento a ser disparado entre os dois.</span><span class="sxs-lookup"><span data-stu-id="756ff-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="756ff-114">Como resultado, o clique do mouse é interceptado pelo evento de **clique** , portanto, o evento **DblClick** não ocorre.</span><span class="sxs-lookup"><span data-stu-id="756ff-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="756ff-115">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="756ff-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="756ff-116">A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeClick DISPID**.</span><span class="sxs-lookup"><span data-stu-id="756ff-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="756ff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756ff-117">Requirements</span></span>



| <span data-ttu-id="756ff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="756ff-118">Requirement</span></span> | <span data-ttu-id="756ff-119">Valor</span><span class="sxs-lookup"><span data-stu-id="756ff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756ff-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="756ff-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="756ff-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="756ff-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="756ff-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="756ff-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="756ff-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="756ff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="756ff-125"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="756ff-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="756ff-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="756ff-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="756ff-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756ff-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="756ff-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="756ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756ff-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="756ff-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




