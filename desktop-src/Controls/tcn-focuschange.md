---
title: TCN_FOCUSCHANGE código de notificação (commctrl. h)
description: Notifica uma janela pai do controle guia que o foco do botão foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644241"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="f4e7e-105">Código de notificação de FOCUSCHANGE de TCN \_</span><span class="sxs-lookup"><span data-stu-id="f4e7e-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="f4e7e-106">Notifica uma janela pai do controle guia que o foco do botão foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f4e7e-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="f4e7e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f4e7e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f4e7e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4e7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4e7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e7e-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="f4e7e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e7e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4e7e-111">Return value</span></span>

<span data-ttu-id="f4e7e-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f4e7e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e7e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4e7e-113">Requirements</span></span>



| <span data-ttu-id="f4e7e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e7e-114">Requirement</span></span> | <span data-ttu-id="f4e7e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f4e7e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e7e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4e7e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e7e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4e7e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4e7e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4e7e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e7e-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4e7e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4e7e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4e7e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e7e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e7e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





