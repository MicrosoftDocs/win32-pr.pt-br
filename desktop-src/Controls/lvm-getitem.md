---
title: Mensagem de LVM_GETITEM (commctrl. h)
description: Recupera alguns ou todos os atributos de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItem do ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Controles de LVM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645023"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="08e87-105">\_Mensagem GETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="08e87-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="08e87-106">Recupera alguns ou todos os atributos de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="08e87-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="08e87-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="08e87-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="08e87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08e87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08e87-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="08e87-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="08e87-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="08e87-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08e87-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08e87-112">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica as informações para recuperar e receber informações sobre o item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="08e87-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e87-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08e87-113">Return value</span></span>

<span data-ttu-id="08e87-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="08e87-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e87-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="08e87-115">Remarks</span></span>

<span data-ttu-id="08e87-116">Quando a **mensagem LVM \_ GETITEM** é enviada, os membros **iItem** e **iSubItem** identificam o item ou subitem para recuperar informações e o membro **Mask** especifica quais atributos serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="08e87-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="08e87-117">Para obter uma lista de valores possíveis, consulte a descrição da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="08e87-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="08e87-118">Se o \_ sinalizador de texto LVIF for definido no membro **Mask** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , o membro **pszText** deverá apontar para um buffer válido e o membro **cchTextMax** deverá ser definido como o número de caracteres nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="08e87-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="08e87-119">Os aplicativos não devem pressupor que o texto será necessariamente colocado no buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="08e87-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="08e87-120">O controle pode, em vez disso, alterar o membro **pszText** da estrutura para apontar para o novo texto, em vez de colocá-lo no buffer.</span><span class="sxs-lookup"><span data-stu-id="08e87-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="08e87-121">Se o membro da **máscara** especificar o \_ valor do estado LVIF, o membro **stateMask** deverá especificar os bits de estado do item a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="08e87-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="08e87-122">Na saída, o membro de **estado** contém os valores dos bits de estado especificados.</span><span class="sxs-lookup"><span data-stu-id="08e87-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e87-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08e87-123">Requirements</span></span>



| <span data-ttu-id="08e87-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08e87-124">Requirement</span></span> | <span data-ttu-id="08e87-125">Valor</span><span class="sxs-lookup"><span data-stu-id="08e87-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08e87-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08e87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08e87-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08e87-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08e87-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08e87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08e87-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08e87-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08e87-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08e87-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="08e87-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08e87-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="08e87-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="08e87-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="08e87-133">**LVM \_ GETITEMW** (Unicode) e **LVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="08e87-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





