---
title: Mensagem de WM_VSCROLL (WinUser. h)
description: A mensagem do WM \_ VSCROLL é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem vertical padrão da janela.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- Controles de WM_VSCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086380"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="444a5-104">Mensagem do WM \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="444a5-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="444a5-105">A mensagem do **WM \_ VSCROLL** é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem vertical padrão da janela.</span><span class="sxs-lookup"><span data-stu-id="444a5-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="444a5-106">Essa mensagem também é enviada para o proprietário de um controle de barra de rolagem vertical quando ocorre um evento de rolagem no controle.</span><span class="sxs-lookup"><span data-stu-id="444a5-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="444a5-107">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="444a5-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="444a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="444a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="444a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="444a5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="444a5-110">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual da caixa de rolagem se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) for SB \_ THUMBPOSITION ou SB \_ THUMBTRACK; caso contrário, essa palavra não será usada.</span><span class="sxs-lookup"><span data-stu-id="444a5-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="444a5-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica um valor de barra de rolagem que indica a solicitação de rolagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="444a5-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="444a5-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="444a5-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="444a5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="444a5-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="444a5-114">Significado</span><span class="sxs-lookup"><span data-stu-id="444a5-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="444a5-115"><dt>**\_parte inferior da SB**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="444a5-116">Rola para a direita inferior.</span><span class="sxs-lookup"><span data-stu-id="444a5-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="444a5-117"><dt>**\_PERrolagem SB**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="444a5-118">Finaliza a rolagem.</span><span class="sxs-lookup"><span data-stu-id="444a5-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="444a5-119"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="444a5-120">Rola uma linha para baixo.</span><span class="sxs-lookup"><span data-stu-id="444a5-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="444a5-121"><dt>**linha de SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="444a5-122">Rola uma linha para cima.</span><span class="sxs-lookup"><span data-stu-id="444a5-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="444a5-123"><dt>**SB \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="444a5-124">Rola uma página para baixo.</span><span class="sxs-lookup"><span data-stu-id="444a5-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="444a5-125"><dt>**SB \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="444a5-126">Rola uma página para cima.</span><span class="sxs-lookup"><span data-stu-id="444a5-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="444a5-127"><dt>**SB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="444a5-128">O usuário arrastou a caixa de rolagem (Thumb) e liberou o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="444a5-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="444a5-129">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição da caixa de rolagem no final da operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="444a5-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="444a5-130"><dt>**SB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="444a5-131">O usuário está arrastando a caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="444a5-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="444a5-132">Essa mensagem é enviada repetidamente até que o usuário libere o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="444a5-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="444a5-133">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição para a qual a caixa de rolagem foi arrastada.</span><span class="sxs-lookup"><span data-stu-id="444a5-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="444a5-134"><dt>**superior da SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="444a5-135">Rola para a parte superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="444a5-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="444a5-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="444a5-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="444a5-137">Se a mensagem for enviada por um controle de barra de rolagem, esse parâmetro será o identificador para o controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="444a5-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="444a5-138">Se a mensagem for enviada por uma barra de rolagem padrão, esse parâmetro será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="444a5-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="444a5-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="444a5-139">Return value</span></span>

<span data-ttu-id="444a5-140">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="444a5-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="444a5-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="444a5-141">Remarks</span></span>

<span data-ttu-id="444a5-142">O \_ código de solicitação SB THUMBTRACK é normalmente usado por aplicativos que fornecem comentários, pois o usuário arrasta a caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="444a5-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="444a5-143">Se um aplicativo rolar o conteúdo da janela, ele também deverá redefinir a posição da caixa de rolagem usando a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="444a5-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="444a5-144">Observe que a mensagem do **WM \_ VSCROLL** transporta apenas 16 bits de dados da posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="444a5-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="444a5-145">Assim, os aplicativos que dependem exclusivamente do **WM \_ VSCROLL** (e do [**WM \_ HSCROLL**](wm-hscroll.md)) para os dados da posição de rolagem têm um valor de posição máximo prático de 65.535.</span><span class="sxs-lookup"><span data-stu-id="444a5-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="444a5-146">No entanto, como as funções [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) dão suporte a dados de posição da barra de rolagem de 32 bits, há uma maneira de burlar a barreira de 16 bits das mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do **WM \_ VSCROLL** .</span><span class="sxs-lookup"><span data-stu-id="444a5-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="444a5-147">Consulte **GetScrollInfo** para obter uma descrição da técnica.</span><span class="sxs-lookup"><span data-stu-id="444a5-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="444a5-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="444a5-148">Requirements</span></span>



| <span data-ttu-id="444a5-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="444a5-149">Requirement</span></span> | <span data-ttu-id="444a5-150">Valor</span><span class="sxs-lookup"><span data-stu-id="444a5-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="444a5-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="444a5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="444a5-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="444a5-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="444a5-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="444a5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="444a5-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="444a5-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="444a5-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="444a5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="444a5-156"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="444a5-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444a5-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="444a5-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="444a5-158">**Referência**</span><span class="sxs-lookup"><span data-stu-id="444a5-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="444a5-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="444a5-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="444a5-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="444a5-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="444a5-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="444a5-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="444a5-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="444a5-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="444a5-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="444a5-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="444a5-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="444a5-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="444a5-165">**HSCROLL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="444a5-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="444a5-166">**WM \_ VSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="444a5-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

