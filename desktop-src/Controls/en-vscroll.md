---
title: Código de notificação EN_VSCROLL (WinUser. h)
description: Enviado quando o usuário clica na barra de rolagem vertical do controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824793"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="ec8f1-104">\_Código de notificação en VSCROLL</span><span class="sxs-lookup"><span data-stu-id="ec8f1-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="ec8f1-105">Enviado quando o usuário clica na barra de rolagem vertical do controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="ec8f1-106">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ec8f1-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="ec8f1-107">A janela pai é notificada antes da atualização da tela.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="ec8f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec8f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec8f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec8f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec8f1-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="ec8f1-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ec8f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec8f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec8f1-113">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec8f1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec8f1-114">Remarks</span></span>

<span data-ttu-id="ec8f1-115">Esta mensagem é enviada para os seguintes eventos de mouse na barra de rolagem vertical: clicando no botão de seta ou clicando entre o botão de seta e o polegar.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="ec8f1-116">No entanto, a mensagem não é enviada ao clicar no próprio mouse da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="ec8f1-117">A mensagem também é enviada quando um evento de teclado causa uma alteração na área de exibição do controle de edição, por exemplo, pressionando HOME, END, PAGE UP, PAGE DOWN, seta para cima ou seta para baixo.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="ec8f1-118">A roda do mouse é um mouse que tem uma roda central que rola.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="ec8f1-119">Para obter mais informações, consulte "a roda do mouse" [sobre a entrada do mouse](/windows/desktop/inputdev/about-mouse-input).</span><span class="sxs-lookup"><span data-stu-id="ec8f1-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="ec8f1-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ec8f1-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ec8f1-121">Para receber \_ códigos de notificação do en VSCROLL, especifique [**enm \_ Scroll**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8f1-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="ec8f1-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ec8f1-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec8f1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec8f1-123">Requirements</span></span>



| <span data-ttu-id="ec8f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec8f1-124">Requirement</span></span> | <span data-ttu-id="ec8f1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ec8f1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8f1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec8f1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8f1-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec8f1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec8f1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec8f1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8f1-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec8f1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec8f1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec8f1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8f1-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec8f1-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec8f1-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec8f1-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec8f1-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ec8f1-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ec8f1-134">HSCROLL de EN \_</span><span class="sxs-lookup"><span data-stu-id="ec8f1-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="ec8f1-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ec8f1-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ec8f1-136">Usando controles de edição</span><span class="sxs-lookup"><span data-stu-id="ec8f1-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ec8f1-137">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ec8f1-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ec8f1-138">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ec8f1-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

