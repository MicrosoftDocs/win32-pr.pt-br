---
title: Código de notificação EN_CHANGE (WinUser. h)
description: Enviado quando o usuário executou uma ação que pode ter alterado o texto em um controle de edição.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824300"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="6d3f1-104">& \_ código de notificação de alteração</span><span class="sxs-lookup"><span data-stu-id="6d3f1-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="6d3f1-105">Enviado quando o usuário executou uma ação que pode ter alterado o texto em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="6d3f1-106">Ao contrário do código de notificação da [ \_ atualização en](en-update.md) , esse código de notificação é enviado depois que o sistema atualiza a tela.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="6d3f1-107">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6d3f1-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d3f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d3f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d3f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d3f1-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="6d3f1-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6d3f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d3f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d3f1-113">Um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d3f1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d3f1-114">Remarks</span></span>

<span data-ttu-id="6d3f1-115">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6d3f1-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6d3f1-116">Para receber \_ códigos de notificação de alteração, [**especifique enm \_ alteração**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="6d3f1-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="6d3f1-117">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6d3f1-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="6d3f1-118">O \_ código de notificação de alteração en não é enviado quando o estilo [**\_ multilinha es**](edit-control-styles.md) é usado e o texto é enviado por meio do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="6d3f1-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3f1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d3f1-119">Requirements</span></span>



| <span data-ttu-id="6d3f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3f1-120">Requirement</span></span> | <span data-ttu-id="6d3f1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6d3f1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3f1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d3f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3f1-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d3f1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d3f1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d3f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3f1-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d3f1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d3f1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d3f1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d3f1-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d3f1-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d3f1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d3f1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d3f1-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6d3f1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d3f1-130">atualização do EN \_</span><span class="sxs-lookup"><span data-stu-id="6d3f1-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="6d3f1-131">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6d3f1-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6d3f1-132">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6d3f1-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

