---
title: Código de notificação de NM_DBLCLK (guia) (commctrl. h)
description: Notifica uma janela pai de um controle guia que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Código de notificação de NM_DBLCLK (guia) controles do Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086147"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="59610-105">\_Código de notificação nm DBLCLK (guia)</span><span class="sxs-lookup"><span data-stu-id="59610-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="59610-106">Notifica uma janela pai de um controle guia que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="59610-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="59610-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="59610-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="59610-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59610-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59610-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59610-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59610-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="59610-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59610-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59610-111">Return value</span></span>

<span data-ttu-id="59610-112">Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="59610-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="59610-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59610-113">Requirements</span></span>



| <span data-ttu-id="59610-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="59610-114">Requirement</span></span> | <span data-ttu-id="59610-115">Valor</span><span class="sxs-lookup"><span data-stu-id="59610-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59610-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59610-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59610-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59610-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59610-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59610-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59610-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59610-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59610-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59610-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59610-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59610-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





