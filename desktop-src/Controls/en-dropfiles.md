---
title: EN_DROPFILES código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário está tentando soltar arquivos no controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM quando recebe \_ a mensagem DropFiles do WM.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454705"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="b7339-105">\_Código de notificação en DropFiles</span><span class="sxs-lookup"><span data-stu-id="b7339-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="b7339-106">Notifica uma janela pai do controle de edição rico que o usuário está tentando soltar arquivos no controle.</span><span class="sxs-lookup"><span data-stu-id="b7339-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="b7339-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) quando recebe a mensagem [**\_ DropFiles do WM**](/windows/desktop/shell/wm-dropfiles) .</span><span class="sxs-lookup"><span data-stu-id="b7339-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b7339-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7339-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7339-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7339-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7339-110">Uma estrutura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recebe informações de arquivos soltos.</span><span class="sxs-lookup"><span data-stu-id="b7339-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7339-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7339-111">Return value</span></span>

<span data-ttu-id="b7339-112">Retornar um valor diferente de zero para permitir a operação DROP.</span><span class="sxs-lookup"><span data-stu-id="b7339-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="b7339-113">Retornar zero para ignorar a operação de soltar.</span><span class="sxs-lookup"><span data-stu-id="b7339-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7339-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7339-114">Remarks</span></span>

<span data-ttu-id="b7339-115">Para um controle de edição rico receber mensagens do [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) , a janela pai deve registrar o controle como um destino de soltar usando a função [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) .</span><span class="sxs-lookup"><span data-stu-id="b7339-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="b7339-116">O controle não se registra.</span><span class="sxs-lookup"><span data-stu-id="b7339-116">The control does not register itself.</span></span>

<span data-ttu-id="b7339-117">Para receber \_ códigos de notificação do en DropFiles, especifique [**enm \_ DropFiles**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="b7339-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7339-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7339-118">Requirements</span></span>



| <span data-ttu-id="b7339-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7339-119">Requirement</span></span> | <span data-ttu-id="b7339-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7339-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7339-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7339-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7339-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7339-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7339-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7339-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7339-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7339-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7339-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7339-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7339-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7339-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7339-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7339-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7339-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b7339-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7339-129">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="b7339-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

