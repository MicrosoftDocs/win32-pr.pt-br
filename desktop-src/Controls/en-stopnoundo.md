---
title: EN_STOPNOUNDO código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que ocorreu uma ação para a qual o controle não pode alocar memória suficiente para manter o estado de desfazer. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086178"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="81068-105">\_Código de notificação en STOPNOUNDO</span><span class="sxs-lookup"><span data-stu-id="81068-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="81068-106">Notifica uma janela pai do controle de edição rico que ocorreu uma ação para a qual o controle não pode alocar memória suficiente para manter o estado de desfazer.</span><span class="sxs-lookup"><span data-stu-id="81068-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="81068-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="81068-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="81068-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81068-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81068-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81068-110">Uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="81068-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81068-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81068-111">Return value</span></span>

<span data-ttu-id="81068-112">Retornar zero para continuar a operação de **desfazer** .</span><span class="sxs-lookup"><span data-stu-id="81068-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="81068-113">Retornar um valor diferente de zero para interromper a operação de **desfazer** .</span><span class="sxs-lookup"><span data-stu-id="81068-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="81068-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81068-114">Remarks</span></span>

<span data-ttu-id="81068-115">A janela pai sempre obterá uma mensagem de [**\_ notificação do WM**](wm-notify.md) para esse evento; ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="81068-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81068-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81068-116">Requirements</span></span>



| <span data-ttu-id="81068-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81068-117">Requirement</span></span> | <span data-ttu-id="81068-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81068-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81068-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81068-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81068-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81068-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81068-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81068-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81068-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81068-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81068-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81068-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81068-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81068-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81068-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="81068-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="81068-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="81068-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81068-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="81068-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="81068-128">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="81068-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





