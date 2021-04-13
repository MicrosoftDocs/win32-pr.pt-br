---
title: Código de notificação EN_MAXTEXT (WinUser. h)
description: Enviado quando a inserção do texto atual excedeu o número especificado de caracteres para o controle de edição.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499668"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="9903d-104">\_Código de notificação en MAXTEXT</span><span class="sxs-lookup"><span data-stu-id="9903d-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="9903d-105">Enviado quando a inserção do texto atual excedeu o número especificado de caracteres para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="9903d-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="9903d-106">A inserção do texto foi truncada.</span><span class="sxs-lookup"><span data-stu-id="9903d-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="9903d-107">Esse código de notificação também é enviado quando um controle de edição não tem o estilo [**es \_ AUTOHSCROLL**](edit-control-styles.md) e o número de caracteres a serem inseridos excede a largura do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="9903d-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="9903d-108">Esse código de notificação também é enviado quando um controle de edição não tem o estilo [**es \_ AUTOVSCROLL**](edit-control-styles.md) e o número total de linhas resultante de uma inserção de texto excede a altura do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="9903d-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="9903d-109">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9903d-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="9903d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9903d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9903d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9903d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9903d-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="9903d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="9903d-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="9903d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9903d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9903d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9903d-115">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="9903d-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9903d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9903d-116">Remarks</span></span>

<span data-ttu-id="9903d-117">A janela pai sempre recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para esse evento, ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="9903d-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="9903d-118">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9903d-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9903d-119">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9903d-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9903d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9903d-120">Requirements</span></span>



| <span data-ttu-id="9903d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9903d-121">Requirement</span></span> | <span data-ttu-id="9903d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9903d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9903d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9903d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9903d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9903d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9903d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9903d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9903d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9903d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9903d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9903d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9903d-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9903d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9903d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9903d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9903d-130">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9903d-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

