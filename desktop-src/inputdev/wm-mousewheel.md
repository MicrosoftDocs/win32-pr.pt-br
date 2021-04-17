---
title: Mensagem de WM_MOUSEWHEEL (WinUser. h)
description: Enviado para a janela de foco quando a roda do mouse é girada.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEWHEEL
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811539"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="8324e-104">Mensagem do WM \_ MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="8324e-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="8324e-105">Enviado para a janela de foco quando a roda do mouse é girada.</span><span class="sxs-lookup"><span data-stu-id="8324e-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="8324e-106">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga a mensagem para o pai da janela.</span><span class="sxs-lookup"><span data-stu-id="8324e-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="8324e-107">Não deve haver nenhum encaminhamento interno da mensagem, pois **DefWindowProc** propaga a cadeia pai até encontrar uma janela que a processa.</span><span class="sxs-lookup"><span data-stu-id="8324e-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="8324e-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8324e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="8324e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8324e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8324e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8324e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8324e-111">A palavra de ordem superior indica a distância em que a roda é girada, expressa em múltiplos ou divisões do **Wheel \_ Delta**, que é 120.</span><span class="sxs-lookup"><span data-stu-id="8324e-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="8324e-112">Um valor positivo indica que a roda foi girada para frente, afastando-a do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário.</span><span class="sxs-lookup"><span data-stu-id="8324e-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="8324e-113">A palavra de ordem inferior indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="8324e-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="8324e-114">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8324e-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8324e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8324e-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="8324e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8324e-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="8324e-117"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="8324e-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="8324e-118">A tecla CTRL está inoperante.</span><span class="sxs-lookup"><span data-stu-id="8324e-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="8324e-119"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="8324e-120">O botão esquerdo do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="8324e-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="8324e-121"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="8324e-122">O botão do meio do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="8324e-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="8324e-123"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="8324e-124">O botão direito do mouse está inativo.</span><span class="sxs-lookup"><span data-stu-id="8324e-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="8324e-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="8324e-126">A tecla SHIFT está inoperante.</span><span class="sxs-lookup"><span data-stu-id="8324e-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="8324e-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="8324e-128">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="8324e-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="8324e-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="8324e-130">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="8324e-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="8324e-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8324e-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8324e-132">A palavra de ordem inferior Especifica a coordenada x do ponteiro, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="8324e-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="8324e-133">A palavra de ordem superior especifica a coordenada y do ponteiro, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="8324e-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8324e-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8324e-134">Return value</span></span>

<span data-ttu-id="8324e-135">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="8324e-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8324e-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="8324e-136">Remarks</span></span>

<span data-ttu-id="8324e-137">Use o código a seguir para obter as informações no parâmetro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="8324e-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="8324e-138">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="8324e-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="8324e-139">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="8324e-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="8324e-140">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8324e-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="8324e-141">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="8324e-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8324e-142">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="8324e-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="8324e-143">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="8324e-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="8324e-144">A rotação da roda será um múltiplo do **Wheel \_ Delta**, que é definido em 120.</span><span class="sxs-lookup"><span data-stu-id="8324e-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="8324e-145">Esse é o limite para a ação a ser tomada e uma ação desse tipo (por exemplo, rolagem de um incremento) deve ocorrer para cada Delta.</span><span class="sxs-lookup"><span data-stu-id="8324e-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="8324e-146">O Delta foi definido como 120 para permitir que a Microsoft ou outros fornecedores criem rodas de resolução mais fina (uma roda de rotação livre sem entalhes) para enviar mais mensagens por rotação, mas com um valor menor em cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8324e-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="8324e-147">Para usar esse recurso, você pode adicionar os valores Delta de entrada até que o **Wheel \_ Delta** seja atingido (para que uma rotação Delta obtenha a mesma resposta) ou role as linhas parciais em resposta às mensagens mais frequentes.</span><span class="sxs-lookup"><span data-stu-id="8324e-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="8324e-148">Você também pode escolher a granularidade da rolagem e acumular deltas até que ele seja atingido.</span><span class="sxs-lookup"><span data-stu-id="8324e-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="8324e-149">Observe que não há nenhum *fwKeys* para **MSH \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="8324e-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="8324e-150">Caso contrário, os parâmetros são exatamente iguais aos do **WM \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="8324e-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="8324e-151">Cabe ao aplicativo encaminhar **MSH \_ MOUSEWHEEL** a quaisquer objetos ou controles inseridos.</span><span class="sxs-lookup"><span data-stu-id="8324e-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="8324e-152">O aplicativo é necessário para enviar a mensagem a um aplicativo OLE incorporado ativo.</span><span class="sxs-lookup"><span data-stu-id="8324e-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="8324e-153">É opcional que o aplicativo o envia para um controle habilitado para roda com foco.</span><span class="sxs-lookup"><span data-stu-id="8324e-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="8324e-154">Se o aplicativo enviar a mensagem a um controle, ele poderá verificar o valor de retorno para ver se a mensagem foi processada.</span><span class="sxs-lookup"><span data-stu-id="8324e-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="8324e-155">Os controles são necessários para retornar um valor **true** se eles processarem a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8324e-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8324e-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8324e-156">Requirements</span></span>



| <span data-ttu-id="8324e-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8324e-157">Requirement</span></span> | <span data-ttu-id="8324e-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8324e-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8324e-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8324e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8324e-160">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8324e-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8324e-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8324e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8324e-162">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8324e-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8324e-163">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8324e-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8324e-164"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8324e-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8324e-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="8324e-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="8324e-166">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8324e-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8324e-167">**OBTER \_ \_ wParam KeyState**</span><span class="sxs-lookup"><span data-stu-id="8324e-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="8324e-168">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="8324e-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="8324e-169">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="8324e-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="8324e-170">**OBTER \_ \_ wParam Delta do volante \_**</span><span class="sxs-lookup"><span data-stu-id="8324e-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="8324e-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8324e-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8324e-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8324e-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8324e-173">**evento do mouse \_**</span><span class="sxs-lookup"><span data-stu-id="8324e-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="8324e-174">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8324e-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8324e-175">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="8324e-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="8324e-176">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8324e-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8324e-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="8324e-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="8324e-178">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="8324e-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="8324e-179">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8324e-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8324e-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="8324e-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

