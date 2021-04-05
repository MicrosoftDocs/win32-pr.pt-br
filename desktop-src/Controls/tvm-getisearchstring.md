---
title: Mensagem de TVM_GETISEARCHSTRING (commctrl. h)
description: Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Controles de TVM_GETISEARCHSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086315"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="baf33-104">\_Mensagem TVM GETISEARCHSTRING</span><span class="sxs-lookup"><span data-stu-id="baf33-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="baf33-105">Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="baf33-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="baf33-106">O controle de exibição de árvore usa a cadeia de caracteres de pesquisa incremental para selecionar um item com base em caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="baf33-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="baf33-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="baf33-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="baf33-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baf33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="baf33-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="baf33-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="baf33-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="baf33-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baf33-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baf33-112">Ponteiro para o buffer que recebe a cadeia de caracteres de pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="baf33-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf33-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baf33-113">Return value</span></span>

<span data-ttu-id="baf33-114">Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="baf33-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="baf33-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="baf33-115">Remarks</span></span>

<span data-ttu-id="baf33-116">**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="baf33-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="baf33-117">Você deve alocar um buffer grande o suficiente para manter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="baf33-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="baf33-118">Primeiro, chame a mensagem transmitindo **NULL** em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="baf33-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="baf33-119">Isso retorna o número de caracteres, excluindo **NULL**, que são necessários.</span><span class="sxs-lookup"><span data-stu-id="baf33-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="baf33-120">Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="baf33-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="baf33-121">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="baf33-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="baf33-122">Se o controle de exibição de árvore não estiver no modo de pesquisa incremental, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="baf33-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf33-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baf33-123">Requirements</span></span>



| <span data-ttu-id="baf33-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="baf33-124">Requirement</span></span> | <span data-ttu-id="baf33-125">Valor</span><span class="sxs-lookup"><span data-stu-id="baf33-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baf33-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baf33-126">Minimum supported client</span></span><br/> | <span data-ttu-id="baf33-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baf33-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baf33-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baf33-128">Minimum supported server</span></span><br/> | <span data-ttu-id="baf33-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="baf33-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baf33-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baf33-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="baf33-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="baf33-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="baf33-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="baf33-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="baf33-133">**TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="baf33-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





