---
title: LVN_LINKCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista em que um link foi clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456051"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="e62e4-105">Código de notificação do LVN \_ LINKCLICK</span><span class="sxs-lookup"><span data-stu-id="e62e4-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="e62e4-106">Notifica uma janela pai do controle de exibição de lista em que um link foi clicado.</span><span class="sxs-lookup"><span data-stu-id="e62e4-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="e62e4-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e62e4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="e62e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e62e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e62e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e62e4-110">Ponteiro para uma estrutura [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) .</span><span class="sxs-lookup"><span data-stu-id="e62e4-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="e62e4-111">O identificador do grupo que contém o link está no membro **iSubItem** .</span><span class="sxs-lookup"><span data-stu-id="e62e4-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62e4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e62e4-112">Return value</span></span>

<span data-ttu-id="e62e4-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e62e4-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e62e4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e62e4-114">Remarks</span></span>

<span data-ttu-id="e62e4-115">O exemplo a seguir mostra como um aplicativo pode responder a esse código de notificação em seu manipulador de mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e62e4-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="e62e4-116">O exemplo alterna o estado recolhido do grupo e define o texto do link apropriado.</span><span class="sxs-lookup"><span data-stu-id="e62e4-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="e62e4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e62e4-117">Requirements</span></span>



| <span data-ttu-id="e62e4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e62e4-118">Requirement</span></span> | <span data-ttu-id="e62e4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e62e4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e62e4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e62e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e62e4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e62e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e62e4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e62e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e62e4-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e62e4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e62e4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e62e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e62e4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e62e4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





