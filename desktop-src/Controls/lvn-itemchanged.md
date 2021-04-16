---
title: LVN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753574"
---
# <a name="lvn_itemchanged-notification-code"></a><span data-ttu-id="4d151-105">Código de notificação LVN com \_ alterações</span><span class="sxs-lookup"><span data-stu-id="4d151-105">LVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="4d151-106">Notifica uma janela pai do controle de exibição de lista que um item foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4d151-106">Notifies a list-view control's parent window that an item has changed.</span></span> <span data-ttu-id="4d151-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4d151-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4d151-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d151-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d151-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d151-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d151-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica o item e especifica quais dos seus atributos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="4d151-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes have changed.</span></span> <span data-ttu-id="4d151-111">Se o membro **iItem** da estrutura apontada por *lParam* for-1, a alteração será aplicada a todos os itens na exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="4d151-111">If the **iItem** member of the structure pointed to by *lParam* is -1, the change has been applied to all items in the list view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d151-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d151-112">Return value</span></span>

<span data-ttu-id="4d151-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4d151-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d151-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d151-114">Remarks</span></span>

<span data-ttu-id="4d151-115">Se um controle de exibição de lista tiver o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) e o usuário selecionar um intervalo de itens, mantendo pressionada a tecla Shift e clicando no mouse, os \_ códigos de notificação com alteração de LVN não serão enviados para cada item selecionado ou desmarcado.</span><span class="sxs-lookup"><span data-stu-id="4d151-115">If a list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, and the user selects a range of items by holding down the SHIFT key and clicking the mouse, LVN\_ITEMCHANGED notification codes are not sent for each selected or deselected item.</span></span> <span data-ttu-id="4d151-116">Em vez disso, você receberá um único código de notificação [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) , indicando que um intervalo de itens alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="4d151-116">Instead, you will receive a single [LVN\_ODSTATECHANGED](lvn-odstatechanged.md) notification code, indicating that a range of items has changed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d151-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d151-117">Requirements</span></span>



| <span data-ttu-id="4d151-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d151-118">Requirement</span></span> | <span data-ttu-id="4d151-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4d151-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d151-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d151-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d151-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d151-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d151-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d151-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d151-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d151-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d151-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d151-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d151-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d151-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





