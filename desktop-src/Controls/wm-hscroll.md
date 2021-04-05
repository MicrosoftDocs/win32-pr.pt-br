---
title: Mensagem de WM_HSCROLL (WinUser. h)
description: A mensagem do WM \_ HSCROLL é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem horizontal padrão da janela.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Controles de WM_HSCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085803"
---
# <a name="wm_hscroll-message"></a><span data-ttu-id="3b758-104">Mensagem do WM \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="3b758-104">WM\_HSCROLL message</span></span>

<span data-ttu-id="3b758-105">A mensagem do **WM \_ HSCROLL** é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem horizontal padrão da janela.</span><span class="sxs-lookup"><span data-stu-id="3b758-105">The **WM\_HSCROLL** message is sent to a window when a scroll event occurs in the window's standard horizontal scroll bar.</span></span> <span data-ttu-id="3b758-106">Essa mensagem também é enviada para o proprietário de um controle de barra de rolagem horizontal quando ocorre um evento de rolagem no controle.</span><span class="sxs-lookup"><span data-stu-id="3b758-106">This message is also sent to the owner of a horizontal scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="3b758-107">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b758-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3b758-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b758-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b758-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b758-110">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual da caixa de rolagem se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) for SB \_ THUMBPOSITION ou SB \_ THUMBTRACK; caso contrário, essa palavra não será usada.</span><span class="sxs-lookup"><span data-stu-id="3b758-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="3b758-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica um valor de barra de rolagem que indica a solicitação de rolagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b758-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="3b758-112">Esta palavra pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b758-112">This word can be one of the following values.</span></span>



| <span data-ttu-id="3b758-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3b758-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="3b758-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3b758-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="3b758-115"><dt>**\_PERrolagem SB**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-115"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="3b758-116">Finaliza a rolagem.</span><span class="sxs-lookup"><span data-stu-id="3b758-116">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="3b758-117"><dt>**SB \_ restante**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-117"><dt>**SB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="3b758-118">Rola para a parte superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="3b758-118">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="3b758-119"><dt>**SB \_ direito**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-119"><dt>**SB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="3b758-120">Rola para a direita inferior.</span><span class="sxs-lookup"><span data-stu-id="3b758-120">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="3b758-121"><dt>**SB \_ LINELEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-121"><dt>**SB\_LINELEFT**</dt></span></span> </dl>                | <span data-ttu-id="3b758-122">Rola para a esquerda em uma unidade.</span><span class="sxs-lookup"><span data-stu-id="3b758-122">Scrolls left by one unit.</span></span><br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="3b758-123"><dt>**SB \_ LINERIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-123"><dt>**SB\_LINERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="3b758-124">Rola para a direita em uma unidade.</span><span class="sxs-lookup"><span data-stu-id="3b758-124">Scrolls right by one unit.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="3b758-125"><dt>**SB \_ PAGELEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-125"><dt>**SB\_PAGELEFT**</dt></span></span> </dl>                | <span data-ttu-id="3b758-126">Rola para a esquerda pela largura da janela.</span><span class="sxs-lookup"><span data-stu-id="3b758-126">Scrolls left by the width of the window.</span></span><br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="3b758-127"><dt>**SB \_ fixada**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-127"><dt>**SB\_PAGERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="3b758-128">Rola para a direita pela largura da janela.</span><span class="sxs-lookup"><span data-stu-id="3b758-128">Scrolls right by the width of the window.</span></span><br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="3b758-129"><dt>**SB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-129"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="3b758-130">O usuário arrastou a caixa de rolagem (Thumb) e liberou o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="3b758-130">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="3b758-131">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição da caixa de rolagem no final da operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="3b758-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="3b758-132"><dt>**SB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-132"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="3b758-133">O usuário está arrastando a caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="3b758-133">The user is dragging the scroll box.</span></span> <span data-ttu-id="3b758-134">Essa mensagem é enviada repetidamente até que o usuário libere o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="3b758-134">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="3b758-135">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica a posição para a qual a caixa de rolagem foi arrastada.</span><span class="sxs-lookup"><span data-stu-id="3b758-135">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b758-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b758-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b758-137">Se a mensagem for enviada por um controle de barra de rolagem, esse parâmetro será o identificador para o controle da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="3b758-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="3b758-138">Se a mensagem for enviada por uma barra de rolagem padrão, esse parâmetro será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b758-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b758-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b758-139">Return value</span></span>

<span data-ttu-id="3b758-140">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="3b758-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b758-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b758-141">Remarks</span></span>

<span data-ttu-id="3b758-142">O \_ código de solicitação SB THUMBTRACK é normalmente usado por aplicativos que fornecem comentários, pois o usuário arrasta a caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="3b758-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="3b758-143">Se um aplicativo rolar o conteúdo da janela, ele também deverá redefinir a posição da caixa de rolagem usando a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="3b758-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="3b758-144">Observe que a mensagem do **WM \_ HSCROLL** transporta apenas 16 bits de dados da posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="3b758-144">Note that the **WM\_HSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="3b758-145">Assim, os aplicativos que dependem exclusivamente do **WM \_ HSCROLL** (e do [**WM \_ VSCROLL**](wm-vscroll.md)) para os dados da posição de rolagem têm um valor de posição máximo prático de 65.535.</span><span class="sxs-lookup"><span data-stu-id="3b758-145">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="3b758-146">No entanto, como as funções [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) dão suporte a dados de posição da barra de rolagem de 32 bits, há uma maneira de burlar a barreira de 16 bits das mensagens do **WM \_ HSCROLL** e do [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="3b758-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the **WM\_HSCROLL** and [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span> <span data-ttu-id="3b758-147">Consulte **GetScrollInfo** para obter uma descrição da técnica.</span><span class="sxs-lookup"><span data-stu-id="3b758-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b758-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b758-148">Requirements</span></span>



| <span data-ttu-id="3b758-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b758-149">Requirement</span></span> | <span data-ttu-id="3b758-150">Valor</span><span class="sxs-lookup"><span data-stu-id="3b758-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b758-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b758-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3b758-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b758-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b758-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b758-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3b758-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b758-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b758-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b758-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b758-156"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b758-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b758-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b758-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b758-158">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3b758-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b758-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="3b758-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="3b758-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="3b758-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="3b758-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="3b758-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="3b758-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="3b758-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="3b758-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="3b758-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="3b758-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="3b758-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="3b758-165">**WM \_ HSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="3b758-165">**WM\_HSCROLL (trackbar)**</span></span>](wm-hscroll--trackbar-.md)
</dt> <dt>

[<span data-ttu-id="3b758-166">**VSCROLL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3b758-166">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

