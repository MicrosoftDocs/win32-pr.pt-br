---
title: Mensagem de TVM_GETCOUNT (commctrl. h)
description: Recupera uma contagem dos itens em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCount de TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Controles de TVM_GETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455734"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="0210d-105">\_Mensagem de GETCOUNT TVM</span><span class="sxs-lookup"><span data-stu-id="0210d-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="0210d-106">Recupera uma contagem dos itens em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="0210d-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="0210d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .</span><span class="sxs-lookup"><span data-stu-id="0210d-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0210d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0210d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0210d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0210d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0210d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0210d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0210d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0210d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0210d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0210d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0210d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0210d-113">Return value</span></span>

<span data-ttu-id="0210d-114">Retorna a contagem de itens.</span><span class="sxs-lookup"><span data-stu-id="0210d-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="0210d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0210d-115">Remarks</span></span>

<span data-ttu-id="0210d-116">A contagem de nós retornada por [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) é limitada a valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="0210d-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="0210d-117">Se você adicionar um nó além de 32767, a macro retornará um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="0210d-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="0210d-118">Depois de adicionar nós 65536, a contagem retorna para zero.</span><span class="sxs-lookup"><span data-stu-id="0210d-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="0210d-119">Quando isso ocorre, o controle de exibição de árvore aparece vazio sem barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0210d-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="0210d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0210d-120">Requirements</span></span>



| <span data-ttu-id="0210d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0210d-121">Requirement</span></span> | <span data-ttu-id="0210d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0210d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0210d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0210d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0210d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0210d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0210d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0210d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0210d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0210d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0210d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0210d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0210d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0210d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





