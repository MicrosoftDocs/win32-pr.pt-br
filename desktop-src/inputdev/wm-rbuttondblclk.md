---
title: Mensagem de WM_RBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes com o botão direito do mouse enquanto o cursor está na área do cliente de uma janela.
ms.assetid: 2db9a947-f052-4738-9fae-6ecaba3de9b9
keywords:
- Entrada de mouse e teclado de mensagem WM_RBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_RBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acde97e19b02ad08b3833f1c1c4eb3e0dd4b147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085419"
---
# <a name="wm_rbuttondblclk-message"></a><span data-ttu-id="18733-104">Mensagem do WM \_ RBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="18733-104">WM\_RBUTTONDBLCLK message</span></span>

<span data-ttu-id="18733-105">Postado quando o usuário clica duas vezes com o botão direito do mouse enquanto o cursor está na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="18733-105">Posted when the user double-clicks the right mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="18733-106">Se o mouse não for capturado, a mensagem será postada na janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="18733-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="18733-107">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="18733-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="18733-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="18733-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RBUTTONDBLCLK                0x0206
```



## <a name="parameters"></a><span data-ttu-id="18733-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18733-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18733-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18733-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18733-111">Indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="18733-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="18733-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="18733-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="18733-113">Valor</span><span class="sxs-lookup"><span data-stu-id="18733-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="18733-114">Significado</span><span class="sxs-lookup"><span data-stu-id="18733-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="18733-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="18733-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="18733-116">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="18733-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="18733-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="18733-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="18733-118">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="18733-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="18733-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="18733-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="18733-120">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="18733-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="18733-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="18733-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="18733-122">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="18733-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="18733-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="18733-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="18733-124">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="18733-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="18733-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="18733-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="18733-126">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="18733-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="18733-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="18733-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="18733-128">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="18733-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="18733-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18733-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18733-130">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="18733-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="18733-131">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="18733-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="18733-132">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="18733-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="18733-133">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="18733-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18733-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18733-134">Return value</span></span>

<span data-ttu-id="18733-135">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="18733-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="18733-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="18733-136">Remarks</span></span>

<span data-ttu-id="18733-137">Somente as janelas que têm o estilo **cs \_ DBLCLKS** podem receber mensagens do **WM \_ RBUTTONDBLCLK** , que o sistema gera sempre que o usuário pressiona, libera e novamente pressiona o botão direito do mouse no limite de tempo de clique duplo do sistema.</span><span class="sxs-lookup"><span data-stu-id="18733-137">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_RBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="18733-138">Clicar duas vezes no botão direito do mouse gera quatro mensagens: [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md), [**WM \_ RBUTTONUP**](wm-rbuttonup.md), **WM \_ RBUTTONDBLCLK** e **WM \_ RBUTTONUP** novamente.</span><span class="sxs-lookup"><span data-stu-id="18733-138">Double-clicking the right mouse button actually generates four messages: [**WM\_RBUTTONDOWN**](wm-rbuttondown.md), [**WM\_RBUTTONUP**](wm-rbuttonup.md), **WM\_RBUTTONDBLCLK**, and **WM\_RBUTTONUP** again.</span></span>

<span data-ttu-id="18733-139">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="18733-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="18733-140">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="18733-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="18733-141">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="18733-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="18733-142">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="18733-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18733-143">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="18733-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="18733-144">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="18733-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18733-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18733-145">Requirements</span></span>



| <span data-ttu-id="18733-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="18733-146">Requirement</span></span> | <span data-ttu-id="18733-147">Valor</span><span class="sxs-lookup"><span data-stu-id="18733-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18733-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18733-148">Minimum supported client</span></span><br/> | <span data-ttu-id="18733-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18733-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18733-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18733-150">Minimum supported server</span></span><br/> | <span data-ttu-id="18733-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18733-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18733-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18733-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="18733-153"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18733-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18733-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="18733-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="18733-155">**Referência**</span><span class="sxs-lookup"><span data-stu-id="18733-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18733-156">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="18733-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="18733-157">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="18733-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="18733-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="18733-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="18733-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="18733-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="18733-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="18733-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="18733-161">**Setdoubleclicktime**</span><span class="sxs-lookup"><span data-stu-id="18733-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="18733-162">**RBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="18733-162">**WM\_RBUTTONDOWN**</span></span>](wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="18733-163">**RBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="18733-163">**WM\_RBUTTONUP**</span></span>](wm-rbuttonup.md)
</dt> <dt>

<span data-ttu-id="18733-164">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="18733-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18733-165">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="18733-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="18733-166">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="18733-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="18733-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="18733-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="18733-168">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18733-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

