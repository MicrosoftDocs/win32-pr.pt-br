---
title: LVN_SETDISPINFO código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que ele deve atualizar as informações que ele mantém para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918801"
---
# <a name="lvn_setdispinfo-notification-code"></a><span data-ttu-id="8cc4e-105">Código de notificação do LVN \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="8cc4e-105">LVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="8cc4e-106">Notifica uma janela pai do controle de exibição de lista que ele deve atualizar as informações que ele mantém para um item.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-106">Notifies a list-view control's parent window that it must update the information it maintains for an item.</span></span> <span data-ttu-id="8cc4e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc4e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="8cc4e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cc4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cc4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc4e-110">Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que especifica informações para o item alterado.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure that specifies information for the changed item.</span></span> <span data-ttu-id="8cc4e-111">O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contém informações sobre o item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains information about the item that was changed.</span></span> <span data-ttu-id="8cc4e-112">O membro **pszText** do **Item** contém um valor válido, independentemente de o sinalizador de \_ texto LVIF ser definido no membro **Mask** dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-112">The **pszText** member of **item** contains a valid value, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc4e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cc4e-113">Return value</span></span>

<span data-ttu-id="8cc4e-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc4e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc4e-115">Remarks</span></span>

<span data-ttu-id="8cc4e-116">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8cc4e-116">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="8cc4e-117">O parâmetro *wParam* contém o código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8cc4e-117">The *wParam* parameter contains the message code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc4e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc4e-118">Requirements</span></span>



| <span data-ttu-id="8cc4e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc4e-119">Requirement</span></span> | <span data-ttu-id="8cc4e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc4e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc4e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cc4e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc4e-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cc4e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cc4e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cc4e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc4e-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cc4e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cc4e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cc4e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc4e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc4e-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8cc4e-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8cc4e-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8cc4e-128">**LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8cc4e-128">**LVN\_SETDISPINFOW** (Unicode) and **LVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8cc4e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc4e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc4e-130">LVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="8cc4e-130">LVN\_GETDISPINFO</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





