---
title: WM_POINTERDOWN mensagem
description: Postado quando um ponteiro faz contato sobre a área do cliente de uma janela.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9f94bf4474e208d0b1d29df7a5e2939d7826ca77
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689199"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="168b0-104">WM_POINTERDOWN mensagem</span><span class="sxs-lookup"><span data-stu-id="168b0-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="168b0-105">Postado quando um ponteiro faz contato sobre a área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="168b0-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="168b0-106">Essa mensagem de entrada tem como destino a janela sobre a qual o ponteiro faz contato e o ponteiro é implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que elebre o contato.</span><span class="sxs-lookup"><span data-stu-id="168b0-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="168b0-107">Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="168b0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="168b0-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="168b0-108">\[!Important\]</span></span>  
> <span data-ttu-id="168b0-109">Os aplicativos da área de trabalho devem estar cientes de DPI.</span><span class="sxs-lookup"><span data-stu-id="168b0-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="168b0-110">Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="168b0-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="168b0-111">A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar).</span><span class="sxs-lookup"><span data-stu-id="168b0-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="168b0-112">Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="168b0-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="168b0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="168b0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="168b0-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="168b0-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="168b0-115">Contém informações sobre o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="168b0-115">Contains information about the pointer.</span></span> <span data-ttu-id="168b0-116">Use as macros a seguir para recuperar informações do parâmetro wParam.</span><span class="sxs-lookup"><span data-stu-id="168b0-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="168b0-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): o identificador de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="168b0-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="168b0-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem representa a primeira entrada gerada por um novo ponteiro.</span><span class="sxs-lookup"><span data-stu-id="168b0-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="168b0-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem foi gerada por um ponteiro durante seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="168b0-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="168b0-120">Esse sinalizador não está definido em mensagens que indicam que o ponteiro tem intervalo de detecção à esquerda</span><span class="sxs-lookup"><span data-stu-id="168b0-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="168b0-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se essa mensagem foi gerada por um ponteiro que está em contato com a superfície da janela.</span><span class="sxs-lookup"><span data-stu-id="168b0-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="168b0-122">Esse sinalizador não é definido em mensagens que indicam um ponteiro de foco.</span><span class="sxs-lookup"><span data-stu-id="168b0-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="168b0-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que esse ponteiro foi designado como primário.</span><span class="sxs-lookup"><span data-stu-id="168b0-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="168b0-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação primária.</span><span class="sxs-lookup"><span data-stu-id="168b0-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="168b0-125">Isso é análogo a um botão esquerdo do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="168b0-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="168b0-126">Um ponteiro de toque terá esse conjunto quando estiver em contato com a superfície do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="168b0-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="168b0-127">Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície do digitalizador sem botões pressionados.</span><span class="sxs-lookup"><span data-stu-id="168b0-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="168b0-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ação secundária.</span><span class="sxs-lookup"><span data-stu-id="168b0-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="168b0-129">Isso é análogo a um botão direito do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="168b0-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="168b0-130">Um ponteiro de caneta terá esse conjunto quando estiver em contato com a superfície do digitalizador com o botão de caneta pressionado.</span><span class="sxs-lookup"><span data-stu-id="168b0-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="168b0-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se há uma ou mais ações terciárias com base no tipo de ponteiro; os aplicativos que desejam responder a ações terciárias devem recuperar informações específicas para o tipo de ponteiro para determinar quais botões terciários são pressionados.</span><span class="sxs-lookup"><span data-stu-id="168b0-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="168b0-132">Por exemplo, um aplicativo pode determinar os estados de botões de uma caneta chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam os estados do botão.</span><span class="sxs-lookup"><span data-stu-id="168b0-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="168b0-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um sinalizador que indica se o ponteiro especificado fez a quarta ação.</span><span class="sxs-lookup"><span data-stu-id="168b0-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="168b0-134">Os aplicativos que desejam responder à quarta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o primeiro botão estendido do mouse (XButton1) é pressionado.</span><span class="sxs-lookup"><span data-stu-id="168b0-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="168b0-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): um [**sinalizador**](pointer-flags-contants.md) que indica se o ponteiro especificado fez a quinta ação.</span><span class="sxs-lookup"><span data-stu-id="168b0-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="168b0-136">Os aplicativos que desejam responder à quinta ação devem recuperar informações específicas para o tipo de ponteiro para determinar se o segundo botão de mouse estendido (XButton2) está pressionado.</span><span class="sxs-lookup"><span data-stu-id="168b0-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="168b0-137">Consulte [**Sinalizadores de ponteiro**](pointer-flags-contants.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="168b0-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="168b0-138">Um ponteiro de foco não tem nenhum dos sinalizadores de botão definidos.</span><span class="sxs-lookup"><span data-stu-id="168b0-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="168b0-139">Isso é análogo a uma movimentação do mouse sem botões do mouse para baixo.</span><span class="sxs-lookup"><span data-stu-id="168b0-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="168b0-140">Um aplicativo pode determinar os estados de botões de uma caneta de foco, por exemplo, chamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) e examinando os sinalizadores que especificam os estados do botão.</span><span class="sxs-lookup"><span data-stu-id="168b0-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="168b0-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="168b0-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="168b0-142">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="168b0-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="168b0-143">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="168b0-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="168b0-144">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="168b0-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="168b0-145">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="168b0-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="168b0-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada x (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="168b0-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="168b0-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="168b0-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="168b0-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="168b0-148">Return value</span></span>

<span data-ttu-id="168b0-149">Se um aplicativo processa essa mensagem, ele deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="168b0-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="168b0-150">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="168b0-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="168b0-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="168b0-151">Remarks</span></span>

> <span data-ttu-id="168b0-152">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="168b0-152">\[!Important\]</span></span>  
> <span data-ttu-id="168b0-153">Quando uma janela perde a captura de um ponteiro e recebe a [**notificação WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) ela normalmente não receberá nenhuma notificação adicional.</span><span class="sxs-lookup"><span data-stu-id="168b0-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="168b0-154">Por esse motivo, é importante que você não faça suposições com base em notificações WM_POINTERDOWN  / [**WM_POINTERUP WM_POINTERUP**](wm-pointerup.md) [](wm-pointerenter.md) / [**WM_POINTERENTER WM_POINTERLEAVE**](wm-pointerleave.md) emparelhadas.</span><span class="sxs-lookup"><span data-stu-id="168b0-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="168b0-155">Cada ponteiro tem um identificador de ponteiro exclusivo durante seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="168b0-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="168b0-156">O tempo de vida de um ponteiro começa quando ele é detectado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="168b0-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="168b0-157">Uma [**WM_POINTERENTER**](wm-pointerenter.md) será gerada se um ponteiro de foco for detectado.</span><span class="sxs-lookup"><span data-stu-id="168b0-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="168b0-158">Uma **WM_POINTERDOWN** mensagem de WM_POINTERENTER seguida por **uma** mensagem de WM_POINTERENTER será gerada se um ponteiro sem foco for detectado.</span><span class="sxs-lookup"><span data-stu-id="168b0-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="168b0-159">Durante seu tempo de vida, um ponteiro pode gerar uma série [**de WM_POINTERUPDATE**](wm-pointerupdate.md) mensagens enquanto ele está passe o mouse ou em contato.</span><span class="sxs-lookup"><span data-stu-id="168b0-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="168b0-160">O tempo de vida de um ponteiro termina quando ele não é mais detectado.</span><span class="sxs-lookup"><span data-stu-id="168b0-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="168b0-161">Isso gera uma mensagem [**WM_POINTERLEAVE**](wm-pointerleave.md) dados.</span><span class="sxs-lookup"><span data-stu-id="168b0-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="168b0-162">Quando um ponteiro é anulado, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) é definido.</span><span class="sxs-lookup"><span data-stu-id="168b0-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="168b0-163">Uma [**WM_POINTERLEAVE**](wm-pointerleave.md) mensagem também pode ser gerada quando um ponteiro não capturado se move para fora dos limites de uma janela.</span><span class="sxs-lookup"><span data-stu-id="168b0-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="168b0-164">Para obter a posição horizontal e vertical de um ponteiro, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="168b0-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="168b0-165">Para converter o parâmetro lParam em uma [**estrutura POINTS,**](/previous-versions//dd162808(v=vs.85)) use a macro [**MAKEPOINTS.**](/windows/win32/api/wingdi/nf-wingdi-makepoints)</span><span class="sxs-lookup"><span data-stu-id="168b0-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="168b0-166">Para recuperar mais informações associadas à mensagem, use a [**função GetPointerInfo.**](/previous-versions/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="168b0-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="168b0-167">Para determinar os estados de chave do modificador de teclado associados a essa mensagem, use a [**função GetKeyState.**](/windows/win32/api/winuser/nf-winuser-getkeystate)</span><span class="sxs-lookup"><span data-stu-id="168b0-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="168b0-168">Por exemplo, para detectar que a tecla ALT foi pressionada, verifique se GetKeyState(VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="168b0-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="168b0-169">Observe que, se o aplicativo não processar essa mensagem, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens WM_GESTURE se [**a**](../wintouch/wm-gesture.md) sequência de entrada desse e, possivelmente, outros ponteiros for reconhecida como um gesto.</span><span class="sxs-lookup"><span data-stu-id="168b0-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="168b0-170">Se um gesto não for reconhecido, **DefWindowProc** poderá gerar entrada do mouse.</span><span class="sxs-lookup"><span data-stu-id="168b0-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="168b0-171">Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o restante para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.</span><span class="sxs-lookup"><span data-stu-id="168b0-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="168b0-172">Quando uma janela perde a captura de um ponteiro e recebe a [**WM_POINTERCAPTURECHANGED,**](wm-pointercapturechanged.md) ela normalmente não receberá nenhuma notificação adicional.</span><span class="sxs-lookup"><span data-stu-id="168b0-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="168b0-173">Portanto, é importante que uma janela não faça suposições de seu status de ponteiro, independentemente de receber notificações DOWN/UP ou ENTER/LEAVE emparelhadas de maneira par.</span><span class="sxs-lookup"><span data-stu-id="168b0-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="168b0-174">Exemplos</span><span class="sxs-lookup"><span data-stu-id="168b0-174">Examples</span></span>

<span data-ttu-id="168b0-175">O exemplo de código [**a**](/previous-versions/windows/desktop/api)seguir mostra como usar IS_POINTER_FIRSTBUTTON_WPARAM , [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)para recuperar as informações relevantes associadas **à WM_POINTERDOWN** mensagem.</span><span class="sxs-lookup"><span data-stu-id="168b0-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



<span data-ttu-id="168b0-176">O exemplo de código a seguir mostra como usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar a ID do ponteiro da **WM_POINTERDOWN** mensagem.</span><span class="sxs-lookup"><span data-stu-id="168b0-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


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



<span data-ttu-id="168b0-177">O exemplo de código a seguir mostra como lidar com diferentes tipos de ponteiro, como toque, caneta ou dispositivos de apontamento padrão.</span><span class="sxs-lookup"><span data-stu-id="168b0-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

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



## <a name="requirements"></a><span data-ttu-id="168b0-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="168b0-178">Requirements</span></span>



| <span data-ttu-id="168b0-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="168b0-179">Requirement</span></span> | <span data-ttu-id="168b0-180">Valor</span><span class="sxs-lookup"><span data-stu-id="168b0-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="168b0-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="168b0-181">Minimum supported client</span></span><br/> | <span data-ttu-id="168b0-182">\[Windows 8 somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="168b0-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="168b0-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="168b0-183">Minimum supported server</span></span><br/> | <span data-ttu-id="168b0-184">\[Windows Server 2012 somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="168b0-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="168b0-185">parâmetro</span><span class="sxs-lookup"><span data-stu-id="168b0-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="168b0-186"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="168b0-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="168b0-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="168b0-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168b0-188">Mensagens</span><span class="sxs-lookup"><span data-stu-id="168b0-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="168b0-189">**Referência**</span><span class="sxs-lookup"><span data-stu-id="168b0-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="168b0-190">**Sinalizadores de ponteiro**</span><span class="sxs-lookup"><span data-stu-id="168b0-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="168b0-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="168b0-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="168b0-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
