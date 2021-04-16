---
title: Mensagem de WM_LBUTTONDOWN (WinUser. h)
description: Postado quando o usuário pressiona o botão esquerdo do mouse enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- Entrada de mouse e teclado de mensagem WM_LBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772929"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="5d823-104">Mensagem do WM \_ LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="5d823-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="5d823-105">Postado quando o usuário pressiona o botão esquerdo do mouse enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="5d823-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="5d823-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="5d823-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="5d823-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="5d823-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="5d823-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5d823-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="5d823-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d823-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d823-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d823-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d823-111">Indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="5d823-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="5d823-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d823-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="5d823-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5d823-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="5d823-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5d823-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="5d823-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="5d823-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="5d823-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="5d823-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="5d823-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="5d823-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="5d823-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="5d823-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="5d823-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="5d823-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="5d823-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="5d823-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="5d823-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="5d823-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="5d823-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="5d823-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="5d823-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="5d823-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="5d823-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="5d823-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="5d823-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="5d823-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="5d823-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d823-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d823-130">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="5d823-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="5d823-131">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="5d823-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="5d823-132">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="5d823-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="5d823-133">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="5d823-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d823-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d823-134">Return value</span></span>

<span data-ttu-id="5d823-135">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="5d823-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="5d823-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5d823-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="5d823-137">Para obter mais exemplos, consulte [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.</span><span class="sxs-lookup"><span data-stu-id="5d823-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d823-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d823-138">Remarks</span></span>

<span data-ttu-id="5d823-139">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="5d823-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="5d823-140">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5d823-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="5d823-141">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="5d823-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d823-142">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="5d823-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="5d823-143">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="5d823-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="5d823-144">Para detectar que a tecla ALT foi pressionada, verifique se [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) com o **\_ menu VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="5d823-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="5d823-145">Observe que isso não deve ser [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="5d823-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d823-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d823-146">Requirements</span></span>



| <span data-ttu-id="5d823-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d823-147">Requirement</span></span> | <span data-ttu-id="5d823-148">Valor</span><span class="sxs-lookup"><span data-stu-id="5d823-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d823-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d823-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5d823-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d823-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d823-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d823-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5d823-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d823-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d823-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d823-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d823-154"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d823-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d823-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d823-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d823-156">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5d823-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d823-157">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="5d823-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="5d823-158">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="5d823-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="5d823-159">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="5d823-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="5d823-160">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="5d823-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="5d823-161">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="5d823-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="5d823-162">**LBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5d823-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="5d823-163">**LBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5d823-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="5d823-164">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5d823-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d823-165">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="5d823-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="5d823-166">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="5d823-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5d823-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="5d823-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="5d823-168">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d823-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

