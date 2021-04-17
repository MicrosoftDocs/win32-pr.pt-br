---
title: WM_PARENTNOTIFY mensagem
description: Enviado a uma janela quando ocorre uma ação significativa em uma janela descendente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Mensagens de entrada e notificações de WM_PARENTNOTIFY mensagem
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499555"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="9268f-104">WM_PARENTNOTIFY mensagem</span><span class="sxs-lookup"><span data-stu-id="9268f-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="9268f-105">Enviado a uma janela quando ocorre uma ação significativa em uma janela descendente.</span><span class="sxs-lookup"><span data-stu-id="9268f-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="9268f-106">Essa mensagem agora é estendida para incluir o evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="9268f-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="9268f-107">Quando a janela filho está sendo criada, o sistema envia [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) logo antes da função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) que cria a janela retorna.</span><span class="sxs-lookup"><span data-stu-id="9268f-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="9268f-108">Quando a janela filho está sendo destruída, o sistema envia a mensagem antes que qualquer processamento para destruir a janela ocorra.</span><span class="sxs-lookup"><span data-stu-id="9268f-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="9268f-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9268f-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="9268f-110">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="9268f-110">\[!Important\]</span></span>  
> <span data-ttu-id="9268f-111">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="9268f-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="9268f-112">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="9268f-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="9268f-113">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="9268f-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="9268f-114">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9268f-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="9268f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9268f-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9268f-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9268f-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9268f-117">A palavra de ordem inferior de *wParam* especifica o evento para o qual o pai está sendo notificado.</span><span class="sxs-lookup"><span data-stu-id="9268f-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="9268f-118">O valor da palavra de ordem superior depende do valor da palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="9268f-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="9268f-119">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9268f-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9268f-120">LOWORD (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="9268f-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="9268f-121">Significado</span><span class="sxs-lookup"><span data-stu-id="9268f-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="9268f-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="9268f-123">A janela filho está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="9268f-123">The child window is being created.</span></span><br/> <span data-ttu-id="9268f-124">HIWORD (*wParam*) é o identificador da janela filho.</span><span class="sxs-lookup"><span data-stu-id="9268f-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="9268f-125">*lParam* é um identificador para a janela filho.</span><span class="sxs-lookup"><span data-stu-id="9268f-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="9268f-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="9268f-127">A janela filho está sendo destruída.</span><span class="sxs-lookup"><span data-stu-id="9268f-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="9268f-128">HIWORD (*wParam*) é o identificador da janela filho.</span><span class="sxs-lookup"><span data-stu-id="9268f-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="9268f-129">*lParam* é um identificador para a janela filho.</span><span class="sxs-lookup"><span data-stu-id="9268f-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="9268f-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="9268f-131">O usuário colocou o cursor sobre a janela filho e clicou com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="9268f-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="9268f-132">HIWORD (*wParam*) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="9268f-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9268f-133">*lParam* é a coordenada x do cursor é a palavra de ordem inferior e a coordenada y do cursor é a palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="9268f-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="9268f-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="9268f-135">O usuário colocou o cursor sobre a janela filho e clicou no botão do meio do mouse.</span><span class="sxs-lookup"><span data-stu-id="9268f-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="9268f-136">HIWORD (*wParam*) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="9268f-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9268f-137">*lParam* é a coordenada x do cursor é a palavra de ordem inferior e a coordenada y do cursor é a palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="9268f-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="9268f-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="9268f-139">O usuário colocou o cursor sobre a janela filho e clicou com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="9268f-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="9268f-140">HIWORD (*wParam*) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="9268f-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9268f-141">*lParam* é a coordenada x do cursor é a palavra de ordem inferior e a coordenada y do cursor é a palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="9268f-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="9268f-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="9268f-143">O usuário colocou o cursor sobre a janela filho e clicou no primeiro ou no segundo botão X.</span><span class="sxs-lookup"><span data-stu-id="9268f-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="9268f-144">HIWORD (*wParam*) indica qual botão foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="9268f-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="9268f-145">Esse parâmetro pode ser um dos seguintes valores: XBUTTON1 ou XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="9268f-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="9268f-146">*lParam* é a coordenada x do cursor é a palavra de ordem inferior e a coordenada y do cursor é a palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="9268f-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="9268f-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="9268f-148">Um ponteiro entrou em contato com a janela filho.</span><span class="sxs-lookup"><span data-stu-id="9268f-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="9268f-149">HIWORD (*wParam*) contém o identificador do ponteiro que gerou o evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="9268f-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="9268f-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9268f-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9268f-151">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9268f-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="9268f-152">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="9268f-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="9268f-153">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="9268f-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="9268f-154">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="9268f-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="9268f-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="9268f-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="9268f-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="9268f-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9268f-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9268f-157">Return value</span></span>

<span data-ttu-id="9268f-158">Se o aplicativo processar essa mensagem, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9268f-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="9268f-159">Se o aplicativo não processar essa mensagem, ele chamará [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="9268f-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="9268f-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="9268f-160">Remarks</span></span>

<span data-ttu-id="9268f-161">Essa mensagem também é enviada para todas as janelas ancestrais da janela filho, incluindo a janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="9268f-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="9268f-162">Todas as janelas filhas, exceto aquelas que têm o **WS_EX_NOPARENTNOTIFY** estilo de janela estendido, enviam essa mensagem para suas janelas pai.</span><span class="sxs-lookup"><span data-stu-id="9268f-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="9268f-163">Por padrão, as janelas filhas em uma caixa de diálogo têm o estilo de **WS_EX_NOPARENTNOTIFY** , a menos que a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) seja chamada para criar a janela filho sem esse estilo.</span><span class="sxs-lookup"><span data-stu-id="9268f-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="9268f-164">Essa notificação fornece ao Windows ancestral da janela filho uma oportunidade de examinar as informações do ponteiro e, se necessário, capturar o ponteiro usando as funções de captura do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9268f-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9268f-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9268f-165">Requirements</span></span>



| <span data-ttu-id="9268f-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="9268f-166">Requirement</span></span> | <span data-ttu-id="9268f-167">Valor</span><span class="sxs-lookup"><span data-stu-id="9268f-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9268f-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9268f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="9268f-169">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9268f-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9268f-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9268f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="9268f-171">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9268f-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9268f-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9268f-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="9268f-173"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9268f-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9268f-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="9268f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9268f-175">Mensagens</span><span class="sxs-lookup"><span data-stu-id="9268f-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="9268f-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="9268f-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="9268f-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="9268f-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="9268f-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9268f-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9268f-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9268f-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9268f-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="9268f-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="9268f-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="9268f-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="9268f-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9268f-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9268f-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9268f-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9268f-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9268f-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9268f-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9268f-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

