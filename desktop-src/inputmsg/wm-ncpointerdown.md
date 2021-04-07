---
title: WM_NCPOINTERDOWN mensagem
description: Postado quando um ponteiro faz contato na área que não é do cliente de uma janela.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- Mensagens de entrada e notificações de WM_NCPOINTERDOWN mensagem
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f4c3ef8ed75c5bd29250cd2f9ce4d666b6d961d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918818"
---
# <a name="wm_ncpointerdown-message"></a><span data-ttu-id="e20c0-104">WM_NCPOINTERDOWN mensagem</span><span class="sxs-lookup"><span data-stu-id="e20c0-104">WM_NCPOINTERDOWN message</span></span>

<span data-ttu-id="e20c0-105">Postado quando um ponteiro faz contato na área que não é do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="e20c0-105">Posted when a pointer makes contact over the non-client area of a window.</span></span> <span data-ttu-id="e20c0-106">A mensagem é direcionada para a janela sobre a qual o ponteiro faz contato.</span><span class="sxs-lookup"><span data-stu-id="e20c0-106">The message targets the window over which the pointer makes contact.</span></span> <span data-ttu-id="e20c0-107">O ponteiro é capturado implicitamente na janela para que a janela continue a receber entrada para o ponteiro até que ele interrompa o contato.</span><span class="sxs-lookup"><span data-stu-id="e20c0-107">The pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="e20c0-108">Se uma janela tiver capturado esse ponteiro, essa mensagem não será postada.</span><span class="sxs-lookup"><span data-stu-id="e20c0-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="e20c0-109">Em vez disso, um [**WM_POINTERDOWN**](wm-pointerdown.md) é Postado na janela que capturou esse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e20c0-109">Instead, a [**WM_POINTERDOWN**](wm-pointerdown.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="e20c0-110">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="e20c0-110">\[!Important\]</span></span>  
> <span data-ttu-id="e20c0-111">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e20c0-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="e20c0-112">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="e20c0-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="e20c0-113">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="e20c0-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="e20c0-114">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e20c0-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a><span data-ttu-id="e20c0-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e20c0-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20c0-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e20c0-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e20c0-117">Contém o identificador de ponteiro e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="e20c0-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="e20c0-118">Use as macros a seguir para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="e20c0-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="e20c0-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e20c0-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="e20c0-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de sucesso retornado pelo processamento da mensagem de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="e20c0-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="e20c0-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e20c0-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e20c0-122">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e20c0-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="e20c0-123">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="e20c0-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="e20c0-124">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="e20c0-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="e20c0-125">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="e20c0-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="e20c0-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="e20c0-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="e20c0-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="e20c0-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20c0-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e20c0-128">Return value</span></span>

<span data-ttu-id="e20c0-129">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="e20c0-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="e20c0-130">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e20c0-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="e20c0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e20c0-131">Remarks</span></span>

<span data-ttu-id="e20c0-132">Se o aplicativo não processar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá executar uma ou mais ações do sistema, dependendo do resultado do teste de clique incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="e20c0-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="e20c0-133">Normalmente, os aplicativos não precisam lidar com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e20c0-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20c0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e20c0-134">Requirements</span></span>



| <span data-ttu-id="e20c0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e20c0-135">Requirement</span></span> | <span data-ttu-id="e20c0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e20c0-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e20c0-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e20c0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e20c0-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e20c0-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e20c0-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e20c0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e20c0-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e20c0-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e20c0-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e20c0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20c0-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e20c0-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20c0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e20c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20c0-144">Mensagens</span><span class="sxs-lookup"><span data-stu-id="e20c0-144">Messages</span></span>](messages.md)
</dt> </dl>

 

