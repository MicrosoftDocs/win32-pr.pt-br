---
title: Mensagem de LVM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertItem do ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Controles de LVM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753965"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="b8778-105">\_Mensagem INSERTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="b8778-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="b8778-106">Insere um novo item em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b8778-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="b8778-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="b8778-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8778-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8778-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8778-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8778-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8778-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8778-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8778-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8778-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8778-112">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica os atributos do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b8778-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="b8778-113">Use o membro **iItem** para especificar o índice de base zero no qual o novo item deve ser inserido.</span><span class="sxs-lookup"><span data-stu-id="b8778-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="b8778-114">Se esse valor for maior que o número de itens contidos atualmente por ListView, o novo item será anexado ao final da lista e atribuído ao índice correto.</span><span class="sxs-lookup"><span data-stu-id="b8778-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="b8778-115">Examine o valor de retorno da mensagem para determinar o índice real atribuído ao item.</span><span class="sxs-lookup"><span data-stu-id="b8778-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8778-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8778-116">Return value</span></span>

<span data-ttu-id="b8778-117">Retorna o índice do novo item se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8778-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8778-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8778-118">Remarks</span></span>

<span data-ttu-id="b8778-119">Você não pode usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou **LVM \_ InsertItem** para inserir subitens.</span><span class="sxs-lookup"><span data-stu-id="b8778-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="b8778-120">O membro **iSubItem** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8778-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="b8778-121">Consulte [**LVM \_ SETITEM**](lvm-setitem.md) para obter informações sobre como configurar subitens.</span><span class="sxs-lookup"><span data-stu-id="b8778-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="b8778-122">Se um controle de exibição de lista tiver o estilo de [**\_ caixas de \_ seleção LVS ex**](extended-list-view-styles.md) definido, qualquer valor colocado em bits 12 a 15 do membro de **estado** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) será ignorado.</span><span class="sxs-lookup"><span data-stu-id="b8778-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="b8778-123">Quando um item é adicionado com esse conjunto de estilos, ele sempre será definido como o estado desmarcado.</span><span class="sxs-lookup"><span data-stu-id="b8778-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="b8778-124">Se um controle de exibição de lista tiver o estilo de janela [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , uma mensagem do **LVM \_ INSERTITEM** falhará se você tentar inserir um item que tenha o do LPSTR \_ como o valor de seu membro **pszText** .</span><span class="sxs-lookup"><span data-stu-id="b8778-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="b8778-125">A mensagem **LVM \_ INSERTITEM** irá inserir o novo item na posição apropriada na ordem de classificação se as seguintes condições tiverem:</span><span class="sxs-lookup"><span data-stu-id="b8778-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="b8778-126">Você está usando um dos estilos LVS \_ SORTXXX.</span><span class="sxs-lookup"><span data-stu-id="b8778-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="b8778-127">Você não está usando o estilo [**LVS \_ OWNERDRAW**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b8778-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="b8778-128">O membro **pszText** da estrutura apontada por **pItem** não está definido como \_ monocallback de LPSTR.</span><span class="sxs-lookup"><span data-stu-id="b8778-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="b8778-129">Se a estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) não contiver LVIF \_ GroupId no membro **Mask** , o valor do membro **iGroupId** será \_ GROUPIDCALLBACK por padrão.</span><span class="sxs-lookup"><span data-stu-id="b8778-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8778-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8778-130">Requirements</span></span>



| <span data-ttu-id="b8778-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8778-131">Requirement</span></span> | <span data-ttu-id="b8778-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b8778-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8778-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8778-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b8778-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8778-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8778-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8778-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b8778-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8778-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8778-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8778-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8778-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8778-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b8778-139">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b8778-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8778-140">**LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8778-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





