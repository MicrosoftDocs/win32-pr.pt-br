---
title: Mensagem de TVM_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador para um item de exibição de árvore e indica se o item está visível. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItemRect.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Controles de TVM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085454"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="94cad-105">\_Mensagem TVM GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="94cad-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="94cad-106">Recupera o retângulo delimitador para um item de exibição de árvore e indica se o item está visível.</span><span class="sxs-lookup"><span data-stu-id="94cad-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="94cad-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="94cad-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="94cad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94cad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94cad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94cad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94cad-110">Valor que especifica a parte do item para o qual recuperar o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="94cad-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="94cad-111">Se esse parâmetro for **true**, o retângulo delimitador incluirá apenas o texto do item.</span><span class="sxs-lookup"><span data-stu-id="94cad-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="94cad-112">Caso contrário, inclui a linha inteira que o item ocupa no controle de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="94cad-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="94cad-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94cad-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94cad-114">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que, ao enviar a mensagem, contém o identificador do item para o qual recuperar o retângulo.</span><span class="sxs-lookup"><span data-stu-id="94cad-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="94cad-115">Consulte o exemplo abaixo para obter mais informações sobre como posicionar o identificador de item nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="94cad-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="94cad-116">Depois de retornar da mensagem, esse parâmetro contém o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="94cad-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="94cad-117">As coordenadas são relativas ao canto superior esquerdo do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="94cad-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94cad-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94cad-118">Return value</span></span>

<span data-ttu-id="94cad-119">Se o item estiver visível e o retângulo delimitador for recuperado com êxito, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="94cad-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="94cad-120">Caso contrário, a mensagem retornará **false** e não recuperará o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="94cad-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="94cad-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="94cad-121">Remarks</span></span>

<span data-ttu-id="94cad-122">Ao enviar essa mensagem, o parâmetro *lParam* contém o identificador do item para o qual o retângulo está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="94cad-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="94cad-123">O identificador é colocado em *lParam* , conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="94cad-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="94cad-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94cad-124">Requirements</span></span>



| <span data-ttu-id="94cad-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="94cad-125">Requirement</span></span> | <span data-ttu-id="94cad-126">Valor</span><span class="sxs-lookup"><span data-stu-id="94cad-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94cad-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94cad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="94cad-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94cad-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94cad-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94cad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="94cad-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94cad-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94cad-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94cad-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="94cad-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94cad-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

