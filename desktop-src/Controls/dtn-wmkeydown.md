---
title: DTN_WMKEYDOWN código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando o usuário digita em um campo de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085254"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="64d77-105">Código de notificação do DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="64d77-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="64d77-106">Enviado por um controle do seletor de data e hora (DTP) quando o usuário digita em um campo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="64d77-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="64d77-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="64d77-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="64d77-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64d77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64d77-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d77-110">Um ponteiro para uma estrutura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) que contém informações sobre esta instância do código de notificação.</span><span class="sxs-lookup"><span data-stu-id="64d77-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="64d77-111">A estrutura inclui informações sobre a chave que o usuário digitou, a subcadeia de caracteres que define o campo de retorno de chamada e a data e hora atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="64d77-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d77-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64d77-112">Return value</span></span>

<span data-ttu-id="64d77-113">O proprietário do controle deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="64d77-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="64d77-114">Remarks</span></span>

<span data-ttu-id="64d77-115">Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.</span><span class="sxs-lookup"><span data-stu-id="64d77-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d77-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d77-116">Requirements</span></span>



| <span data-ttu-id="64d77-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d77-117">Requirement</span></span> | <span data-ttu-id="64d77-118">Valor</span><span class="sxs-lookup"><span data-stu-id="64d77-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64d77-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d77-119">Minimum supported client</span></span><br/> | <span data-ttu-id="64d77-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64d77-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64d77-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d77-121">Minimum supported server</span></span><br/> | <span data-ttu-id="64d77-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64d77-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64d77-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64d77-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d77-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d77-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="64d77-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="64d77-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64d77-126">**DTN \_ WMKEYDOWNW** (Unicode) e **DTN \_ WMKEYDOWNA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64d77-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





