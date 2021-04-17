---
title: LVN_ENDLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754375"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="4f736-105">Código de notificação do LVN \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="4f736-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="4f736-106">Notifica uma janela pai do controle de exibição de lista sobre o fim da edição de rótulo para um item.</span><span class="sxs-lookup"><span data-stu-id="4f736-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="4f736-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4f736-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4f736-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f736-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f736-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f736-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f736-110">Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="4f736-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="4f736-111">O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item que está sendo editado.</span><span class="sxs-lookup"><span data-stu-id="4f736-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="4f736-112">O membro **pszText** do **Item** contém um valor válido quando o \_ código de notificação ENDLABELEDIT de LVN é enviado, independentemente de o \_ sinalizador de texto LVIF ser definido no membro **Mask** da estrutura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="4f736-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="4f736-113">Se o usuário cancelar a edição, o membro **pszText** da estrutura **LVITEM** será **nulo**; caso contrário, **pszText** será o endereço do texto editado.</span><span class="sxs-lookup"><span data-stu-id="4f736-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f736-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f736-114">Return value</span></span>

<span data-ttu-id="4f736-115">Se o membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) for não **nulo**, retornará **true** para definir o rótulo do item como o texto editado.</span><span class="sxs-lookup"><span data-stu-id="4f736-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="4f736-116">Retorne **false** para rejeitar o texto editado e reverter para o rótulo original.</span><span class="sxs-lookup"><span data-stu-id="4f736-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="4f736-117">Se o membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) for **nulo**, o valor de retorno será ignorado.</span><span class="sxs-lookup"><span data-stu-id="4f736-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f736-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f736-118">Remarks</span></span>

<span data-ttu-id="4f736-119">O valor de retorno do procedimento da caixa de diálogo é se a mensagem foi tratada.</span><span class="sxs-lookup"><span data-stu-id="4f736-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="4f736-120">O segundo valor de retorno deve ser definido chamando [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) com **DWLP_MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f736-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="4f736-121">Quando o usuário começa a editar um rótulo de item, a janela pai do controle List-View recebe um código de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="4f736-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="4f736-122">Quando o usuário cancela ou conclui a edição, a janela pai recebe um \_ código de notificação LVN ENDLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="4f736-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f736-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f736-123">Requirements</span></span>



| <span data-ttu-id="4f736-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f736-124">Requirement</span></span> | <span data-ttu-id="4f736-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4f736-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f736-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f736-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4f736-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f736-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f736-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f736-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4f736-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f736-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f736-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f736-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f736-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f736-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4f736-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4f736-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f736-133">**LVN \_ ENDLABELEDITW** (Unicode) e **LVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f736-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





