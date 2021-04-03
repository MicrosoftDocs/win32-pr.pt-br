---
title: Mensagem de WM_XBUTTONUP (WinUser. h)
description: Postado quando o usuário libera o primeiro ou o segundo botão X enquanto o cursor está na área do cliente de uma janela.
ms.assetid: ad726859-368a-4603-bffa-4e639bc69a6a
keywords:
- Entrada de mouse e teclado de mensagem WM_XBUTTONUP
topic_type:
- apiref
api_name:
- WM_XBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 08/23/2019
ms.openlocfilehash: 521faefb2e2a76e94a0517c28a5fa812ef34ef5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918821"
---
# <a name="wm_xbuttonup-message"></a><span data-ttu-id="227c5-104">Mensagem do WM \_ XBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="227c5-104">WM\_XBUTTONUP message</span></span>

<span data-ttu-id="227c5-105">Postado quando o usuário libera o primeiro ou o segundo botão X enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="227c5-105">Posted when the user releases the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="227c5-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="227c5-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="227c5-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="227c5-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="227c5-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="227c5-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONUP                    0x020C
```



## <a name="parameters"></a><span data-ttu-id="227c5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="227c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227c5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="227c5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="227c5-111">A palavra de ordem inferior indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="227c5-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="227c5-112">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="227c5-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="227c5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="227c5-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="227c5-114">Significado</span><span class="sxs-lookup"><span data-stu-id="227c5-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="227c5-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="227c5-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="227c5-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="227c5-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="227c5-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="227c5-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="227c5-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="227c5-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="227c5-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="227c5-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="227c5-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="227c5-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="227c5-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="227c5-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="227c5-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="227c5-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="227c5-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="227c5-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="227c5-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="227c5-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="227c5-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="227c5-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="227c5-129">A palavra de ordem superior indica qual botão foi liberado.</span><span class="sxs-lookup"><span data-stu-id="227c5-129">The high-order word indicates which button was released.</span></span> <span data-ttu-id="227c5-130">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="227c5-130">It can be one of the following values:</span></span>



| <span data-ttu-id="227c5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="227c5-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="227c5-132">Significado</span><span class="sxs-lookup"><span data-stu-id="227c5-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="227c5-133"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="227c5-134">O primeiro botão X foi liberado.</span><span class="sxs-lookup"><span data-stu-id="227c5-134">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="227c5-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="227c5-136">O segundo botão X foi liberado.</span><span class="sxs-lookup"><span data-stu-id="227c5-136">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="227c5-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="227c5-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="227c5-138">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="227c5-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="227c5-139">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="227c5-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="227c5-140">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="227c5-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="227c5-141">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="227c5-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227c5-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="227c5-142">Return value</span></span>

<span data-ttu-id="227c5-143">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="227c5-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="227c5-144">Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="227c5-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="227c5-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="227c5-145">Remarks</span></span>

<span data-ttu-id="227c5-146">Use o código a seguir para obter as informações no parâmetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="227c5-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="227c5-147">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="227c5-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="227c5-148">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="227c5-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="227c5-149">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="227c5-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="227c5-150">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="227c5-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="227c5-151">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="227c5-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="227c5-152">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="227c5-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="227c5-153">Ao contrário das mensagens do [**WM \_ LBUTTONUP**](wm-lbuttonup.md), do [**WM \_ MBUTTONUP**](wm-mbuttonup.md)e do [**WM \_ RBUTTONUP**](wm-rbuttonup.md) , um aplicativo deve retornar **true** dessa mensagem se a processar.</span><span class="sxs-lookup"><span data-stu-id="227c5-153">Unlike the [**WM\_LBUTTONUP**](wm-lbuttonup.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), and [**WM\_RBUTTONUP**](wm-rbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="227c5-154">Isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.</span><span class="sxs-lookup"><span data-stu-id="227c5-154">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="227c5-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="227c5-155">Requirements</span></span>



| <span data-ttu-id="227c5-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="227c5-156">Requirement</span></span> | <span data-ttu-id="227c5-157">Valor</span><span class="sxs-lookup"><span data-stu-id="227c5-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="227c5-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="227c5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="227c5-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="227c5-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="227c5-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="227c5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="227c5-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="227c5-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="227c5-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="227c5-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="227c5-163"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="227c5-163"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="227c5-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="227c5-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="227c5-165">**Referência**</span><span class="sxs-lookup"><span data-stu-id="227c5-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="227c5-166">**OBTER \_ \_ wParam KeyState**</span><span class="sxs-lookup"><span data-stu-id="227c5-166">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="227c5-167">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="227c5-167">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="227c5-168">**OBTER \_ \_ wParam XBUTTON**</span><span class="sxs-lookup"><span data-stu-id="227c5-168">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="227c5-169">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="227c5-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="227c5-170">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="227c5-170">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="227c5-171">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="227c5-171">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="227c5-172">**XBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="227c5-172">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="227c5-173">**XBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="227c5-173">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

<span data-ttu-id="227c5-174">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="227c5-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="227c5-175">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="227c5-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="227c5-176">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="227c5-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="227c5-177">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="227c5-177">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="227c5-178">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="227c5-178">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

