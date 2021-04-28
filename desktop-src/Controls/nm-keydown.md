---
title: NM_KEYDOWN código de notificação (commctrl. h)
description: NM_KEYDOWN código de notificação – enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN de código de notificação controles do Windows
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
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112344"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="82b58-105">Código de notificação do NM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="82b58-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="82b58-106">Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla.</span><span class="sxs-lookup"><span data-stu-id="82b58-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="82b58-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="82b58-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="82b58-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82b58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82b58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82b58-110">Um ponteiro para uma estrutura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contém informações adicionais sobre a chave que causou o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="82b58-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b58-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="82b58-111">Return value</span></span>

<span data-ttu-id="82b58-112">Retornar diferente de zero para impedir que o controle processe a chave ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="82b58-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b58-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b58-113">Requirements</span></span>



| <span data-ttu-id="82b58-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b58-114">Requirement</span></span> | <span data-ttu-id="82b58-115">Valor</span><span class="sxs-lookup"><span data-stu-id="82b58-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82b58-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82b58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82b58-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82b58-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82b58-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82b58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82b58-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82b58-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82b58-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82b58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b58-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b58-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





