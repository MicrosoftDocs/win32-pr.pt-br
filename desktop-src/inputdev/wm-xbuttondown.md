---
title: Mensagem de WM_XBUTTONDOWN (WinUser. h)
description: Postado quando o usuário pressiona o primeiro ou o segundo botão X enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 4d972841-1513-4925-9d59-2557233561a2
keywords:
- Entrada de mouse e teclado de mensagem WM_XBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_XBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976a5f3d7282853b5267b0b1640a7a95120efbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455558"
---
# <a name="wm_xbuttondown-message"></a><span data-ttu-id="08375-104">Mensagem do WM \_ XBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="08375-104">WM\_XBUTTONDOWN message</span></span>

<span data-ttu-id="08375-105">Postado quando o usuário pressiona o primeiro ou o segundo botão X enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="08375-105">Posted when the user presses the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="08375-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="08375-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="08375-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="08375-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="08375-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="08375-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDOWN                  0x020B
```



## <a name="parameters"></a><span data-ttu-id="08375-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08375-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08375-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08375-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08375-111">A palavra de ordem inferior indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="08375-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="08375-112">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="08375-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="08375-113">Valor</span><span class="sxs-lookup"><span data-stu-id="08375-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="08375-114">Significado</span><span class="sxs-lookup"><span data-stu-id="08375-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="08375-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="08375-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="08375-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="08375-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="08375-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="08375-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="08375-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="08375-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="08375-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="08375-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="08375-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="08375-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="08375-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="08375-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="08375-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="08375-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="08375-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="08375-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="08375-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="08375-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="08375-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="08375-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="08375-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="08375-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="08375-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="08375-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="08375-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="08375-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="08375-129">A palavra de ordem superior indica em qual botão foi clicado.</span><span class="sxs-lookup"><span data-stu-id="08375-129">The high-order word indicates which button was clicked.</span></span> <span data-ttu-id="08375-130">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="08375-130">It can be one of the following values.</span></span>



| <span data-ttu-id="08375-131">Valor</span><span class="sxs-lookup"><span data-stu-id="08375-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="08375-132">Significado</span><span class="sxs-lookup"><span data-stu-id="08375-132">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="08375-133"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="08375-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="08375-134">O primeiro botão X foi clicado.</span><span class="sxs-lookup"><span data-stu-id="08375-134">The first X button was clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="08375-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="08375-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="08375-136">O segundo botão X foi clicado.</span><span class="sxs-lookup"><span data-stu-id="08375-136">The second X button was clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="08375-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08375-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08375-138">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="08375-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="08375-139">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="08375-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="08375-140">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="08375-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="08375-141">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="08375-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08375-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08375-142">Return value</span></span>

<span data-ttu-id="08375-143">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="08375-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="08375-144">Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="08375-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="08375-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="08375-145">Remarks</span></span>

<span data-ttu-id="08375-146">Use o código a seguir para obter as informações no parâmetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="08375-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam);
```



<span data-ttu-id="08375-147">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="08375-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="08375-148">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="08375-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="08375-149">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="08375-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="08375-150">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="08375-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08375-151">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="08375-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="08375-152">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="08375-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="08375-153">Ao contrário das mensagens do [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), do [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)e do [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md) , um aplicativo deve retornar **true** dessa mensagem se a processar.</span><span class="sxs-lookup"><span data-stu-id="08375-153">Unlike the [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_MBUTTONDOWN**](wm-mbuttondown.md), and [**WM\_RBUTTONDOWN**](wm-rbuttondown.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="08375-154">Isso permite que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.</span><span class="sxs-lookup"><span data-stu-id="08375-154">Doing so allows software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="08375-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08375-155">Requirements</span></span>



| <span data-ttu-id="08375-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="08375-156">Requirement</span></span> | <span data-ttu-id="08375-157">Valor</span><span class="sxs-lookup"><span data-stu-id="08375-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08375-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08375-158">Minimum supported client</span></span><br/> | <span data-ttu-id="08375-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08375-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="08375-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08375-160">Minimum supported server</span></span><br/> | <span data-ttu-id="08375-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08375-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="08375-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="08375-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="08375-163"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08375-163"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08375-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="08375-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="08375-165">**Referência**</span><span class="sxs-lookup"><span data-stu-id="08375-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08375-166">**OBTER \_ \_ wParam KeyState**</span><span class="sxs-lookup"><span data-stu-id="08375-166">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="08375-167">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="08375-167">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="08375-168">**OBTER \_ \_ wParam XBUTTON**</span><span class="sxs-lookup"><span data-stu-id="08375-168">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="08375-169">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="08375-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="08375-170">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="08375-170">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="08375-171">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="08375-171">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="08375-172">**XBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="08375-172">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="08375-173">**XBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="08375-173">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="08375-174">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="08375-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08375-175">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="08375-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="08375-176">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="08375-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="08375-177">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="08375-177">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="08375-178">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08375-178">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

