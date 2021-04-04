---
title: EN_SAVECLIPBOARD código de notificação (RichEdit. h)
description: Notifica a janela pai do controle de edição rico que o controle está fechando e a área de transferência contém informações. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824340"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="2685c-105">\_Código de notificação en SAVECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="2685c-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="2685c-106">Notifica a janela pai do controle de edição rico que o controle está fechando e a área de transferência contém informações.</span><span class="sxs-lookup"><span data-stu-id="2685c-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="2685c-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2685c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2685c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2685c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2685c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2685c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2685c-110">Uma estrutura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) que contém informações sobre informações da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="2685c-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2685c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2685c-111">Return value</span></span>

<span data-ttu-id="2685c-112">Retorna zero se a área de transferência deve ser disponibilizada para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2685c-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="2685c-113">Retorna um valor diferente de zero se a área de transferência não deve ser salva.</span><span class="sxs-lookup"><span data-stu-id="2685c-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="2685c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2685c-114">Remarks</span></span>

<span data-ttu-id="2685c-115">A janela pai sempre obterá uma mensagem de [**\_ notificação do WM**](wm-notify.md) para esse evento; ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="2685c-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2685c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2685c-116">Requirements</span></span>



| <span data-ttu-id="2685c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2685c-117">Requirement</span></span> | <span data-ttu-id="2685c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2685c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2685c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2685c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2685c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2685c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2685c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2685c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2685c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2685c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2685c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2685c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2685c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2685c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2685c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2685c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2685c-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2685c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2685c-127">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="2685c-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





