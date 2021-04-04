---
title: Mensagem de LVM_SETITEMTEXT (commctrl. h)
description: Altera o texto de um item de exibição de lista ou subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemText do ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Controles de LVM_SETITEMTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824454"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="40d0a-105">\_Mensagem SETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="40d0a-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="40d0a-106">Altera o texto de um item de exibição de lista ou subitem.</span><span class="sxs-lookup"><span data-stu-id="40d0a-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="40d0a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .</span><span class="sxs-lookup"><span data-stu-id="40d0a-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="40d0a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40d0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40d0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40d0a-110">Índice de base zero do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="40d0a-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="40d0a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40d0a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40d0a-112">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="40d0a-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="40d0a-113">O membro **iSubItem** é o índice do subitem ou pode ser zero para definir o rótulo do item.</span><span class="sxs-lookup"><span data-stu-id="40d0a-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="40d0a-114">O membro **pszText** é o endereço de uma cadeia de caracteres terminada em nulo que contém o novo texto; Ele também pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="40d0a-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="40d0a-115">O membro **pszText** também pode ser LPSTR \_ textcallback para indicar um item de retorno de chamada para o qual a janela pai armazena o texto.</span><span class="sxs-lookup"><span data-stu-id="40d0a-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="40d0a-116">Nesse caso, o controle List-View envia ao pai um código de notificação [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) quando ele precisa do texto.</span><span class="sxs-lookup"><span data-stu-id="40d0a-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d0a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40d0a-117">Return value</span></span>

<span data-ttu-id="40d0a-118">Se você enviar essa mensagem explicitamente, ela retornará **true** se for bem-sucedida ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="40d0a-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40d0a-119">Requirements</span></span>



| <span data-ttu-id="40d0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d0a-120">Requirement</span></span> | <span data-ttu-id="40d0a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="40d0a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40d0a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40d0a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40d0a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40d0a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40d0a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40d0a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40d0a-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="40d0a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40d0a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40d0a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d0a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d0a-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="40d0a-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="40d0a-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="40d0a-129">**LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="40d0a-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





