---
title: Mensagem de TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetVisibleCount.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Controles de TVM_GETVISIBLECOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918160"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="393ff-105">\_Mensagem TVM GETVISIBLECOUNT</span><span class="sxs-lookup"><span data-stu-id="393ff-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="393ff-106">Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="393ff-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="393ff-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .</span><span class="sxs-lookup"><span data-stu-id="393ff-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="393ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="393ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="393ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="393ff-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="393ff-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="393ff-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="393ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="393ff-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="393ff-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="393ff-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="393ff-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="393ff-113">Return value</span></span>

<span data-ttu-id="393ff-114">Retorna o número de itens que podem ser totalmente visíveis na janela do cliente do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="393ff-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="393ff-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="393ff-115">Remarks</span></span>

<span data-ttu-id="393ff-116">O número de itens que podem ser totalmente visíveis pode ser maior que o número de itens no controle.</span><span class="sxs-lookup"><span data-stu-id="393ff-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="393ff-117">O controle calcula esse valor dividindo a altura da janela do cliente pela altura de um item.</span><span class="sxs-lookup"><span data-stu-id="393ff-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="393ff-118">Observe que o valor de retorno é o número de itens que podem estar *totalmente* visíveis.</span><span class="sxs-lookup"><span data-stu-id="393ff-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="393ff-119">Se você puder ver todos os 20 itens e parte de um item mais, o valor de retorno será 20.</span><span class="sxs-lookup"><span data-stu-id="393ff-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="393ff-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="393ff-120">Requirements</span></span>



| <span data-ttu-id="393ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="393ff-121">Requirement</span></span> | <span data-ttu-id="393ff-122">Valor</span><span class="sxs-lookup"><span data-stu-id="393ff-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="393ff-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="393ff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="393ff-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="393ff-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="393ff-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="393ff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="393ff-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="393ff-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="393ff-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="393ff-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="393ff-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="393ff-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





