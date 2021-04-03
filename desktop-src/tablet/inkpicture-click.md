---
description: Ocorre quando um usuário clica no controle InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture. Click (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829694"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="38243-103">Evento InkPicture. Click</span><span class="sxs-lookup"><span data-stu-id="38243-103">InkPicture.Click event</span></span>

<span data-ttu-id="38243-104">Ocorre quando um usuário clica no controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="38243-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="38243-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38243-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="38243-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38243-106">Parameters</span></span>

<span data-ttu-id="38243-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="38243-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38243-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38243-108">Return value</span></span>

<span data-ttu-id="38243-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38243-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38243-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="38243-110">Remarks</span></span>

<span data-ttu-id="38243-111">Clicar em um controle gera eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) além do evento de clique.</span><span class="sxs-lookup"><span data-stu-id="38243-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="38243-112">Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="38243-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="38243-113">Se houver código no evento de **clique** , o evento [**DblClick**](inkpicture-dblclick.md) nunca será disparado, pois o evento de **clique** é o primeiro evento a ser disparado entre os dois.</span><span class="sxs-lookup"><span data-stu-id="38243-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="38243-114">Como resultado, o clique do mouse é interceptado pelo evento de **clique** , portanto, o evento **DblClick** não ocorre.</span><span class="sxs-lookup"><span data-stu-id="38243-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="38243-115">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="38243-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="38243-116">A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEClick DISPID**.</span><span class="sxs-lookup"><span data-stu-id="38243-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38243-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38243-117">Requirements</span></span>



| <span data-ttu-id="38243-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38243-118">Requirement</span></span> | <span data-ttu-id="38243-119">Valor</span><span class="sxs-lookup"><span data-stu-id="38243-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38243-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38243-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38243-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="38243-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="38243-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38243-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38243-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="38243-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="38243-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38243-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38243-125"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="38243-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="38243-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38243-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="38243-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38243-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="38243-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="38243-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38243-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="38243-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




