---
title: TCN_SELCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle guia que a guia selecionada atualmente está prestes a ser alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755420"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="fcf67-105">Código de notificação de SELCHANGING de TCN \_</span><span class="sxs-lookup"><span data-stu-id="fcf67-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="fcf67-106">Notifica uma janela pai do controle guia que a guia selecionada atualmente está prestes a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="fcf67-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="fcf67-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fcf67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fcf67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcf67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcf67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcf67-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="fcf67-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf67-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcf67-111">Return value</span></span>

<span data-ttu-id="fcf67-112">Retorna **true** para impedir que a seleção seja alterada ou **false** para permitir que a seleção seja alterada.</span><span class="sxs-lookup"><span data-stu-id="fcf67-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf67-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcf67-113">Remarks</span></span>

<span data-ttu-id="fcf67-114">Para determinar a guia selecionada no momento, use a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="fcf67-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf67-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcf67-115">Requirements</span></span>



| <span data-ttu-id="fcf67-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf67-116">Requirement</span></span> | <span data-ttu-id="fcf67-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fcf67-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf67-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcf67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf67-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcf67-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcf67-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcf67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf67-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcf67-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcf67-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcf67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf67-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf67-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf67-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcf67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf67-125">SELCHANGE de TCN \_</span><span class="sxs-lookup"><span data-stu-id="fcf67-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





