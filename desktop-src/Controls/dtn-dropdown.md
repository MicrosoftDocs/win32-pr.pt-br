---
title: DTN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando o usuário ativa o calendário do mês suspenso. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824590"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="c828c-105">\_Código de notificação da lista suspensa DTN</span><span class="sxs-lookup"><span data-stu-id="c828c-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="c828c-106">Enviado por um controle do seletor de data e hora (DTP) quando o usuário ativa o calendário do mês suspenso.</span><span class="sxs-lookup"><span data-stu-id="c828c-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="c828c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c828c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="c828c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c828c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c828c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c828c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c828c-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre a notificação.</span><span class="sxs-lookup"><span data-stu-id="c828c-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c828c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c828c-111">Return value</span></span>

<span data-ttu-id="c828c-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="c828c-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c828c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c828c-113">Remarks</span></span>

<span data-ttu-id="c828c-114">Uma tarefa que seu manipulador de notificação pode precisar executar é personalizar o controle de calendário de mês suspenso.</span><span class="sxs-lookup"><span data-stu-id="c828c-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="c828c-115">Por exemplo, se você não quiser "ir para hoje", precisará definir o estilo [**MCS \_ noToday**](month-calendar-control-styles.md)  do controle.</span><span class="sxs-lookup"><span data-stu-id="c828c-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="c828c-116">Para recuperar um identificador para o controle mês-Calendar, envie o controle DTP a uma mensagem [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) .</span><span class="sxs-lookup"><span data-stu-id="c828c-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="c828c-117">Você pode usar esse identificador e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir o estilo de calendário de mês desejado.</span><span class="sxs-lookup"><span data-stu-id="c828c-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="c828c-118">Os controles DTP não mantêm um controle de calendário de mês filho estático.</span><span class="sxs-lookup"><span data-stu-id="c828c-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="c828c-119">O controle DTP cria um novo controle de calendário mensal antes de enviar este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="c828c-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="c828c-120">Além disso, o controle DTP destrói o controle filho quando ele não está ativo (visível).</span><span class="sxs-lookup"><span data-stu-id="c828c-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="c828c-121">Portanto, seu aplicativo não deve depender de um identificador de janela estático para o calendário do mês filho do controle.</span><span class="sxs-lookup"><span data-stu-id="c828c-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="c828c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c828c-122">Requirements</span></span>



| <span data-ttu-id="c828c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c828c-123">Requirement</span></span> | <span data-ttu-id="c828c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c828c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c828c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c828c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c828c-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c828c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c828c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c828c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c828c-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c828c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c828c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c828c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c828c-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c828c-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c828c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c828c-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c828c-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c828c-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c828c-133">DTN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="c828c-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="c828c-134">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="c828c-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

