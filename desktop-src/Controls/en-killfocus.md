---
title: Código de notificação EN_KILLFOCUS (WinUser. h)
description: Enviado quando um controle de edição perde o foco do teclado. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ .
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_KILLFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c30c037d985647f50b93402667832b18b3897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824200"
---
# <a name="en_killfocus-notification-code"></a><span data-ttu-id="041a0-105">\_Código de notificação en KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="041a0-105">EN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="041a0-106">Enviado quando um controle de edição perde o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="041a0-106">Sent when an edit control loses the keyboard focus.</span></span> <span data-ttu-id="041a0-107">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="041a0-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="041a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="041a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="041a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="041a0-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="041a0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="041a0-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="041a0-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="041a0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="041a0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="041a0-113">Identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="041a0-113">Handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="041a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="041a0-114">Remarks</span></span>

<span data-ttu-id="041a0-115">A janela pai sempre recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para esse evento, ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="041a0-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="041a0-116">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="041a0-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="041a0-117">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="041a0-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="041a0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="041a0-118">Requirements</span></span>



| <span data-ttu-id="041a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="041a0-119">Requirement</span></span> | <span data-ttu-id="041a0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="041a0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041a0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="041a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="041a0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="041a0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="041a0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="041a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="041a0-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="041a0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="041a0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="041a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="041a0-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="041a0-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041a0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="041a0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="041a0-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="041a0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="041a0-129">**EN \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="041a0-129">**EN\_SETFOCUS**</span></span>](en-setfocus.md)
</dt> <dt>

<span data-ttu-id="041a0-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="041a0-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="041a0-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="041a0-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

