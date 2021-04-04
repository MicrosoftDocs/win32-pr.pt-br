---
title: Mensagem de WM_MBUTTONUP (WinUser. h)
description: Postado quando o usuário libera o botão do meio do mouse enquanto o cursor está na área do cliente de uma janela.
ms.assetid: fb8dee71-11bd-4405-855d-a5d120442271
keywords:
- Entrada de mouse e teclado de mensagem WM_MBUTTONUP
topic_type:
- apiref
api_name:
- WM_MBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7eb6b84c227934b5351a27ff8884fa78946ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009229"
---
# <a name="wm_mbuttonup-message"></a><span data-ttu-id="cd67e-104">Mensagem do WM \_ MBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="cd67e-104">WM\_MBUTTONUP message</span></span>

<span data-ttu-id="cd67e-105">Postado quando o usuário libera o botão do meio do mouse enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="cd67e-105">Posted when the user releases the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="cd67e-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="cd67e-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="cd67e-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="cd67e-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="cd67e-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cd67e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONUP                    0x0208
```



## <a name="parameters"></a><span data-ttu-id="cd67e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd67e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd67e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd67e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd67e-111">Indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="cd67e-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="cd67e-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd67e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cd67e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="cd67e-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="cd67e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="cd67e-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="cd67e-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="cd67e-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="cd67e-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="cd67e-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="cd67e-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="cd67e-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="cd67e-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="cd67e-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="cd67e-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="cd67e-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="cd67e-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="cd67e-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="cd67e-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="cd67e-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="cd67e-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="cd67e-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="cd67e-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="cd67e-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="cd67e-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="cd67e-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="cd67e-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="cd67e-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="cd67e-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd67e-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd67e-130">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="cd67e-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="cd67e-131">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="cd67e-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="cd67e-132">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="cd67e-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="cd67e-133">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="cd67e-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="cd67e-134">Observe que quando um menu de atalho está presente (exibido), as coordenadas são relativas à tela, não à área do cliente.</span><span class="sxs-lookup"><span data-stu-id="cd67e-134">Note that when a shortcut menu is present (displayed), coordinates are relative to the screen, not the client area.</span></span> <span data-ttu-id="cd67e-135">Como [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) é uma chamada assíncrona e a notificação do **\_ MBUTTONUP do WM** não tem um sinalizador especial indicando a derivação de coordenadas, um aplicativo não pode determinar se as coordenadas x, y contidas em *lParam* são relativas à tela ou à área do cliente.</span><span class="sxs-lookup"><span data-stu-id="cd67e-135">Because [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) is an asynchronous call and the **WM\_MBUTTONUP** notification does not have a special flag indicating coordinate derivation, an application cannot tell if the x,y coordinates contained in *lParam* are relative to the screen or the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd67e-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd67e-136">Return value</span></span>

<span data-ttu-id="cd67e-137">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="cd67e-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd67e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd67e-138">Remarks</span></span>

<span data-ttu-id="cd67e-139">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="cd67e-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="cd67e-140">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="cd67e-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="cd67e-141">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cd67e-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="cd67e-142">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="cd67e-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd67e-143">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="cd67e-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="cd67e-144">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="cd67e-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd67e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd67e-145">Requirements</span></span>



| <span data-ttu-id="cd67e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd67e-146">Requirement</span></span> | <span data-ttu-id="cd67e-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cd67e-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd67e-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd67e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cd67e-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd67e-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd67e-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd67e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cd67e-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd67e-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd67e-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cd67e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd67e-153"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd67e-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd67e-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd67e-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd67e-155">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cd67e-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd67e-156">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="cd67e-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="cd67e-157">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="cd67e-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="cd67e-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="cd67e-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="cd67e-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="cd67e-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="cd67e-160">**MBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd67e-160">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="cd67e-161">**MBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd67e-161">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
</dt> <dt>

<span data-ttu-id="cd67e-162">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cd67e-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cd67e-163">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="cd67e-163">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="cd67e-164">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="cd67e-164">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cd67e-165">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="cd67e-165">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="cd67e-166">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cd67e-166">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

