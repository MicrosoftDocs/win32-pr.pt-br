---
title: LVN_COLUMNDROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o botão suspenso da exibição de lista é pressionado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- LVN_COLUMNDROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499378"
---
# <a name="lvn_columndropdown-notification-code"></a><span data-ttu-id="12806-105">Código de notificação do LVN \_ COLUMNDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="12806-105">LVN\_COLUMNDROPDOWN notification code</span></span>

<span data-ttu-id="12806-106">Enviado por um controle de exibição de lista quando o botão suspenso da exibição de lista é pressionado.</span><span class="sxs-lookup"><span data-stu-id="12806-106">Sent by a list-view control when the list-view's drop-down button is pressed.</span></span> <span data-ttu-id="12806-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="12806-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="12806-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12806-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12806-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12806-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12806-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que descreve o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="12806-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="12806-111">O chamador é responsável por alocar essa estrutura, incluindo a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida.</span><span class="sxs-lookup"><span data-stu-id="12806-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="12806-112">Defina os membros da estrutura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="12806-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="12806-113">O membro do **código** deve ser definido como LVN \_ COLUMNDROPDOWN.</span><span class="sxs-lookup"><span data-stu-id="12806-113">The **code** member must be set to LVN\_COLUMNDROPDOWN.</span></span>

<span data-ttu-id="12806-114">Defina o membro **iItem** da estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) como-1.</span><span class="sxs-lookup"><span data-stu-id="12806-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="12806-115">Defina o membro **iSubItem** para o índice do subitem.</span><span class="sxs-lookup"><span data-stu-id="12806-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="12806-116">Defina os membros **uNewState**, **uOldState** e **lParam** como zero.</span><span class="sxs-lookup"><span data-stu-id="12806-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="12806-117">Os membros restantes da estrutura **NMLISTVEIW** não são usados.</span><span class="sxs-lookup"><span data-stu-id="12806-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12806-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12806-118">Return value</span></span>

<span data-ttu-id="12806-119">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="12806-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12806-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="12806-120">Remarks</span></span>

<span data-ttu-id="12806-121">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="12806-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="12806-122">O parâmetro *wParam* contém a ID do controle que envia o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="12806-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="12806-123">Se um controle de cabeçalho for um filho do modo de exibição de lista, o controle de cabeçalho deverá enviar esse código notificações para o controle de exibição de lista quando o controle de cabeçalho receber o código de notificação [ \_ DROPDOWN HDN](hdn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="12806-123">If a header control is a child of the list-view, the header control should send this notidication code to the list-view control when the header control receives the [HDN\_DROPDOWN](hdn-dropdown.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12806-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12806-124">Requirements</span></span>



| <span data-ttu-id="12806-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12806-125">Requirement</span></span> | <span data-ttu-id="12806-126">Valor</span><span class="sxs-lookup"><span data-stu-id="12806-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12806-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12806-127">Minimum supported client</span></span><br/> | <span data-ttu-id="12806-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12806-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12806-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12806-129">Minimum supported server</span></span><br/> | <span data-ttu-id="12806-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12806-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12806-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12806-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="12806-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12806-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





