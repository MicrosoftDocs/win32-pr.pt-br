---
title: Mensagem de TVM_GETITEMSTATE (commctrl. h)
description: Recupera alguns ou todos os atributos de estado de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemState do TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Controles de TVM_GETITEMSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009548"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="85f51-105">\_Mensagem TVM GETitemstate</span><span class="sxs-lookup"><span data-stu-id="85f51-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="85f51-106">Recupera alguns ou todos os atributos de estado de um item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="85f51-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="85f51-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemState do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="85f51-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="85f51-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85f51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f51-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85f51-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85f51-110">Identificador para o item.</span><span class="sxs-lookup"><span data-stu-id="85f51-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="85f51-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85f51-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85f51-112">Máscara usada para especificar os Estados a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="85f51-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="85f51-113">É equivalente ao membro **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="85f51-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f51-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85f51-114">Return value</span></span>

<span data-ttu-id="85f51-115">Retorna um valor **uint** com os bits de estado apropriados definidos como **true**.</span><span class="sxs-lookup"><span data-stu-id="85f51-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="85f51-116">Somente os bits especificados por *lParam* e que são **true** serão definidos.</span><span class="sxs-lookup"><span data-stu-id="85f51-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="85f51-117">Esse valor é equivalente ao **estado** membro de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="85f51-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="85f51-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85f51-118">Requirements</span></span>



| <span data-ttu-id="85f51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f51-119">Requirement</span></span> | <span data-ttu-id="85f51-120">Valor</span><span class="sxs-lookup"><span data-stu-id="85f51-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85f51-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85f51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="85f51-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85f51-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85f51-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85f51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="85f51-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85f51-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85f51-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85f51-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f51-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f51-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





