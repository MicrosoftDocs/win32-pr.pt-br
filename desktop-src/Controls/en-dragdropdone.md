---
title: EN_DRAGDROPDONE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que a operação de arrastar e soltar foi concluída. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918036"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="62be8-105">\_Código de notificação en DRAGDROPDONE</span><span class="sxs-lookup"><span data-stu-id="62be8-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="62be8-106">Notifica uma janela pai do controle de edição rico que a operação de arrastar e soltar foi concluída.</span><span class="sxs-lookup"><span data-stu-id="62be8-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="62be8-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="62be8-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="62be8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62be8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62be8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62be8-110">Uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="62be8-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62be8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62be8-111">Return value</span></span>

<span data-ttu-id="62be8-112">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="62be8-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62be8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="62be8-113">Remarks</span></span>

<span data-ttu-id="62be8-114">Para receber um \_ código de notificação en DRAGDROPDONE, especifique o sinalizador [**enm \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="62be8-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="62be8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62be8-115">Requirements</span></span>



| <span data-ttu-id="62be8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62be8-116">Requirement</span></span> | <span data-ttu-id="62be8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="62be8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62be8-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62be8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62be8-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62be8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62be8-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62be8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62be8-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62be8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62be8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62be8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62be8-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62be8-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62be8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="62be8-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="62be8-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="62be8-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62be8-126">**em \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="62be8-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





