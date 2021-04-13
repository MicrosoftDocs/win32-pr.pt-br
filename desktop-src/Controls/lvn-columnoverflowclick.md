---
title: LVN_COLUMNOVERFLOWCLICK código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o botão de estouro é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456055"
---
# <a name="lvn_columnoverflowclick-notification-code"></a><span data-ttu-id="1ed83-105">Código de notificação do LVN \_ COLUMNOVERFLOWCLICK</span><span class="sxs-lookup"><span data-stu-id="1ed83-105">LVN\_COLUMNOVERFLOWCLICK notification code</span></span>

<span data-ttu-id="1ed83-106">Enviado por um controle de exibição de lista quando o botão de estouro é clicado.</span><span class="sxs-lookup"><span data-stu-id="1ed83-106">Sent by a list-view control when its overflow button is clicked.</span></span> <span data-ttu-id="1ed83-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ed83-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1ed83-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed83-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ed83-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed83-110">Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que descreve o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ed83-110">Pointer to a [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that describes the notification code.</span></span> <span data-ttu-id="1ed83-111">O chamador é responsável por alocar essa estrutura, incluindo a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida.</span><span class="sxs-lookup"><span data-stu-id="1ed83-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="1ed83-112">Defina os membros da estrutura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="1ed83-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="1ed83-113">O membro do **código** deve ser definido como LVN \_ COLUMNOVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="1ed83-113">The **code** member must be set to LVN\_COLUMNOVERFLOWCLICK.</span></span>

<span data-ttu-id="1ed83-114">Defina o membro **iItem** da estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) como-1.</span><span class="sxs-lookup"><span data-stu-id="1ed83-114">Set the **iItem** member of the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure to -1.</span></span> <span data-ttu-id="1ed83-115">Defina o membro **iSubItem** para o índice do subitem.</span><span class="sxs-lookup"><span data-stu-id="1ed83-115">Set the **iSubItem** member to the index of the subitem.</span></span> <span data-ttu-id="1ed83-116">Defina os membros **uNewState**, **uOldState** e **lParam** como zero.</span><span class="sxs-lookup"><span data-stu-id="1ed83-116">Set the **uNewState**, **uOldState**, and **lParam** members to zero.</span></span> <span data-ttu-id="1ed83-117">Os membros restantes da estrutura **NMLISTVEIW** não são usados.</span><span class="sxs-lookup"><span data-stu-id="1ed83-117">The remaining members of the **NMLISTVIEW** structure are not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed83-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ed83-118">Return value</span></span>

<span data-ttu-id="1ed83-119">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1ed83-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed83-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ed83-120">Remarks</span></span>

<span data-ttu-id="1ed83-121">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="1ed83-121">The notification receiver casts *lParam* to retrieve the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="1ed83-122">O parâmetro *wParam* contém a ID do controle que envia o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ed83-122">The *wParam* parameter contains the ID of the control that sends the notification code.</span></span>

<span data-ttu-id="1ed83-123">Se um controle de cabeçalho for um filho de ListView, o controle de cabeçalho deverá enviar esse código de notificação ao controle ListView quando o controle de cabeçalho receber o código de notificação [HDN \_ OVERFLOWCLICK](hdn-overflowclick.md) .</span><span class="sxs-lookup"><span data-stu-id="1ed83-123">If a header control is a child of the listview, the header control should send this notification code to the listview control when the header control receives the [HDN\_OVERFLOWCLICK](hdn-overflowclick.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed83-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed83-124">Requirements</span></span>



| <span data-ttu-id="1ed83-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed83-125">Requirement</span></span> | <span data-ttu-id="1ed83-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed83-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed83-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed83-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed83-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ed83-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ed83-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed83-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed83-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ed83-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ed83-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ed83-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed83-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed83-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





