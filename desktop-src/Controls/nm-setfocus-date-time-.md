---
title: Código de notificação de NM_SETFOCUS (data e hora) (commctrl. h)
description: Notifica uma janela pai do controle seletor de data e hora que o controle recebeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS de código de notificação (data e hora) controles do Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454930"
---
# <a name="nm_setfocus-date-time-notification-code"></a><span data-ttu-id="eab8f-105">\_Código de notificação nm SETFOCUS (data e hora)</span><span class="sxs-lookup"><span data-stu-id="eab8f-105">NM\_SETFOCUS (date time) notification code</span></span>

<span data-ttu-id="eab8f-106">Notifica uma janela pai do controle seletor de data e hora que o controle recebeu o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="eab8f-106">Notifies a date and time picker control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="eab8f-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eab8f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eab8f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eab8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eab8f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eab8f-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="eab8f-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab8f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eab8f-111">Return value</span></span>

<span data-ttu-id="eab8f-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="eab8f-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab8f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eab8f-113">Requirements</span></span>



| <span data-ttu-id="eab8f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab8f-114">Requirement</span></span> | <span data-ttu-id="eab8f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eab8f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eab8f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eab8f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eab8f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eab8f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eab8f-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eab8f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eab8f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eab8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab8f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab8f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





