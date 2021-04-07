---
title: DTN_DATETIMECHANGE código de notificação (commctrl. h)
description: Enviado por um controle de data e hora (DTP) sempre que ocorre uma alteração. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824591"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="1431d-105">Código de notificação do DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="1431d-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="1431d-106">Enviado por um controle de data e hora (DTP) sempre que ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="1431d-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="1431d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1431d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1431d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1431d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1431d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1431d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1431d-110">Um ponteiro para uma estrutura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) que contém informações sobre a alteração que ocorreu no controle.</span><span class="sxs-lookup"><span data-stu-id="1431d-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1431d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1431d-111">Return value</span></span>

<span data-ttu-id="1431d-112">O proprietário do controle deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="1431d-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1431d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1431d-113">Requirements</span></span>



| <span data-ttu-id="1431d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1431d-114">Requirement</span></span> | <span data-ttu-id="1431d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1431d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1431d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1431d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1431d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1431d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1431d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1431d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1431d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1431d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1431d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1431d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1431d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1431d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





