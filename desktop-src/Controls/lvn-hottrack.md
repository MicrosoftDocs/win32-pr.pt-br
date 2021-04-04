---
title: LVN_HOTTRACK código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item. Este código de notificação é enviado somente por controles de exibição de lista que têm \_ o \_ estilo de exibição de lista estendida LVS ex TRACKSELECT. Ele é enviado na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824859"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="af014-106">Código de notificação do LVN \_ HOTTRACK</span><span class="sxs-lookup"><span data-stu-id="af014-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="af014-107">Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item.</span><span class="sxs-lookup"><span data-stu-id="af014-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="af014-108">Este código de notificação é enviado somente por controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="af014-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="af014-109">Ele é enviado na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="af014-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="af014-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af014-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af014-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af014-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af014-112">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="af014-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="af014-113">Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="af014-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="af014-114">O aplicativo receptor pode modificar o membro **iItem** para especificar o item que será selecionado.</span><span class="sxs-lookup"><span data-stu-id="af014-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="af014-115">Se **iItem** for definido como-1, nenhum item será selecionado.</span><span class="sxs-lookup"><span data-stu-id="af014-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af014-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af014-116">Return value</span></span>

<span data-ttu-id="af014-117">Retornar zero para permitir que o modo de exibição de lista execute seu processamento normal de faixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="af014-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="af014-118">Se o aplicativo retornar um zero diferente, o item não será selecionado.</span><span class="sxs-lookup"><span data-stu-id="af014-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="af014-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af014-119">Requirements</span></span>



| <span data-ttu-id="af014-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af014-120">Requirement</span></span> | <span data-ttu-id="af014-121">Valor</span><span class="sxs-lookup"><span data-stu-id="af014-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af014-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af014-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af014-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af014-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af014-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af014-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af014-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af014-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af014-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af014-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af014-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af014-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





