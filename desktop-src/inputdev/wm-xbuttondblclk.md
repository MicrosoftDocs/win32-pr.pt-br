---
title: Mensagem de WM_XBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes no primeiro ou no segundo botão X enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- Entrada de mouse e teclado de mensagem WM_XBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644860"
---
# <a name="wm_xbuttondblclk-message"></a><span data-ttu-id="258cb-104">Mensagem do WM \_ XBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="258cb-104">WM\_XBUTTONDBLCLK message</span></span>

<span data-ttu-id="258cb-105">Postado quando o usuário clica duas vezes no primeiro ou no segundo botão X enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="258cb-105">Posted when the user double-clicks the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="258cb-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="258cb-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="258cb-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="258cb-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="258cb-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="258cb-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a><span data-ttu-id="258cb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="258cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258cb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="258cb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="258cb-111">A palavra de ordem inferior indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="258cb-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="258cb-112">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="258cb-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="258cb-113">Valor</span><span class="sxs-lookup"><span data-stu-id="258cb-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="258cb-114">Significado</span><span class="sxs-lookup"><span data-stu-id="258cb-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="258cb-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="258cb-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="258cb-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="258cb-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="258cb-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="258cb-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="258cb-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="258cb-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="258cb-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="258cb-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="258cb-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="258cb-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="258cb-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="258cb-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="258cb-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="258cb-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="258cb-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="258cb-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="258cb-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="258cb-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="258cb-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="258cb-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="258cb-129">A palavra de ordem superior indica qual botão foi clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="258cb-129">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="258cb-130">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="258cb-130">It can be one of the following values.</span></span>



| <span data-ttu-id="258cb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="258cb-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="258cb-132">Significado</span><span class="sxs-lookup"><span data-stu-id="258cb-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="258cb-133"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="258cb-134">O primeiro botão X foi clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="258cb-134">The first X button was double-clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="258cb-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="258cb-136">O segundo botão X foi clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="258cb-136">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="258cb-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="258cb-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="258cb-138">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="258cb-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="258cb-139">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="258cb-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="258cb-140">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="258cb-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="258cb-141">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="258cb-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258cb-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="258cb-142">Return value</span></span>

<span data-ttu-id="258cb-143">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="258cb-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="258cb-144">Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="258cb-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="258cb-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="258cb-145">Remarks</span></span>

<span data-ttu-id="258cb-146">Use o código a seguir para obter as informações no parâmetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="258cb-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="258cb-147">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="258cb-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="258cb-148">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="258cb-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="258cb-149">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="258cb-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="258cb-150">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="258cb-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="258cb-151">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="258cb-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="258cb-152">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="258cb-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="258cb-153">Somente as janelas que têm o estilo **cs \_ DBLCLKS** podem receber mensagens do **WM \_ XBUTTONDBLCLK** , que o sistema gera sempre que o usuário pressiona, libera e novamente pressiona um botão X dentro do limite de tempo de clique duplo do sistema.</span><span class="sxs-lookup"><span data-stu-id="258cb-153">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_XBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="258cb-154">Clicar duas vezes em um desses botões gera quatro mensagens: [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md), [**WM \_ XBUTTONUP**](wm-xbuttonup.md), **WM \_ XBUTTONDBLCLK** e **WM \_ XBUTTONUP** novamente.</span><span class="sxs-lookup"><span data-stu-id="258cb-154">Double-clicking one of these buttons actually generates four messages: [**WM\_XBUTTONDOWN**](wm-xbuttondown.md), [**WM\_XBUTTONUP**](wm-xbuttonup.md), **WM\_XBUTTONDBLCLK**, and **WM\_XBUTTONUP** again.</span></span>

<span data-ttu-id="258cb-155">Ao contrário das mensagens do [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md), do [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)e do [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) , um aplicativo deve retornar **true** dessa mensagem se a processar.</span><span class="sxs-lookup"><span data-stu-id="258cb-155">Unlike the [**WM\_LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM\_MBUTTONDBLCLK**](wm-mbuttondblclk.md), and [**WM\_RBUTTONDBLCLK**](wm-rbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="258cb-156">Isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.</span><span class="sxs-lookup"><span data-stu-id="258cb-156">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="258cb-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="258cb-157">Requirements</span></span>



| <span data-ttu-id="258cb-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="258cb-158">Requirement</span></span> | <span data-ttu-id="258cb-159">Valor</span><span class="sxs-lookup"><span data-stu-id="258cb-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="258cb-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="258cb-160">Minimum supported client</span></span><br/> | <span data-ttu-id="258cb-161">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="258cb-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="258cb-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="258cb-162">Minimum supported server</span></span><br/> | <span data-ttu-id="258cb-163">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="258cb-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="258cb-164">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="258cb-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="258cb-165"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-165"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="258cb-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="258cb-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="258cb-167">**Referência**</span><span class="sxs-lookup"><span data-stu-id="258cb-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="258cb-168">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="258cb-168">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="258cb-169">**OBTER \_ \_ wParam KeyState**</span><span class="sxs-lookup"><span data-stu-id="258cb-169">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="258cb-170">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="258cb-170">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="258cb-171">**OBTER \_ \_ wParam XBUTTON**</span><span class="sxs-lookup"><span data-stu-id="258cb-171">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="258cb-172">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="258cb-172">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="258cb-173">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="258cb-173">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="258cb-174">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="258cb-174">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="258cb-175">**Setdoubleclicktime**</span><span class="sxs-lookup"><span data-stu-id="258cb-175">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="258cb-176">**XBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="258cb-176">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

[<span data-ttu-id="258cb-177">**XBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="258cb-177">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="258cb-178">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="258cb-178">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="258cb-179">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="258cb-179">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="258cb-180">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="258cb-180">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="258cb-181">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="258cb-181">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="258cb-182">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="258cb-182">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

