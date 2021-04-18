---
description: O método PossiblyEatMessage encaminha as mensagens de teclado e mouse para a janela de drenagem de mensagem.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Método CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756204"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="3f9a2-103">Método CBaseControlWindow. PossiblyEatMessage</span><span class="sxs-lookup"><span data-stu-id="3f9a2-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="3f9a2-104">O `PossiblyEatMessage` método encaminha as mensagens de teclado e mouse para a janela de drenagem de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f9a2-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="3f9a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f9a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f9a2-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="3f9a2-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3f9a2-108">Mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="3f9a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f9a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f9a2-110">Primeiro parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3f9a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f9a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f9a2-112">Segundo parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f9a2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f9a2-113">Return value</span></span>

<span data-ttu-id="3f9a2-114">Retorna **true** se a mensagem foi encaminhada para a janela ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f9a2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f9a2-115">Remarks</span></span>

<span data-ttu-id="3f9a2-116">A janela de drenagem de mensagem é uma janela designada para receber determinadas mensagens de mouse e teclado.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="3f9a2-117">Inicialmente, a janela é **nula**; Ele pode ser definido chamando [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span><span class="sxs-lookup"><span data-stu-id="3f9a2-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="3f9a2-118">Se a janela de drenagem de mensagem não for **nula**, `PossiblyEatMessage` o posta as seguintes mensagens nessa janela:</span><span class="sxs-lookup"><span data-stu-id="3f9a2-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="3f9a2-119">caractere do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-119">WM\_CHAR</span></span>
-   <span data-ttu-id="3f9a2-120">DEADCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="3f9a2-121">o WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="3f9a2-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="3f9a2-122">o WM \_ KEYUP</span><span class="sxs-lookup"><span data-stu-id="3f9a2-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="3f9a2-123">LBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-124">LBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-125">LBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-126">MBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-127">MBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-128">MBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-129">MOUSEACTIVATE do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="3f9a2-130">admousemove do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="3f9a2-131">NCLBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-132">NCLBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-133">NCLBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-134">NCMBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-135">NCMBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-136">NCMBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-137">NCMOUSEMOVE do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="3f9a2-138">NCRBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-139">NCRBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-140">NCRBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-141">RBUTTONDBLCLK do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="3f9a2-142">RBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="3f9a2-143">RBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="3f9a2-144">SYSCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="3f9a2-145">SYSDEADCHAR do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="3f9a2-146">SYSKEYDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="3f9a2-147">SYSKEYUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="3f9a2-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="3f9a2-148">Ele ignora outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-148">It ignores other messages.</span></span> <span data-ttu-id="3f9a2-149">Se a janela de drenagem de mensagem for **nula**, o método ignorará todas as mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="3f9a2-150">O método retornará **true** se publicar a mensagem ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="3f9a2-151">A classe **CBaseWindow** chama esse método quando recebe uma mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="3f9a2-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f9a2-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f9a2-152">Requirements</span></span>



| <span data-ttu-id="3f9a2-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f9a2-153">Requirement</span></span> | <span data-ttu-id="3f9a2-154">Valor</span><span class="sxs-lookup"><span data-stu-id="3f9a2-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9a2-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f9a2-155">Header</span></span><br/>  | <dl> <span data-ttu-id="3f9a2-156"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f9a2-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f9a2-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f9a2-157">Library</span></span><br/> | <dl> <span data-ttu-id="3f9a2-158"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3f9a2-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f9a2-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f9a2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f9a2-160">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




