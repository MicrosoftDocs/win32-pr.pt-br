---
title: TVN_GETDISPINFO código de notificação (commctrl. h)
description: Solicita que uma janela pai do controle de exibição de árvore forneça as informações necessárias para exibir ou classificar um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499391"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="d8255-105">Código de notificação do TVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d8255-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="d8255-106">Solicita que uma janela pai do controle de exibição de árvore forneça as informações necessárias para exibir ou classificar um item.</span><span class="sxs-lookup"><span data-stu-id="d8255-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="d8255-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8255-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d8255-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8255-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8255-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8255-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8255-110">Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d8255-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="d8255-111">O **membro item** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos membros **Mask**, **hItem**, **State** e **lParam** especificam o tipo de informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="d8255-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="d8255-112">Você deve preencher os membros da estrutura com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d8255-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8255-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8255-113">Return value</span></span>

<span data-ttu-id="d8255-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="d8255-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8255-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8255-115">Remarks</span></span>

<span data-ttu-id="d8255-116">Esse código de notificação é enviado sob as seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="d8255-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="d8255-117">Se o membro **pszText** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor de \_ textcallback de LPStr, o controle enviará esse código de notificação para recuperar o texto do item.</span><span class="sxs-lookup"><span data-stu-id="d8255-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="d8255-118">Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador de texto TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="d8255-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="d8255-119">Se o membro **iImage** ou **ISelectedImage** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ IMAGECALLBACK, o controle enviará esse código de notificação para recuperar o índice dos ícones de um item na lista de imagens do controle.</span><span class="sxs-lookup"><span data-stu-id="d8255-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="d8255-120">Nesse caso, se o item for selecionado, o membro **Mask** de *lParam* terá o \_ sinalizador de SELECTEDIMAGE TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="d8255-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="d8255-121">Se o item não estiver selecionado, o membro **Mask** de *lParam* terá o sinalizador de \_ imagem TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="d8255-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="d8255-122">Se o membro **cChildren** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item for o valor I \_ CHILDRENCALLBACK, o controle enviará esse código de notificação para recuperar um valor que indica se o item tem itens filho.</span><span class="sxs-lookup"><span data-stu-id="d8255-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="d8255-123">Nesse caso, o membro **Mask** de *lParam* terá o \_ sinalizador filhos TVIF definido.</span><span class="sxs-lookup"><span data-stu-id="d8255-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8255-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8255-124">Requirements</span></span>



| <span data-ttu-id="d8255-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8255-125">Requirement</span></span> | <span data-ttu-id="d8255-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d8255-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8255-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8255-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d8255-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8255-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8255-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8255-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d8255-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8255-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8255-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8255-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8255-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8255-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d8255-133">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d8255-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d8255-134">**TVN \_ GETDISPINFOW** (Unicode) e **TVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d8255-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d8255-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8255-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8255-136">TVN \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="d8255-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 





