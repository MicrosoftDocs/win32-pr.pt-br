---
title: EN_OLEOPFAILED código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que uma ação do usuário em um objeto de Component Object Model (COM) falhou. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824458"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="0f2a1-105">\_Código de notificação en OLEOPFAILED</span><span class="sxs-lookup"><span data-stu-id="0f2a1-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="0f2a1-106">Notifica uma janela pai do controle de edição rico que uma ação do usuário em um objeto de Component Object Model (COM) falhou.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="0f2a1-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0f2a1-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0f2a1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f2a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f2a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f2a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f2a1-110">Uma estrutura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) que contém informações sobre a falha.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f2a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f2a1-111">Return value</span></span>

<span data-ttu-id="0f2a1-112">Esse código de notificação retorna zero.</span><span class="sxs-lookup"><span data-stu-id="0f2a1-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f2a1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f2a1-113">Remarks</span></span>

<span data-ttu-id="0f2a1-114">A janela pai sempre obterá uma mensagem de [**\_ notificação do WM**](wm-notify.md) para esse evento; ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="0f2a1-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f2a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f2a1-115">Requirements</span></span>



| <span data-ttu-id="0f2a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f2a1-116">Requirement</span></span> | <span data-ttu-id="0f2a1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0f2a1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2a1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f2a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2a1-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f2a1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f2a1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f2a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2a1-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f2a1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f2a1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f2a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f2a1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f2a1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f2a1-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0f2a1-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f2a1-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0f2a1-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f2a1-126">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="0f2a1-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





