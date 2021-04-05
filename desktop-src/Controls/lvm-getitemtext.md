---
title: Mensagem de LVM_GETITEMTEXT (commctrl. h)
description: Recupera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemText do ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Controles de LVM_GETITEMTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086163"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="479f9-105">\_Mensagem GETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="479f9-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="479f9-106">Recupera o texto de um item de exibição de lista ou subitem.</span><span class="sxs-lookup"><span data-stu-id="479f9-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="479f9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="479f9-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="479f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="479f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="479f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="479f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="479f9-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="479f9-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="479f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="479f9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="479f9-112">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="479f9-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="479f9-113">Para recuperar o texto do item, defina **iSubItem** como zero.</span><span class="sxs-lookup"><span data-stu-id="479f9-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="479f9-114">Para recuperar o texto de um subitem, defina **iSubItem** como o índice do subitem.</span><span class="sxs-lookup"><span data-stu-id="479f9-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="479f9-115">O membro **pszText** aponta para um buffer que recebe o texto.</span><span class="sxs-lookup"><span data-stu-id="479f9-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="479f9-116">O membro **cchTextMax** especifica o número de caracteres no buffer.</span><span class="sxs-lookup"><span data-stu-id="479f9-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="479f9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="479f9-117">Return value</span></span>

<span data-ttu-id="479f9-118">Se você enviar essa mensagem explicitamente, ela retornará o número de caracteres no membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="479f9-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="479f9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="479f9-119">Remarks</span></span>

<span data-ttu-id="479f9-120">Você também pode enviar essa mensagem chamando a macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="479f9-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="479f9-121">No entanto, essa macro não retorna o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="479f9-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="479f9-122">**LVM \_** Não há suporte para GETITEMTEXT no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="479f9-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="479f9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="479f9-123">Requirements</span></span>



| <span data-ttu-id="479f9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="479f9-124">Requirement</span></span> | <span data-ttu-id="479f9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="479f9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="479f9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="479f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="479f9-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="479f9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="479f9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="479f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="479f9-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="479f9-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="479f9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="479f9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="479f9-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="479f9-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="479f9-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="479f9-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="479f9-133">**LVM \_ GETITEMTEXTW** (Unicode) e **LVM \_ GETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="479f9-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





