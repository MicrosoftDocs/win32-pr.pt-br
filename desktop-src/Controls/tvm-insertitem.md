---
title: Mensagem de TVM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Controles de TVM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824266"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="ed3da-105">\_Mensagem TVM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="ed3da-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="ed3da-106">Insere um novo item em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="ed3da-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="ed3da-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="ed3da-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed3da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed3da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3da-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed3da-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ed3da-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ed3da-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ed3da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed3da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed3da-112">Ponteiro para uma estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica os atributos do item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="ed3da-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3da-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed3da-113">Return value</span></span>

<span data-ttu-id="ed3da-114">Retorna o identificador **HTREEITEM** para o novo item, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ed3da-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed3da-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed3da-115">Requirements</span></span>



| <span data-ttu-id="ed3da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed3da-116">Requirement</span></span> | <span data-ttu-id="ed3da-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed3da-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3da-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed3da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3da-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed3da-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed3da-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed3da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3da-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed3da-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed3da-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed3da-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed3da-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed3da-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ed3da-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ed3da-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ed3da-125">**TVM \_ INSERTITEMW** (Unicode) e **TVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ed3da-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ed3da-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed3da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3da-127">TVN \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="ed3da-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





