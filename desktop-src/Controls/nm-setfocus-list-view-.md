---
title: Código de notificação de NM_SETFOCUS (exibição de lista) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que o controle recebeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99cc84e76c0203a6e2930d3d9f50bc61a1e31395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009197"
---
# <a name="nm_setfocus-list-view-notification-code"></a><span data-ttu-id="cac61-105">\_Código de notificação nm SETFOCUS (modo de exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="cac61-105">NM\_SETFOCUS (list view) notification code</span></span>

<span data-ttu-id="cac61-106">Notifica uma janela pai do controle de exibição de lista que o controle recebeu o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="cac61-106">Notifies a list-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="cac61-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cac61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cac61-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cac61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cac61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cac61-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="cac61-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac61-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cac61-111">Return value</span></span>

<span data-ttu-id="cac61-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="cac61-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac61-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac61-113">Requirements</span></span>



| <span data-ttu-id="cac61-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac61-114">Requirement</span></span> | <span data-ttu-id="cac61-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cac61-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cac61-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cac61-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cac61-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cac61-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cac61-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cac61-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cac61-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cac61-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac61-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac61-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





