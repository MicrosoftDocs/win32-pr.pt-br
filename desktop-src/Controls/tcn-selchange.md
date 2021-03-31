---
title: TCN_SELCHANGE código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de guia que a guia selecionada atualmente foi alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644240"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="8a67f-105">Código de notificação de SELCHANGE de TCN \_</span><span class="sxs-lookup"><span data-stu-id="8a67f-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="8a67f-106">Notifica uma janela pai do controle de guia que a guia selecionada atualmente foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8a67f-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="8a67f-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8a67f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8a67f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a67f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a67f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a67f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a67f-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="8a67f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a67f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a67f-111">Return value</span></span>

<span data-ttu-id="8a67f-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8a67f-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a67f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a67f-113">Remarks</span></span>

<span data-ttu-id="8a67f-114">Para determinar a guia selecionada no momento, use a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="8a67f-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a67f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a67f-115">Requirements</span></span>



| <span data-ttu-id="8a67f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a67f-116">Requirement</span></span> | <span data-ttu-id="8a67f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8a67f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a67f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a67f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a67f-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a67f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a67f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a67f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a67f-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a67f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a67f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a67f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a67f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a67f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a67f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a67f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a67f-125">SELCHANGING de TCN \_</span><span class="sxs-lookup"><span data-stu-id="8a67f-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





