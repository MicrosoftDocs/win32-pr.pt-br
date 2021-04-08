---
title: NM_TOOLTIPSCREATED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle criou um controle ToolTip. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009195"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="881f6-105">\_Código de notificação nm TOOLTIPSCREATED</span><span class="sxs-lookup"><span data-stu-id="881f6-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="881f6-106">Notifica uma janela pai do controle que o controle criou um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="881f6-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="881f6-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="881f6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="881f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="881f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="881f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="881f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="881f6-110">Um ponteiro para uma estrutura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="881f6-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="881f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="881f6-111">Return value</span></span>

<span data-ttu-id="881f6-112">A menos que especificado de outra forma, o controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="881f6-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="881f6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="881f6-113">Requirements</span></span>



| <span data-ttu-id="881f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="881f6-114">Requirement</span></span> | <span data-ttu-id="881f6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="881f6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="881f6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="881f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="881f6-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="881f6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="881f6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="881f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="881f6-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="881f6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="881f6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="881f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="881f6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="881f6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





