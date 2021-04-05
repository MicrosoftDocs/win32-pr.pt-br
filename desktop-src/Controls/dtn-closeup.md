---
title: DTN_CLOSEUP código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando o usuário fecha o calendário do mês suspenso.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644982"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="0c105-104">Código de notificação do DTN \_ closeup</span><span class="sxs-lookup"><span data-stu-id="0c105-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="0c105-105">Enviado por um controle do seletor de data e hora (DTP) quando o usuário fecha o calendário do mês suspenso.</span><span class="sxs-lookup"><span data-stu-id="0c105-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="0c105-106">O calendário mensal é fechado quando o usuário escolhe uma data do calendário mês ou clica na seta suspensa enquanto o calendário está aberto.</span><span class="sxs-lookup"><span data-stu-id="0c105-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="0c105-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0c105-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="0c105-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c105-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c105-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c105-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c105-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre a notificação.</span><span class="sxs-lookup"><span data-stu-id="0c105-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c105-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c105-111">Return value</span></span>

<span data-ttu-id="0c105-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="0c105-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c105-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c105-113">Remarks</span></span>

<span data-ttu-id="0c105-114">Os controles DTP não mantêm um controle de calendário de mês filho estático.</span><span class="sxs-lookup"><span data-stu-id="0c105-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="0c105-115">O controle DTP destrói o controle de calendário de mês filho antes de enviar este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0c105-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="0c105-116">Portanto, seu aplicativo não deve depender de um identificador de janela estático para o calendário do mês filho do controle.</span><span class="sxs-lookup"><span data-stu-id="0c105-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c105-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c105-117">Requirements</span></span>



| <span data-ttu-id="0c105-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c105-118">Requirement</span></span> | <span data-ttu-id="0c105-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0c105-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c105-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c105-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c105-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c105-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c105-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c105-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c105-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c105-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c105-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c105-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c105-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c105-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c105-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c105-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c105-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0c105-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c105-128">\_lista suspensa DTN</span><span class="sxs-lookup"><span data-stu-id="0c105-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="0c105-129">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="0c105-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





