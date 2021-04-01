---
title: WM_NCPOINTERUP mensagem
description: Postado quando um ponteiro que fez contato na área de não cliente de uma janela quebra o contato.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensagens de entrada e notificações de WM_NCPOINTERUP mensagem
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644918"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="aa01b-104">WM_NCPOINTERUP mensagem</span><span class="sxs-lookup"><span data-stu-id="aa01b-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="aa01b-105">Postado quando um ponteiro que fez contato na área de não cliente de uma janela quebra o contato.</span><span class="sxs-lookup"><span data-stu-id="aa01b-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="aa01b-106">A mensagem é direcionada para a janela sobre a qual o ponteiro faz contato e o ponteiro é, nesse ponto, implicitamente capturado para a janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato, incluindo a notificação de **WM_NCPOINTERUP** .</span><span class="sxs-lookup"><span data-stu-id="aa01b-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="aa01b-107">Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada.</span><span class="sxs-lookup"><span data-stu-id="aa01b-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="aa01b-108">Em vez disso, um [**WM_POINTERUP**](wm-pointerup.md) é Postado na janela que capturou esse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="aa01b-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="aa01b-109">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="aa01b-109">\[!Important\]</span></span>  
> <span data-ttu-id="aa01b-110">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="aa01b-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="aa01b-111">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="aa01b-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="aa01b-112">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="aa01b-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="aa01b-113">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aa01b-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="aa01b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa01b-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa01b-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa01b-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa01b-116">Contém o identificador de ponteiro e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="aa01b-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="aa01b-117">Use as macros a seguir para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="aa01b-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="aa01b-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa01b-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="aa01b-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de sucesso retornado pelo processamento da mensagem de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="aa01b-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="aa01b-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa01b-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa01b-121">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="aa01b-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="aa01b-122">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="aa01b-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="aa01b-123">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="aa01b-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="aa01b-124">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="aa01b-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="aa01b-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="aa01b-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="aa01b-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="aa01b-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa01b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa01b-127">Return value</span></span>

<span data-ttu-id="aa01b-128">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="aa01b-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="aa01b-129">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="aa01b-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa01b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa01b-130">Remarks</span></span>

<span data-ttu-id="aa01b-131">Se o aplicativo não processar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá executar uma ou mais ações do sistema, dependendo do resultado do teste de clique incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa01b-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="aa01b-132">Normalmente, os aplicativos não precisam lidar com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa01b-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa01b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa01b-133">Requirements</span></span>



| <span data-ttu-id="aa01b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa01b-134">Requirement</span></span> | <span data-ttu-id="aa01b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="aa01b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa01b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa01b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="aa01b-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="aa01b-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="aa01b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa01b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="aa01b-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="aa01b-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa01b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa01b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa01b-141"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa01b-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa01b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa01b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa01b-143">Mensagens</span><span class="sxs-lookup"><span data-stu-id="aa01b-143">Messages</span></span>](messages.md)
</dt> </dl>

 

