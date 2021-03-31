---
title: EN_SELCHANGE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que a seleção atual foi alterada. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645032"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="82251-105">\_Código de notificação en SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="82251-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="82251-106">Notifica uma janela pai do controle de edição rico que a seleção atual foi alterada.</span><span class="sxs-lookup"><span data-stu-id="82251-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="82251-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="82251-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="82251-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82251-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82251-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82251-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82251-110">Uma estrutura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que recebe informações sobre a seleção.</span><span class="sxs-lookup"><span data-stu-id="82251-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82251-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82251-111">Return value</span></span>

<span data-ttu-id="82251-112">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="82251-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82251-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="82251-113">Remarks</span></span>

<span data-ttu-id="82251-114">Para receber \_ códigos de notificação do en SELCHANGE, especifique [**enm \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="82251-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="82251-115">Esse código de notificação é enviado quando a posição do cursor é alterada e nenhum texto é selecionado (a seleção está vazia).</span><span class="sxs-lookup"><span data-stu-id="82251-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="82251-116">A posição do cursor pode ser alterada quando o usuário clica no mouse, digita ou pressiona uma tecla de direção.</span><span class="sxs-lookup"><span data-stu-id="82251-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="82251-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82251-117">Requirements</span></span>



| <span data-ttu-id="82251-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="82251-118">Requirement</span></span> | <span data-ttu-id="82251-119">Valor</span><span class="sxs-lookup"><span data-stu-id="82251-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82251-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82251-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82251-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82251-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82251-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82251-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82251-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82251-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82251-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82251-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="82251-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="82251-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82251-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="82251-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="82251-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="82251-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="82251-128">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="82251-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="82251-129">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="82251-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





