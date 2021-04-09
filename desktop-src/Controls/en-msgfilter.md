---
title: EN_MSGFILTER código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico de um evento de teclado ou de mouse no controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085639"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="0f437-105">\_Código de notificação en MSGFILTER</span><span class="sxs-lookup"><span data-stu-id="0f437-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="0f437-106">Notifica uma janela pai do controle de edição rico de um evento de teclado ou de mouse no controle.</span><span class="sxs-lookup"><span data-stu-id="0f437-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="0f437-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0f437-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0f437-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f437-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f437-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f437-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f437-110">Uma estrutura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) que contém informações sobre a mensagem do teclado ou do mouse.</span><span class="sxs-lookup"><span data-stu-id="0f437-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="0f437-111">Se a janela pai modificar essa estrutura e retornar um valor diferente de zero, a mensagem modificada será processada em vez da original.</span><span class="sxs-lookup"><span data-stu-id="0f437-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f437-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f437-112">Return value</span></span>

<span data-ttu-id="0f437-113">Retorna zero se o controle deve processar o teclado ou o evento de mouse.</span><span class="sxs-lookup"><span data-stu-id="0f437-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="0f437-114">Retorne diferente de zero se o controle precisar ignorar o evento de teclado ou de mouse.</span><span class="sxs-lookup"><span data-stu-id="0f437-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f437-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f437-115">Remarks</span></span>

<span data-ttu-id="0f437-116">Para receber \_ códigos de notificação do en MSGFILTER para eventos, especifique um ou mais dos seguintes sinalizadores na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="0f437-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="0f437-117">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="0f437-117">Flag</span></span>                                                                             | <span data-ttu-id="0f437-118">Significado</span><span class="sxs-lookup"><span data-stu-id="0f437-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0f437-119">**ENM \_**</span><span class="sxs-lookup"><span data-stu-id="0f437-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="0f437-120">Para receber códigos de notificação para eventos de teclado.</span><span class="sxs-lookup"><span data-stu-id="0f437-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="0f437-121">**ENM \_ MOUSEEVENTS**</span><span class="sxs-lookup"><span data-stu-id="0f437-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="0f437-122">Para receber códigos de notificação para eventos de mouse.</span><span class="sxs-lookup"><span data-stu-id="0f437-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="0f437-123">**ENM \_ SCROLLEVENTS**</span><span class="sxs-lookup"><span data-stu-id="0f437-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="0f437-124">Para receber códigos de notificação para um evento de roda do mouse.</span><span class="sxs-lookup"><span data-stu-id="0f437-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0f437-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f437-125">Requirements</span></span>



| <span data-ttu-id="0f437-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f437-126">Requirement</span></span> | <span data-ttu-id="0f437-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0f437-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f437-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f437-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f437-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f437-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f437-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f437-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f437-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f437-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f437-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f437-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f437-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f437-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f437-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f437-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f437-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0f437-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f437-136">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="0f437-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="0f437-137">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0f437-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





