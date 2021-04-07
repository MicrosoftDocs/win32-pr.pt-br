---
title: Código de notificação EN_HSCROLL (WinUser. h)
description: Enviado quando o usuário clica na barra de rolagem horizontal do controle de edição. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ . A janela pai é notificada antes da atualização da tela.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824521"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="0b170-106">\_Código de notificação en HSCROLL</span><span class="sxs-lookup"><span data-stu-id="0b170-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="0b170-107">Enviado quando o usuário clica na barra de rolagem horizontal do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0b170-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="0b170-108">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0b170-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="0b170-109">A janela pai é notificada antes da atualização da tela.</span><span class="sxs-lookup"><span data-stu-id="0b170-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0b170-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b170-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b170-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b170-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b170-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0b170-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="0b170-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0b170-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0b170-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b170-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b170-115">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0b170-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b170-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b170-116">Remarks</span></span>

<span data-ttu-id="0b170-117">Este código de notificação é enviado para os seguintes eventos de mouse na barra de rolagem horizontal: clicando no botão de seta ou clicando entre o botão de seta e o polegar.</span><span class="sxs-lookup"><span data-stu-id="0b170-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="0b170-118">No entanto, o código de notificação não é enviado ao clicar no polegar da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0b170-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="0b170-119">O código de notificação também é enviado quando um evento de teclado causa uma alteração na área de exibição do controle de edição, por exemplo, pressionando HOME, END, seta para a esquerda ou seta para a direita.</span><span class="sxs-lookup"><span data-stu-id="0b170-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="0b170-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0b170-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="0b170-121">Para receber códigos de notificação do **en \_ HSCROLL** , especifique [**enm \_ Scroll**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="0b170-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="0b170-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0b170-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b170-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b170-123">Requirements</span></span>



| <span data-ttu-id="0b170-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b170-124">Requirement</span></span> | <span data-ttu-id="0b170-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0b170-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b170-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b170-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b170-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b170-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b170-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b170-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b170-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b170-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b170-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b170-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b170-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b170-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b170-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b170-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b170-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0b170-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b170-134">VSCROLL de EN \_</span><span class="sxs-lookup"><span data-stu-id="0b170-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="0b170-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="0b170-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0b170-136">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0b170-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

