---
title: Mensagem de WM_MOUSEHWHEEL (WinUser. h)
description: Enviado para a janela ativa quando a roda de rolagem horizontal do mouse é inclinada ou girada.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEHWHEEL
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781637"
---
# <a name="wm_mousehwheel-message"></a><span data-ttu-id="29156-104">Mensagem do WM \_ MOUSEHWHEEL</span><span class="sxs-lookup"><span data-stu-id="29156-104">WM\_MOUSEHWHEEL message</span></span>

<span data-ttu-id="29156-105">Enviado para a janela ativa quando a roda de rolagem horizontal do mouse é inclinada ou girada.</span><span class="sxs-lookup"><span data-stu-id="29156-105">Sent to the active window when the mouse's horizontal scroll wheel is tilted or rotated.</span></span> <span data-ttu-id="29156-106">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga a mensagem para o pai da janela.</span><span class="sxs-lookup"><span data-stu-id="29156-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="29156-107">Não deve haver nenhum encaminhamento interno da mensagem, pois **DefWindowProc** propaga a cadeia pai até encontrar uma janela que a processa.</span><span class="sxs-lookup"><span data-stu-id="29156-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="29156-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="29156-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a><span data-ttu-id="29156-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29156-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29156-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29156-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29156-111">A palavra de ordem superior indica a distância em que a roda é girada, expressa em múltiplos ou fatores do **Wheel \_ Delta**, que é definido como 120.</span><span class="sxs-lookup"><span data-stu-id="29156-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or factors of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="29156-112">Um valor positivo indica que a roda foi girada para a direita; um valor negativo indica que a roda foi girada para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="29156-112">A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left.</span></span>

<span data-ttu-id="29156-113">A palavra de ordem inferior indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="29156-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="29156-114">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="29156-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="29156-115">Valor</span><span class="sxs-lookup"><span data-stu-id="29156-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="29156-116">Significado</span><span class="sxs-lookup"><span data-stu-id="29156-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="29156-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="29156-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="29156-118">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="29156-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="29156-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="29156-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="29156-120">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="29156-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="29156-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="29156-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="29156-122">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="29156-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="29156-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="29156-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="29156-124">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="29156-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="29156-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="29156-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="29156-126">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="29156-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="29156-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="29156-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="29156-128">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="29156-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="29156-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="29156-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="29156-130">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="29156-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="29156-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29156-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29156-132">A palavra de ordem inferior Especifica a coordenada x do ponteiro, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="29156-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="29156-133">A palavra de ordem superior especifica a coordenada y do ponteiro, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="29156-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29156-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29156-134">Return value</span></span>

<span data-ttu-id="29156-135">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="29156-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="29156-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="29156-136">Remarks</span></span>

<span data-ttu-id="29156-137">Use o código a seguir para obter as informações no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="29156-137">Use the following code to obtain the information in the *wParam* parameter.</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="29156-138">Use o código a seguir para obter a posição horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="29156-138">Use the following code to obtain the horizontal and vertical position.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="29156-139">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="29156-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="29156-140">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="29156-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="29156-141">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="29156-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29156-142">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="29156-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="29156-143">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="29156-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="29156-144">A rotação da roda é um múltiplo do **Wheel \_ Delta**, que é definido como 120.</span><span class="sxs-lookup"><span data-stu-id="29156-144">The wheel rotation is a multiple of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="29156-145">Esse é o limite para a ação a ser tomada e uma ação desse tipo (por exemplo, rolagem de um incremento) deve ocorrer para cada Delta.</span><span class="sxs-lookup"><span data-stu-id="29156-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="29156-146">O Delta foi definido como 120 para permitir que a Microsoft ou outros fornecedores criem rodas de resolução mais refinada (por exemplo, uma roda com rotação livre sem entalhes) para enviar mais mensagens por rotação, mas com um valor menor em cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="29156-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (for example, a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="29156-147">Para usar esse recurso, você pode adicionar os valores Delta de entrada até que o **Wheel \_ Delta** seja atingido (para que uma rotação Delta obtenha a mesma resposta) ou role as linhas parciais em resposta a mensagens mais frequentes.</span><span class="sxs-lookup"><span data-stu-id="29156-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to more frequent messages.</span></span> <span data-ttu-id="29156-148">Você também pode escolher a granularidade da rolagem e acumular deltas até que ele seja atingido.</span><span class="sxs-lookup"><span data-stu-id="29156-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="29156-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29156-149">Requirements</span></span>



| <span data-ttu-id="29156-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="29156-150">Requirement</span></span> | <span data-ttu-id="29156-151">Valor</span><span class="sxs-lookup"><span data-stu-id="29156-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29156-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29156-152">Minimum supported client</span></span><br/> | <span data-ttu-id="29156-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29156-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="29156-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29156-154">Minimum supported server</span></span><br/> | <span data-ttu-id="29156-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29156-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="29156-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29156-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="29156-157"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29156-157"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29156-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="29156-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="29156-159">**Referência**</span><span class="sxs-lookup"><span data-stu-id="29156-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29156-160">**OBTER \_ \_ wParam KeyState**</span><span class="sxs-lookup"><span data-stu-id="29156-160">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="29156-161">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="29156-161">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="29156-162">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="29156-162">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="29156-163">**OBTER \_ \_ wParam Delta do volante \_**</span><span class="sxs-lookup"><span data-stu-id="29156-163">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="29156-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29156-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="29156-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29156-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="29156-166">**evento do mouse \_**</span><span class="sxs-lookup"><span data-stu-id="29156-166">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="29156-167">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="29156-167">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29156-168">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="29156-168">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="29156-169">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="29156-169">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="29156-170">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="29156-170">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="29156-171">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="29156-171">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="29156-172">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29156-172">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="29156-173">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="29156-173">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

