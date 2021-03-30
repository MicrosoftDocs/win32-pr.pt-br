---
title: DTN_FORMAT código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) para solicitar que o texto seja exibido em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455452"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="db384-105">\_Código de notificação do formato DTN</span><span class="sxs-lookup"><span data-stu-id="db384-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="db384-106">Enviado por um controle do seletor de data e hora (DTP) para solicitar que o texto seja exibido em um campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="db384-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="db384-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="db384-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="db384-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db384-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db384-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db384-110">Um ponteiro para uma estrutura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) que contém informações sobre esta instância do código de notificação.</span><span class="sxs-lookup"><span data-stu-id="db384-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="db384-111">A estrutura contém a subcadeia de caracteres que define o campo de retorno de chamada e recebe a cadeia de caracteres formatada que o controle exibirá.</span><span class="sxs-lookup"><span data-stu-id="db384-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db384-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db384-112">Return value</span></span>

<span data-ttu-id="db384-113">O proprietário do controle deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="db384-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="db384-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db384-114">Remarks</span></span>

<span data-ttu-id="db384-115">Manipular esse código de notificação permite que o proprietário do controle forneça uma cadeia de caracteres personalizada que o controle exibirá.</span><span class="sxs-lookup"><span data-stu-id="db384-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="db384-116">(Para obter informações adicionais sobre campos de retorno de chamada, consulte [campos de retorno de chamada](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="db384-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="db384-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db384-117">Requirements</span></span>



| <span data-ttu-id="db384-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db384-118">Requirement</span></span> | <span data-ttu-id="db384-119">Valor</span><span class="sxs-lookup"><span data-stu-id="db384-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db384-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db384-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db384-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db384-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db384-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db384-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db384-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db384-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db384-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db384-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db384-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db384-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db384-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="db384-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db384-127">**DTN \_ FORMATW** (Unicode) e **DTN \_ formata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db384-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 





