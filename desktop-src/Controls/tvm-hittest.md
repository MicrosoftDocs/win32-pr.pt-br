---
title: Mensagem de TVM_HITTEST (commctrl. h)
description: Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro HitTest do TreeView.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Controles de TVM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009108"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="5fd0f-105">\_Mensagem TVM HITTEST</span><span class="sxs-lookup"><span data-stu-id="5fd0f-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="5fd0f-106">Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="5fd0f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ HitTest do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="5fd0f-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fd0f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fd0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fd0f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5fd0f-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5fd0f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fd0f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd0f-112">Ponteiro para uma estrutura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="5fd0f-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="5fd0f-113">Quando a mensagem é enviada, o membro **pt** especifica as coordenadas do ponto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="5fd0f-114">Quando a mensagem retornar, o membro **hItem** será o identificador para o item no ponto especificado ou **NULL** se nenhum item ocupar o ponto.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="5fd0f-115">Além disso, quando a mensagem retorna, o membro **flags** é um valor de teste de clique que indica o local do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="5fd0f-116">Para obter uma lista de valores de teste de clique, consulte a descrição da estrutura **TVHITTESTINFO** .</span><span class="sxs-lookup"><span data-stu-id="5fd0f-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd0f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fd0f-117">Return value</span></span>

<span data-ttu-id="5fd0f-118">Retorna o identificador para o item de exibição de árvore que ocupa o ponto especificado ou **nulo** se nenhum item ocupar o ponto.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd0f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fd0f-119">Requirements</span></span>



| <span data-ttu-id="5fd0f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd0f-120">Requirement</span></span> | <span data-ttu-id="5fd0f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd0f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd0f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd0f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fd0f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fd0f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd0f-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fd0f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fd0f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fd0f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd0f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd0f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





