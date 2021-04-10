---
title: LVN_ITEMCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item está sendo alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919241"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="028b9-105">Código de notificação de LVN de \_ alteração</span><span class="sxs-lookup"><span data-stu-id="028b9-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="028b9-106">Notifica uma janela pai do controle de exibição de lista que um item está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="028b9-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="028b9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="028b9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="028b9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="028b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="028b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="028b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="028b9-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica o item e especifica quais dos seus atributos estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="028b9-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="028b9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="028b9-111">Return value</span></span>

<span data-ttu-id="028b9-112">Retorna **true** para evitar a alteração ou **false** para permitir a alteração.</span><span class="sxs-lookup"><span data-stu-id="028b9-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="028b9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="028b9-113">Remarks</span></span>

<span data-ttu-id="028b9-114">Se o controle de exibição de lista tiver o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , os \_ códigos de notificação de alteração LVN não serão enviados.</span><span class="sxs-lookup"><span data-stu-id="028b9-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="028b9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="028b9-115">Requirements</span></span>



| <span data-ttu-id="028b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="028b9-116">Requirement</span></span> | <span data-ttu-id="028b9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="028b9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="028b9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="028b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="028b9-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="028b9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="028b9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="028b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="028b9-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="028b9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="028b9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="028b9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="028b9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="028b9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





