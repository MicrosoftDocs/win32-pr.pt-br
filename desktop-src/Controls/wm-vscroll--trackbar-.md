---
title: Código de notificação WM_VSCROLL (TrackBar) (WinUser. h)
description: A mensagem do WM \_ VSCROLL é enviada ao proprietário de um controle TrackBar vertical quando o controle deslizante muda de posição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- TrackBar (código de notificação de WM_VSCROLL) controles do Windows
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085801"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="24bfc-105">\_Código de notificação do WM VSCROLL (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="24bfc-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="24bfc-106">A mensagem do **WM \_ VSCROLL** é enviada ao proprietário de um controle TrackBar vertical quando o controle deslizante muda de posição.</span><span class="sxs-lookup"><span data-stu-id="24bfc-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="24bfc-107">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="24bfc-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="24bfc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24bfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24bfc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24bfc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24bfc-110">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do controle deslizante se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) for TB \_ THUMBPOSITION ou TB \_ THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="24bfc-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="24bfc-111">Para todos os outros códigos de notificação, a palavra de ordem superior é zero; Envie a mensagem [**tbm \_ GETPOS**](tbm-getpos.md) para determinar a posição do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="24bfc-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="24bfc-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica um código de notificação que indica a interação do usuário com o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="24bfc-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="24bfc-113">Esta palavra pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="24bfc-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="24bfc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="24bfc-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="24bfc-115">Significado</span><span class="sxs-lookup"><span data-stu-id="24bfc-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="24bfc-116"><dt>**TB \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="24bfc-117">O usuário pressionou a tecla END ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="24bfc-118"><dt>**endtrack de TB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="24bfc-119">O TrackBar recebeu o [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), o que significa que o usuário lançou uma chave que enviou um código de chave virtual relevante.</span><span class="sxs-lookup"><span data-stu-id="24bfc-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="24bfc-120"><dt>**TB de \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="24bfc-121">O usuário pressionou a tecla seta para a direita ([**VK \_ direita**](/windows/desktop/inputdev/virtual-key-codes)) ou seta para baixo ([**VK \_ down**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="24bfc-122"><dt>**linha de TB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="24bfc-123">O usuário pressionou a tecla seta para a esquerda ([**VK \_ esquerda**](/windows/desktop/inputdev/virtual-key-codes)) ou seta para cima ([**VK \_ cima**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="24bfc-124"><dt>**TB \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="24bfc-125">O usuário clicou no canal abaixo ou à direita do controle deslizante ([**VK \_ Avançar**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="24bfc-126"><dt>**TB de \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="24bfc-127">O usuário clicou no canal acima ou à esquerda do controle deslizante ([**VK \_ anterior**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="24bfc-128"><dt>**TB de \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="24bfc-129">O TrackBar recebeu o [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) seguindo um \_ código de notificação de THUMBTRACK TB.</span><span class="sxs-lookup"><span data-stu-id="24bfc-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="24bfc-130"><dt>**TB de \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="24bfc-131">O usuário arrastou o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="24bfc-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="24bfc-132"><dt>**TB \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="24bfc-133">O usuário pressionou a tecla HOME ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="24bfc-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="24bfc-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24bfc-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24bfc-135">O identificador para o controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="24bfc-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24bfc-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24bfc-136">Return value</span></span>

<span data-ttu-id="24bfc-137">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="24bfc-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24bfc-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="24bfc-138">Remarks</span></span>

<span data-ttu-id="24bfc-139">O código de TB \_ THUMBTRACK é normalmente usado por aplicativos que fornecem comentários quando o usuário arrasta a caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="24bfc-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="24bfc-140">Observe que a mensagem do **WM \_ VSCROLL** transporta apenas 16 bits de dados de posição.</span><span class="sxs-lookup"><span data-stu-id="24bfc-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="24bfc-141">Assim, os aplicativos que dependem exclusivamente do **WM \_ VSCROLL** (e do [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) para os dados da posição do controle deslizante têm um valor de posição máximo prático de 65.535.</span><span class="sxs-lookup"><span data-stu-id="24bfc-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bfc-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24bfc-142">Requirements</span></span>



| <span data-ttu-id="24bfc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="24bfc-143">Requirement</span></span> | <span data-ttu-id="24bfc-144">Valor</span><span class="sxs-lookup"><span data-stu-id="24bfc-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24bfc-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24bfc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="24bfc-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24bfc-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24bfc-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24bfc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="24bfc-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24bfc-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24bfc-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24bfc-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="24bfc-150"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24bfc-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24bfc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="24bfc-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="24bfc-152">**Referência**</span><span class="sxs-lookup"><span data-stu-id="24bfc-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24bfc-153">**HSCROLL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="24bfc-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

