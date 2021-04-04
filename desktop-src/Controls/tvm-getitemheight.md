---
title: Mensagem de TVM_GETITEMHEIGHT (commctrl. h)
description: Recupera a altura atual de cada item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItemHeight.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Controles de TVM_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824839"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="33c38-105">\_Mensagem TVM GETITEMHEIGHT</span><span class="sxs-lookup"><span data-stu-id="33c38-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="33c38-106">Recupera a altura atual de cada item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="33c38-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="33c38-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .</span><span class="sxs-lookup"><span data-stu-id="33c38-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33c38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c38-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33c38-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33c38-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="33c38-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33c38-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33c38-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="33c38-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="33c38-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c38-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33c38-113">Return value</span></span>

<span data-ttu-id="33c38-114">Retorna a altura de cada item, em pixels.</span><span class="sxs-lookup"><span data-stu-id="33c38-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c38-115">Requirements</span></span>



| <span data-ttu-id="33c38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c38-116">Requirement</span></span> | <span data-ttu-id="33c38-117">Valor</span><span class="sxs-lookup"><span data-stu-id="33c38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33c38-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33c38-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33c38-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33c38-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33c38-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33c38-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33c38-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33c38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c38-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c38-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c38-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="33c38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c38-125">**TVM \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="33c38-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





