---
title: EN_PROTECTED código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário está realizando uma ação que alteraria um intervalo de texto protegido. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455233"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="cd746-105">Código de notificação do EN \_ Protected</span><span class="sxs-lookup"><span data-stu-id="cd746-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="cd746-106">Notifica uma janela pai do controle de edição rico que o usuário está realizando uma ação que alteraria um intervalo de texto protegido.</span><span class="sxs-lookup"><span data-stu-id="cd746-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="cd746-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cd746-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cd746-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd746-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd746-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd746-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd746-110">Uma estrutura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) que contém informações sobre a mensagem que disparou o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="cd746-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd746-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd746-111">Return value</span></span>

<span data-ttu-id="cd746-112">Retornar zero para permitir a operação.</span><span class="sxs-lookup"><span data-stu-id="cd746-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="cd746-113">Retornar um valor diferente de zero para impedir a operação.</span><span class="sxs-lookup"><span data-stu-id="cd746-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd746-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd746-114">Remarks</span></span>

<span data-ttu-id="cd746-115">Se zero for retornado e os membros **msg**, **wParam** e **lParam** da estrutura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) forem alterados, o controle processará a mensagem revisada em vez da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="cd746-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="cd746-116">Para receber códigos de notificação do EN \_ Protected, especifique [**enm \_ Protected**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="cd746-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd746-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd746-117">Requirements</span></span>



| <span data-ttu-id="cd746-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd746-118">Requirement</span></span> | <span data-ttu-id="cd746-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cd746-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd746-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd746-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd746-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd746-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd746-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd746-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd746-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd746-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd746-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd746-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd746-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd746-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd746-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd746-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd746-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cd746-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd746-128">**PROTEGIDO**</span><span class="sxs-lookup"><span data-stu-id="cd746-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="cd746-129">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd746-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





