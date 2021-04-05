---
title: EN_REQUESTRESIZE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o conteúdo do controle é menor ou maior do que o tamanho da janela do controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085828"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="9105c-105">\_Código de notificação en REQUESTRESIZE</span><span class="sxs-lookup"><span data-stu-id="9105c-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="9105c-106">Notifica uma janela pai do controle de edição rico que o conteúdo do controle é menor ou maior do que o tamanho da janela do controle.</span><span class="sxs-lookup"><span data-stu-id="9105c-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="9105c-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9105c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9105c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9105c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9105c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9105c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9105c-110">Uma estrutura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) que recebe o tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="9105c-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9105c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9105c-111">Return value</span></span>

<span data-ttu-id="9105c-112">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9105c-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9105c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9105c-113">Remarks</span></span>

<span data-ttu-id="9105c-114">Para dar suporte ao comportamento inferior de um controle de edição rico, a janela pai deve redimensionar o controle quando ele recebe esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="9105c-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="9105c-115">Para receber \_ códigos de notificação do en REQUESTRESIZE, especifique [**enm \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9105c-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9105c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9105c-116">Requirements</span></span>



| <span data-ttu-id="9105c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9105c-117">Requirement</span></span> | <span data-ttu-id="9105c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9105c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9105c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9105c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9105c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9105c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9105c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9105c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9105c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9105c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9105c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9105c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9105c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9105c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9105c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9105c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9105c-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9105c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9105c-127">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="9105c-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="9105c-128">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9105c-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





