---
title: TVN_SETDISPINFO código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que ele deve atualizar as informações que ele mantém sobre um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756230"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="8fdb4-105">Código de notificação do TVN \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="8fdb4-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="8fdb4-106">Notifica uma janela pai do controle de exibição de árvore que ele deve atualizar as informações que ele mantém sobre um item.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="8fdb4-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8fdb4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="8fdb4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fdb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fdb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fdb4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fdb4-110">Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) que descreve o item que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="8fdb4-111">O membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica o item que está sendo atualizado e o membro **Mask** especifica quais atributos do item estão sendo atualizados.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fdb4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fdb4-112">Return value</span></span>

<span data-ttu-id="8fdb4-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fdb4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fdb4-114">Remarks</span></span>

<span data-ttu-id="8fdb4-115">Se o membro **pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor de \_ textcallback de LPStr, o controle enviará essa notificação para definir o texto do item.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="8fdb4-116">Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador de texto TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="8fdb4-117">Se o membro **iImage** ou **ISelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ IMAGECALLBACK, o controle enviará essa notificação para recuperar o índice da imagem de ícone a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="8fdb4-118">Nesse caso, o membro **Mask** de *lParam* terá a \_ imagem TVIF ou o sinalizador de \_ SELECTEDIMAGE TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="8fdb4-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fdb4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fdb4-119">Requirements</span></span>



| <span data-ttu-id="8fdb4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fdb4-120">Requirement</span></span> | <span data-ttu-id="8fdb4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8fdb4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fdb4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8fdb4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fdb4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fdb4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8fdb4-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fdb4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fdb4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fdb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fdb4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fdb4-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8fdb4-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8fdb4-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8fdb4-129">**TVN \_ SETDISPINFOW** (Unicode) e **TVN \_ SETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8fdb4-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8fdb4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fdb4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fdb4-131">**TVITEM**</span><span class="sxs-lookup"><span data-stu-id="8fdb4-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="8fdb4-132">**TVITEMEX**</span><span class="sxs-lookup"><span data-stu-id="8fdb4-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="8fdb4-133">TVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="8fdb4-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 





