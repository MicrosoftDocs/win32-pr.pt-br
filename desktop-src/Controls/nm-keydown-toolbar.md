---
title: Código de notificação de NM_KEYDOWN (barra de ferramentas) (commctrl. h)
description: Código de notificação de NM_KEYDOWN (barra de ferramentas) – enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Código de notificação de NM_KEYDOWN (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112354"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="be593-105">\_Código de notificação do nm KEYDOWN (Toolbar)</span><span class="sxs-lookup"><span data-stu-id="be593-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="be593-106">Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla.</span><span class="sxs-lookup"><span data-stu-id="be593-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="be593-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="be593-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="be593-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be593-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be593-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be593-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be593-110">Ponteiro para uma estrutura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contém informações adicionais sobre a chave que causou o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="be593-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be593-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be593-111">Return value</span></span>

<span data-ttu-id="be593-112">Retornar diferente de zero para impedir que o controle processe a chave ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="be593-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="be593-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be593-113">Remarks</span></span>

<span data-ttu-id="be593-114">Atualmente, somente o controle Toolbar envia esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="be593-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="be593-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be593-115">Requirements</span></span>



| <span data-ttu-id="be593-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="be593-116">Requirement</span></span> | <span data-ttu-id="be593-117">Valor</span><span class="sxs-lookup"><span data-stu-id="be593-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be593-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be593-118">Minimum supported client</span></span><br/> | <span data-ttu-id="be593-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be593-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be593-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be593-120">Minimum supported server</span></span><br/> | <span data-ttu-id="be593-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be593-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be593-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be593-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="be593-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be593-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





