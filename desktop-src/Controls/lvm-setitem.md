---
title: Mensagem de LVM_SETITEM (commctrl. h)
description: Define alguns ou todos os atributos de um item de exibição de lista. Você também pode enviar \_ o LVM SETITEM para definir o texto de um subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItem do ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Controles de LVM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009131"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="b8be2-106">\_Mensagem SETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="b8be2-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="b8be2-107">Define alguns ou todos os atributos de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b8be2-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="b8be2-108">Você também pode enviar \_ o LVM SETITEM para definir o texto de um subitem.</span><span class="sxs-lookup"><span data-stu-id="b8be2-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="b8be2-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="b8be2-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8be2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8be2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8be2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8be2-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8be2-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8be2-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8be2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8be2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8be2-114">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contém os novos atributos de item.</span><span class="sxs-lookup"><span data-stu-id="b8be2-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="b8be2-115">Os membros **iItem** e **iSubItem** identificam o item ou subitem, e o membro **Mask** especifica quais atributos definir.</span><span class="sxs-lookup"><span data-stu-id="b8be2-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="b8be2-116">Se o membro de **máscara** especificar o \_ valor de texto LVIF, o membro **pszText** será o endereço de uma cadeia de caracteres terminada em nulo e o membro **cchTextMax** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="b8be2-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="b8be2-117">Se o membro de **máscara** especificar o \_ valor de estado LVIF, o membro **stateMask** especificará quais Estados de item alterar e o membro de **estado** conterá os valores para esses Estados.</span><span class="sxs-lookup"><span data-stu-id="b8be2-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8be2-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8be2-118">Return value</span></span>

<span data-ttu-id="b8be2-119">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8be2-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8be2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8be2-120">Remarks</span></span>

<span data-ttu-id="b8be2-121">Para definir os atributos de um item de exibição de lista, defina o membro **iItem** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) para o índice do item e defina o membro **iSubItem** como zero.</span><span class="sxs-lookup"><span data-stu-id="b8be2-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="b8be2-122">Para um item, você pode definir os membros **State**, **pszText**, **iImage** e **lParam** da estrutura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="b8be2-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="b8be2-123">Para definir o texto de um subitem, defina os membros **iItem** e **iSubItem** para indicar o subitem específico e use o membro **pszText** para especificar o texto.</span><span class="sxs-lookup"><span data-stu-id="b8be2-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="b8be2-124">Como alternativa, você pode usar a [**macro \_ SetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) para definir o texto de um subitem.</span><span class="sxs-lookup"><span data-stu-id="b8be2-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="b8be2-125">Você não pode definir os membros de **estado** ou **lParam** para subitens porque os subitens não têm esses atributos.</span><span class="sxs-lookup"><span data-stu-id="b8be2-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="b8be2-126">Na versão 4,70 e posterior, você pode definir o membro **iImage** para subitens.</span><span class="sxs-lookup"><span data-stu-id="b8be2-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="b8be2-127">A imagem do subitem será exibida se o controle de exibição de lista tiver o estilo estendido [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b8be2-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="b8be2-128">As versões anteriores irão ignorar a imagem do subitem.</span><span class="sxs-lookup"><span data-stu-id="b8be2-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8be2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8be2-129">Requirements</span></span>



| <span data-ttu-id="b8be2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8be2-130">Requirement</span></span> | <span data-ttu-id="b8be2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b8be2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8be2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8be2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b8be2-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8be2-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8be2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8be2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b8be2-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8be2-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8be2-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8be2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8be2-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8be2-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b8be2-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b8be2-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8be2-139">**LVM \_ SETITEMW** (Unicode) e **LVM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8be2-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





