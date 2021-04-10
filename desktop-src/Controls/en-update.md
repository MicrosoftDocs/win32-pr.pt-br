---
title: Código de notificação EN_UPDATE (WinUser. h)
description: Enviado quando um controle de edição está prestes a ser redesenhado.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086179"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="1a6cb-104">\_Código de notificação de atualização en</span><span class="sxs-lookup"><span data-stu-id="1a6cb-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="1a6cb-105">Enviado quando um controle de edição está prestes a ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="1a6cb-106">Esse código de notificação é enviado depois que o controle tiver formatado o texto, mas antes de exibir o texto.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="1a6cb-107">Isso torna possível redimensionar a janela de controle de edição, se necessário.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="1a6cb-108">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1a6cb-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="1a6cb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a6cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6cb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a6cb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6cb-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="1a6cb-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1a6cb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a6cb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6cb-114">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a6cb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a6cb-115">Remarks</span></span>

<span data-ttu-id="1a6cb-116">**Edição avançada 1,0:** Para receber \_ códigos de notificação de atualização do en, especifique [**enm \_ Update**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6cb-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="1a6cb-117">**Edição avançada 2,0 e posterior:** O sinalizador de [**\_ atualização do enm**](rich-edit-control-event-mask-flags.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="1a6cb-118">O \_ código de notificação de atualização en sempre é recebido.</span><span class="sxs-lookup"><span data-stu-id="1a6cb-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="1a6cb-119">No entanto, quando o Microsoft Rich Edit 3,0 emula o Microsoft Rich Edit 1,0, para receber \_ códigos de notificação de atualização, você deve especificar **enm \_ Update** na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6cb-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="1a6cb-120">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1a6cb-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6cb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a6cb-121">Requirements</span></span>



| <span data-ttu-id="1a6cb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a6cb-122">Requirement</span></span> | <span data-ttu-id="1a6cb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1a6cb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6cb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6cb-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a6cb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a6cb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6cb-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a6cb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a6cb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a6cb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6cb-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a6cb-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6cb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a6cb-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a6cb-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1a6cb-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a6cb-132">alteração de EN \_</span><span class="sxs-lookup"><span data-stu-id="1a6cb-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="1a6cb-133">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1a6cb-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1a6cb-134">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1a6cb-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

