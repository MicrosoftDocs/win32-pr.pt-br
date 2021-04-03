---
title: Mensagem WM_POINTERUP
description: Postado quando um ponteiro que fez contato na área do cliente de uma janela quebra o contato.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- Mensagens de entrada e notificações de WM_POINTERUP mensagem
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f6c23b810b7ec5a7f60ae7e52ddbb5b535ab0503
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103930043"
---
# <a name="wm_pointerup-message"></a><span data-ttu-id="fe1db-104">Mensagem WM_POINTERUP</span><span class="sxs-lookup"><span data-stu-id="fe1db-104">WM_POINTERUP message</span></span>

<span data-ttu-id="fe1db-105">Postado quando um ponteiro que fez contato na área do cliente de uma janela quebra o contato.</span><span class="sxs-lookup"><span data-stu-id="fe1db-105">Posted when a pointer that made contact over the client area of a window breaks contact.</span></span> <span data-ttu-id="fe1db-106">Essa mensagem de entrada visa a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber mensagens de entrada, incluindo a notificação de **WM_POINTERUP** para o ponteiro até que ele interrompa o contato.</span><span class="sxs-lookup"><span data-stu-id="fe1db-106">This input message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input messages including the **WM_POINTERUP** notification for the pointer until it breaks contact.</span></span>

<span data-ttu-id="fe1db-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe1db-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="fe1db-108">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="fe1db-108">\[!Important\]</span></span>  
> <span data-ttu-id="fe1db-109">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="fe1db-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="fe1db-110">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="fe1db-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="fe1db-111">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="fe1db-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="fe1db-112">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe1db-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a><span data-ttu-id="fe1db-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe1db-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe1db-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe1db-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe1db-115">Contém informações sobre o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe1db-115">Contains information about the pointer.</span></span> <span data-ttu-id="fe1db-116">Use as macros a seguir para recuperar informações do parâmetro wParam.</span><span class="sxs-lookup"><span data-stu-id="fe1db-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="fe1db-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe1db-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="fe1db-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem representa a primeira entrada gerada por um novo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe1db-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="fe1db-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se esta mensagem foi gerada por um ponteiro durante seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="fe1db-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="fe1db-120">Esse sinalizador não é definido em mensagens que indicam que o ponteiro tem um intervalo de detecção à esquerda</span><span class="sxs-lookup"><span data-stu-id="fe1db-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="fe1db-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se esta mensagem foi gerada por um ponteiro que está em contato com a superfície da janela.</span><span class="sxs-lookup"><span data-stu-id="fe1db-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="fe1db-122">Esse sinalizador não é definido em mensagens que indicam um ponteiro de focalização.</span><span class="sxs-lookup"><span data-stu-id="fe1db-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="fe1db-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que esse ponteiro foi designado como primário.</span><span class="sxs-lookup"><span data-stu-id="fe1db-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="fe1db-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação primária.</span><span class="sxs-lookup"><span data-stu-id="fe1db-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="fe1db-125">Isso é análogo a um botão esquerdo do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="fe1db-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="fe1db-126">Um ponteiro de toque terá esse conjunto quando estiver em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="fe1db-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="fe1db-127">Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície digitalizadora sem botões pressionados.</span><span class="sxs-lookup"><span data-stu-id="fe1db-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="fe1db-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação secundária.</span><span class="sxs-lookup"><span data-stu-id="fe1db-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="fe1db-129">Isso é análogo a um botão direito do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="fe1db-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="fe1db-130">Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície digitalizadora com o botão de rosca de caneta pressionado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="fe1db-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ou mais ações de terciário com base no tipo de ponteiro; os aplicativos que desejam responder às ações de terciário devem recuperar informações específicas ao tipo de ponteiro para determinar quais botões terciários são pressionados.</span><span class="sxs-lookup"><span data-stu-id="fe1db-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="fe1db-132">Por exemplo, um aplicativo pode determinar os Estados de botões de uma caneta chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam Estados de botão.</span><span class="sxs-lookup"><span data-stu-id="fe1db-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="fe1db-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se o ponteiro especificado levou a quarta ação.</span><span class="sxs-lookup"><span data-stu-id="fe1db-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="fe1db-134">Os aplicativos que desejam responder às quartas ações devem recuperar informações específicas do tipo de ponteiro para determinar se o primeiro botão do mouse estendido (XButton1) é pressionado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="fe1db-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um [**sinalizador**](pointer-flags-contants.md) que indica se o ponteiro especificado levou a quinta ação.</span><span class="sxs-lookup"><span data-stu-id="fe1db-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="fe1db-136">Os aplicativos que desejam responder às quinta ações devem recuperar informações específicas do tipo de ponteiro para determinar se o segundo botão de mouse estendido (XButton2) é pressionado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="fe1db-137">Consulte [**sinalizadores de ponteiro**](pointer-flags-contants.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="fe1db-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="fe1db-138">Um ponteiro em foco não tem nenhum dos sinalizadores de botão definidos.</span><span class="sxs-lookup"><span data-stu-id="fe1db-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="fe1db-139">Isso é análogo a um movimento de mouse sem botões de mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="fe1db-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="fe1db-140">Um aplicativo pode determinar os Estados dos botões de uma caneta em foco, por exemplo, chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam Estados de botão.</span><span class="sxs-lookup"><span data-stu-id="fe1db-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="fe1db-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe1db-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe1db-142">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe1db-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="fe1db-143">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="fe1db-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="fe1db-144">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="fe1db-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="fe1db-145">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="fe1db-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="fe1db-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="fe1db-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="fe1db-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="fe1db-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe1db-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe1db-148">Return value</span></span>

<span data-ttu-id="fe1db-149">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="fe1db-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="fe1db-150">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="fe1db-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe1db-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe1db-151">Remarks</span></span>

> <span data-ttu-id="fe1db-152">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="fe1db-152">\[!Important\]</span></span>  
> <span data-ttu-id="fe1db-153">Quando uma janela perde a captura de um ponteiro e recebe a notificação de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , ela normalmente não receberá notificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="fe1db-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="fe1db-154">Por esse motivo, é importante que você não faça nenhuma suposição com base em WM_POINTERDOWN igualmente emparelhadas [](wm-pointerdown.md) / **WM_POINTERUP** ou [**WM_POINTERENTER**](wm-pointerenter.md) / notificações de [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="fe1db-154">For this reason, it is important that you not make any assumptions based on evenly paired [**WM_POINTERDOWN**](wm-pointerdown.md)/**WM_POINTERUP** or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="fe1db-155">Cada ponteiro tem um identificador de ponteiro exclusivo durante seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="fe1db-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="fe1db-156">O tempo de vida de um ponteiro começa quando é detectado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fe1db-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="fe1db-157">Uma mensagem de [**WM_POINTERENTER**](wm-pointerenter.md) será gerada se um ponteiro em foco for detectado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="fe1db-158">Uma mensagem de [**WM_POINTERDOWN**](wm-pointerdown.md) seguida por uma mensagem de **WM_POINTERENTER** será gerada se um ponteiro sem foco for detectado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-158">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="fe1db-159">Durante seu tempo de vida, um ponteiro pode gerar uma série de [**WM_POINTERUPDATE**](wm-pointerupdate.md) mensagens enquanto está focalizando ou em contato.</span><span class="sxs-lookup"><span data-stu-id="fe1db-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="fe1db-160">O tempo de vida de um ponteiro termina quando ele não é mais detectado.</span><span class="sxs-lookup"><span data-stu-id="fe1db-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="fe1db-161">Isso gera uma mensagem de [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="fe1db-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="fe1db-162">Quando um ponteiro é anulado, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) é definido.</span><span class="sxs-lookup"><span data-stu-id="fe1db-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="fe1db-163">Uma mensagem de [**WM_POINTERLEAVE**](wm-pointerleave.md) também pode ser gerada quando um ponteiro não capturado é movido para fora dos limites de uma janela.</span><span class="sxs-lookup"><span data-stu-id="fe1db-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="fe1db-164">Para obter a posição horizontal e vertical de um ponteiro, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fe1db-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>

<span data-ttu-id="fe1db-165">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="fe1db-165">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="fe1db-166">A macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) também pode ser usada para converter o parâmetro lParam em uma estrutura [**Points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe1db-166">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="fe1db-167">A função [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) pode ser usada para determinar os Estados de chave de modificador de teclado associados a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe1db-167">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="fe1db-168">Por exemplo, para detectar que a tecla ALT foi pressionada, verifique se **GetKeyState**(VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="fe1db-168">For example, to detect that the ALT key was pressed, check whether **GetKeyState**(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="fe1db-169">Se o aplicativo não processar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens de [**WM_GESTURE**](../wintouch/wm-gesture.md)se a sequência de entrada desse e, possivelmente, outros ponteiros for reconhecida como um gesto.</span><span class="sxs-lookup"><span data-stu-id="fe1db-169">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md)messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="fe1db-170">Se um gesto não for reconhecido, **DefWindowProc** poderá gerar a entrada do mouse.</span><span class="sxs-lookup"><span data-stu-id="fe1db-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="fe1db-171">Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o resto para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.</span><span class="sxs-lookup"><span data-stu-id="fe1db-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="fe1db-172">Use a função [**GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar informações adicionais relacionadas a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe1db-172">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

## <a name="examples"></a><span data-ttu-id="fe1db-173">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe1db-173">Examples</span></span>

<span data-ttu-id="fe1db-174">O exemplo de código a seguir mostra como recuperar a posição x e y do ponteiro associado com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe1db-174">The following code example shows how to retrieve the x and y position of the pointer associated witht this message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



<span data-ttu-id="fe1db-175">O exemplo de código a seguir mostra como obter a ID do ponteiro associada a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe1db-175">The following code example shows how to obtain the pointer id associated with this message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



<span data-ttu-id="fe1db-176">O exemplo de código a seguir mostra como tratar diferentes tipos de ponteiro associados a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe1db-176">The following code example shows how to handle different pointer types associated with this message.</span></span>


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="fe1db-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe1db-177">Requirements</span></span>



| <span data-ttu-id="fe1db-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe1db-178">Requirement</span></span> | <span data-ttu-id="fe1db-179">Valor</span><span class="sxs-lookup"><span data-stu-id="fe1db-179">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe1db-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe1db-180">Minimum supported client</span></span><br/> | <span data-ttu-id="fe1db-181">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe1db-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="fe1db-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe1db-182">Minimum supported server</span></span><br/> | <span data-ttu-id="fe1db-183">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe1db-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe1db-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe1db-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe1db-185"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe1db-185"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe1db-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe1db-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe1db-187">Mensagens</span><span class="sxs-lookup"><span data-stu-id="fe1db-187">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="fe1db-188">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fe1db-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe1db-189">**Sinalizadores de ponteiro**</span><span class="sxs-lookup"><span data-stu-id="fe1db-189">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="fe1db-190">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-190">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-191">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-191">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-192">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-192">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-193">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-193">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-194">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-194">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="fe1db-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fe1db-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
