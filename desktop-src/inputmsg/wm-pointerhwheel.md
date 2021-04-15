---
title: WM_POINTERHWHEEL mensagem
description: Postado na janela com o foco do teclado de primeiro plano quando uma roda de rolagem horizontal é girada.
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- Mensagens de entrada e notificações de WM_POINTERHWHEEL mensagem
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5817d5ed243363c82038dc3df2d8f1e337079076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369801"
---
# <a name="wm_pointerhwheel-message"></a><span data-ttu-id="fe6aa-104">WM_POINTERHWHEEL mensagem</span><span class="sxs-lookup"><span data-stu-id="fe6aa-104">WM_POINTERHWHEEL message</span></span>

<span data-ttu-id="fe6aa-105">Postado na janela com o foco do teclado de primeiro plano quando uma roda de rolagem horizontal é girada.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-105">Posted to the window with foreground keyboard focus when a horizontal scroll wheel is rotated.</span></span>

<span data-ttu-id="fe6aa-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe6aa-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="fe6aa-107">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="fe6aa-107">\[!Important\]</span></span>  
> <span data-ttu-id="fe6aa-108">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="fe6aa-109">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="fe6aa-110">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="fe6aa-111">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a><span data-ttu-id="fe6aa-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe6aa-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6aa-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe6aa-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6aa-114">Contém o identificador de ponteiro e o Delta de roda.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="fe6aa-115">Use as macros a seguir para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="fe6aa-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="fe6aa-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): o Delta de roda como um valor curto assinado.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="fe6aa-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe6aa-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6aa-119">Contém o local do ponto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="fe6aa-120">Como o ponteiro pode fazer contato com o dispositivo em uma área não trivial, esse local de ponto pode ser uma simplificação de uma área de ponteiro mais complexa.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="fe6aa-121">Sempre que possível, um aplicativo deve usar as informações completas da área do ponteiro em vez do local do ponto.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="fe6aa-122">Use as macros a seguir para recuperar as coordenadas de tela física do ponto.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="fe6aa-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): a coordenada X (ponto horizontal).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="fe6aa-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): a coordenada Y (ponto vertical).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6aa-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe6aa-125">Return value</span></span>

<span data-ttu-id="fe6aa-126">Se o aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="fe6aa-127">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6aa-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe6aa-128">Remarks</span></span>

<span data-ttu-id="fe6aa-129">Para recuperar as unidades de rolagem de roda, use o **inputData** arquivado da estrutura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) retornada chamando a função [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fe6aa-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="fe6aa-130">Este campo contém um valor assinado e é expresso em um múltiplo de **WHEEL_DELTA**.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="fe6aa-131">Um valor positivo indica uma rotação para frente e um valor negativo indica uma rotação para trás.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="fe6aa-132">Observe que as entradas da roda podem ser entregues mesmo que o cursor do mouse esteja localizado fora da janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="fe6aa-133">As mensagens de roda são entregues de maneira muito semelhante às entradas do teclado.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="fe6aa-134">A janela de foco da fila de mensagens do foregournd recebe as mensagens de roda.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6aa-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6aa-135">Requirements</span></span>



| <span data-ttu-id="fe6aa-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6aa-136">Requirement</span></span> | <span data-ttu-id="fe6aa-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fe6aa-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6aa-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe6aa-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6aa-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe6aa-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="fe6aa-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe6aa-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6aa-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe6aa-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe6aa-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe6aa-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe6aa-143"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe6aa-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6aa-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe6aa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6aa-145">Mensagens</span><span class="sxs-lookup"><span data-stu-id="fe6aa-145">Messages</span></span>](messages.md)
</dt> </dl>

 

