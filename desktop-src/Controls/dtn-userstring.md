---
title: DTN_USERSTRING código de notificação (commctrl. h)
description: Enviado por um controle do seletor de data e hora (DTP) quando um usuário termina de editar uma cadeia de caracteres no controle.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824226"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="aa362-104">Código de notificação do DTN \_ userstring</span><span class="sxs-lookup"><span data-stu-id="aa362-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="aa362-105">Enviado por um controle do seletor de data e hora (DTP) quando um usuário termina de editar uma cadeia de caracteres no controle.</span><span class="sxs-lookup"><span data-stu-id="aa362-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="aa362-106">Esse código de notificação é enviado somente por controles DTP que são definidos para o estilo [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="aa362-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="aa362-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aa362-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aa362-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa362-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa362-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa362-110">Um ponteiro para uma estrutura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) que contém informações sobre a instância do código de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa362-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa362-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa362-111">Return value</span></span>

<span data-ttu-id="aa362-112">O proprietário do controle deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="aa362-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa362-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa362-113">Remarks</span></span>

<span data-ttu-id="aa362-114">Manipular esse código de notificação permite que o proprietário forneça respostas personalizadas para cadeias de caracteres inseridas no controle pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aa362-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="aa362-115">O proprietário deve estar preparado para analisar a cadeia de caracteres de entrada e tomar medidas, se necessário.</span><span class="sxs-lookup"><span data-stu-id="aa362-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa362-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa362-116">Requirements</span></span>



| <span data-ttu-id="aa362-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa362-117">Requirement</span></span> | <span data-ttu-id="aa362-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa362-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa362-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa362-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa362-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa362-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa362-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa362-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa362-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa362-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa362-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa362-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa362-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa362-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aa362-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="aa362-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aa362-126">**DTN \_ USERSTRINGW** (Unicode) e **DTN \_ userstringa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aa362-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





