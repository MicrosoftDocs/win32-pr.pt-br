---
title: Mensagem de WM_MOUSEMOVE (WinUser. h)
description: Postado em uma janela quando o cursor se move. Se o mouse não for capturado, a mensagem será postada na janela que contém o cursor. Caso contrário, a mensagem será postada na janela que capturou o mouse.
ms.assetid: 9b99387e-e176-4b20-a05a-bc75928a1367
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEMOVE
topic_type:
- apiref
api_name:
- WM_MOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61ffd10edbd58d11c5667fbda9dc0408ea1d72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499317"
---
# <a name="wm_mousemove-message"></a><span data-ttu-id="53606-106">\_Mensagem MOUSEMOVE do WM</span><span class="sxs-lookup"><span data-stu-id="53606-106">WM\_MOUSEMOVE message</span></span>

<span data-ttu-id="53606-107">Postado em uma janela quando o cursor se move.</span><span class="sxs-lookup"><span data-stu-id="53606-107">Posted to a window when the cursor moves.</span></span> <span data-ttu-id="53606-108">Se o mouse não for capturado, a mensagem será postada na janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="53606-108">If the mouse is not captured, the message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="53606-109">Caso contrário, a mensagem será postada na janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="53606-109">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="53606-110">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="53606-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEMOVE                    0x0200
```



## <a name="parameters"></a><span data-ttu-id="53606-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53606-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53606-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53606-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53606-113">Indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="53606-113">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="53606-114">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="53606-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="53606-115">Valor</span><span class="sxs-lookup"><span data-stu-id="53606-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="53606-116">Significado</span><span class="sxs-lookup"><span data-stu-id="53606-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="53606-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="53606-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="53606-118">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="53606-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="53606-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="53606-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="53606-120">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="53606-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="53606-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="53606-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="53606-122">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="53606-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="53606-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="53606-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="53606-124">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="53606-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="53606-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="53606-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="53606-126">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="53606-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="53606-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="53606-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="53606-128">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="53606-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="53606-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="53606-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="53606-130">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="53606-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="53606-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53606-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53606-132">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="53606-132">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="53606-133">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="53606-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="53606-134">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="53606-134">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="53606-135">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="53606-135">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53606-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53606-136">Return value</span></span>

<span data-ttu-id="53606-137">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="53606-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="53606-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="53606-138">Remarks</span></span>

<span data-ttu-id="53606-139">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="53606-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="53606-140">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="53606-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="53606-141">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="53606-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="53606-142">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="53606-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53606-143">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="53606-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="53606-144">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="53606-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53606-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53606-145">Requirements</span></span>



| <span data-ttu-id="53606-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="53606-146">Requirement</span></span> | <span data-ttu-id="53606-147">Valor</span><span class="sxs-lookup"><span data-stu-id="53606-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53606-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53606-148">Minimum supported client</span></span><br/> | <span data-ttu-id="53606-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53606-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53606-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53606-150">Minimum supported server</span></span><br/> | <span data-ttu-id="53606-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53606-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53606-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53606-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="53606-153"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53606-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53606-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="53606-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="53606-155">**Referência**</span><span class="sxs-lookup"><span data-stu-id="53606-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53606-156">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="53606-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="53606-157">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="53606-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="53606-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="53606-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="53606-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="53606-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="53606-160">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="53606-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53606-161">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="53606-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="53606-162">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="53606-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="53606-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="53606-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="53606-164">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="53606-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

