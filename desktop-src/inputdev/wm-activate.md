---
title: Mensagem de WM_ACTIVATE (WinUser. h)
description: Enviado para a janela que está sendo ativada e a janela sendo desativada.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Entrada de mouse e teclado de mensagem WM_ACTIVATE
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085427"
---
# <a name="wm_activate-message"></a><span data-ttu-id="bef84-104">Mensagem de ativação do WM \_</span><span class="sxs-lookup"><span data-stu-id="bef84-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="bef84-105">Enviado para a janela que está sendo ativada e a janela sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="bef84-106">Se as janelas usarem a mesma fila de entrada, a mensagem será enviada de forma síncrona, primeiro para o procedimento de janela da janela de nível superior sendo desativada, em seguida, para o procedimento de janela da janela de nível superior que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="bef84-107">Se as janelas usarem filas de entrada diferentes, a mensagem será enviada de forma assíncrona, de modo que a janela seja ativada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bef84-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="bef84-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bef84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bef84-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bef84-110">A palavra de ordem inferior Especifica se a janela está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="bef84-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bef84-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="bef84-112">A palavra de ordem superior especifica o estado minimizado da janela que está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="bef84-113">Um valor diferente de zero indica que a janela está minimizada.</span><span class="sxs-lookup"><span data-stu-id="bef84-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="bef84-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bef84-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="bef84-115">Significado</span><span class="sxs-lookup"><span data-stu-id="bef84-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="bef84-116"><dt>**Wa \_ ATIVO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bef84-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="bef84-117">Ativado por algum método que não seja um clique do mouse (por exemplo, por uma chamada para a função [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) ou pelo uso da interface do teclado para selecionar a janela).</span><span class="sxs-lookup"><span data-stu-id="bef84-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="bef84-118"><dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bef84-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="bef84-119">Ativado por um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="bef84-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="bef84-120"><dt>**Wa \_ Inativo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bef84-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="bef84-121">Desativado.</span><span class="sxs-lookup"><span data-stu-id="bef84-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="bef84-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bef84-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bef84-123">Um identificador para a janela que está sendo ativada ou desativada, dependendo do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="bef84-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="bef84-124">Se a palavra de ordem inferior de *wParam* for **wa \_ inativa**, *lParam* será o identificador para a janela que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="bef84-125">Se a palavra de ordem inferior de *wParam* for **wa \_ Active** ou **wa \_ CLICKACTIVE**, *lParam* será o identificador para a janela que está sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="bef84-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="bef84-126">Esse identificador pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bef84-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef84-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bef84-127">Return value</span></span>

<span data-ttu-id="bef84-128">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="bef84-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bef84-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="bef84-129">Remarks</span></span>

<span data-ttu-id="bef84-130">Se a janela estiver sendo ativada e não for minimizada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) definirá o foco do teclado para a janela.</span><span class="sxs-lookup"><span data-stu-id="bef84-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="bef84-131">Se a janela for ativada por um clique do mouse, ela também receberá uma mensagem do [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="bef84-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef84-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef84-132">Requirements</span></span>



| <span data-ttu-id="bef84-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef84-133">Requirement</span></span> | <span data-ttu-id="bef84-134">Valor</span><span class="sxs-lookup"><span data-stu-id="bef84-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef84-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef84-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bef84-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bef84-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bef84-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef84-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bef84-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bef84-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bef84-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bef84-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef84-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bef84-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef84-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="bef84-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="bef84-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bef84-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bef84-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bef84-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bef84-144">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="bef84-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="bef84-145">**MOUSEACTIVATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bef84-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="bef84-146">**NCACTIVATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bef84-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="bef84-147">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="bef84-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bef84-148">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="bef84-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

