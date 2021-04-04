---
title: TVN_ENDLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore sobre o fim da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085629"
---
# <a name="tvn_endlabeledit-notification-code"></a><span data-ttu-id="974d8-105">Código de notificação do TVN \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="974d8-105">TVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="974d8-106">Notifica uma janela pai do controle de exibição de árvore sobre o fim da edição de rótulo para um item.</span><span class="sxs-lookup"><span data-stu-id="974d8-106">Notifies a tree-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="974d8-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="974d8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="974d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="974d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="974d8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="974d8-110">Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="974d8-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="974d8-111">O membro **Item** dessa estrutura é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **hItem**, **lParam** e **pszText** contêm informações válidas sobre o item que foi editado.</span><span class="sxs-lookup"><span data-stu-id="974d8-111">The **item** member of this structure is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem**, **lParam**, and **pszText** members contain valid information about the item that was edited.</span></span> <span data-ttu-id="974d8-112">Se a edição do rótulo foi cancelada, o membro **pszText** da estrutura **TVITEM** é **nulo**; caso contrário, **pszText** será o endereço do texto editado.</span><span class="sxs-lookup"><span data-stu-id="974d8-112">If label editing was canceled, the **pszText** member of the **TVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974d8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="974d8-113">Return value</span></span>

<span data-ttu-id="974d8-114">Se o membro **pszText** for não **nulo**, retornará **true** para definir o rótulo do item como o texto editado.</span><span class="sxs-lookup"><span data-stu-id="974d8-114">If the **pszText** member is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="974d8-115">Retorne **false** para rejeitar o texto editado e reverter para o rótulo original.</span><span class="sxs-lookup"><span data-stu-id="974d8-115">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

## <a name="remarks"></a><span data-ttu-id="974d8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="974d8-116">Remarks</span></span>

<span data-ttu-id="974d8-117">Se o membro **pszText** for **nulo**, o valor de retorno será ignorado.</span><span class="sxs-lookup"><span data-stu-id="974d8-117">If the **pszText** member is **NULL**, the return value is ignored.</span></span>

<span data-ttu-id="974d8-118">Se você especificou o \_ valor de **pszText** de texto de LPSTR para este item e o membro de messagecast não for **nulo**, o \_ manipulador de ENDLABELEDIT TVN deverá copiar o texto de **pszText** para o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="974d8-118">If you specified the LPSTR\_TEXTCALLBACK value for this item and the **pszText** member is non-**NULL**, your TVN\_ENDLABELEDIT handler should copy the text from **pszText** to your local storage.</span></span>

## <a name="requirements"></a><span data-ttu-id="974d8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="974d8-119">Requirements</span></span>



| <span data-ttu-id="974d8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="974d8-120">Requirement</span></span> | <span data-ttu-id="974d8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="974d8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="974d8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="974d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="974d8-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="974d8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="974d8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="974d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="974d8-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="974d8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="974d8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="974d8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="974d8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="974d8-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="974d8-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="974d8-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="974d8-129">**TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="974d8-129">**TVN\_ENDLABELEDITW** (Unicode) and **TVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 





