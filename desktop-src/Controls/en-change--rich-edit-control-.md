---
title: Código de notificação de EN_CHANGE (Rich Edit) (WinUser. h)
description: Notifica uma janela de host do controle de edição rico sem janela que ocorreu uma alteração. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE de código de notificação (Rich Edit) controles do Windows
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918278"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="8e53e-105">\_Código de notificação de alteração (Rich Edit)</span><span class="sxs-lookup"><span data-stu-id="8e53e-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="8e53e-106">Notifica uma janela de host do controle de edição rico sem janela que ocorreu uma alteração.</span><span class="sxs-lookup"><span data-stu-id="8e53e-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="8e53e-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e53e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8e53e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e53e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e53e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e53e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e53e-110">Uma estrutura [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) que especifica a alteração feita.</span><span class="sxs-lookup"><span data-stu-id="8e53e-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e53e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e53e-111">Return value</span></span>

<span data-ttu-id="8e53e-112">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8e53e-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e53e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e53e-113">Remarks</span></span>

<span data-ttu-id="8e53e-114">Para receber \_ códigos de notificação de alteração, [**especifique enm \_ alteração**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="8e53e-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e53e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e53e-115">Requirements</span></span>



| <span data-ttu-id="8e53e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e53e-116">Requirement</span></span> | <span data-ttu-id="8e53e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8e53e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e53e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e53e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e53e-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e53e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e53e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e53e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e53e-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e53e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e53e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e53e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e53e-123"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e53e-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e53e-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8e53e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e53e-125">**TxNotify**</span><span class="sxs-lookup"><span data-stu-id="8e53e-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





