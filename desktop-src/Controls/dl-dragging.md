---
title: DL_DRAGGING código de notificação (commctrl. h)
description: Sinaliza que o usuário moveu o mouse ao arrastar um item.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499870"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="1571b-104">Código de notificação de arrastar para DL \_</span><span class="sxs-lookup"><span data-stu-id="1571b-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="1571b-105">Sinaliza que o usuário moveu o mouse ao arrastar um item.</span><span class="sxs-lookup"><span data-stu-id="1571b-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="1571b-106">\_O recurso de DL também é enviado periodicamente durante a arrastar, mesmo que o mouse não seja movido.</span><span class="sxs-lookup"><span data-stu-id="1571b-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="1571b-107">Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista.</span><span class="sxs-lookup"><span data-stu-id="1571b-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="1571b-108">Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="1571b-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1571b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1571b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1571b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1571b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1571b-111">O identificador de controle da caixa de listagem de arrastar.</span><span class="sxs-lookup"><span data-stu-id="1571b-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="1571b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1571b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1571b-113">Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o código de notificação de arrastar da DL \_ , o identificador para a caixa de listagem de arrastar e a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="1571b-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1571b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1571b-114">Return value</span></span>

<span data-ttu-id="1571b-115">O valor de retorno determina o tipo de cursor do mouse que a lista de arrastar deve definir; pode ser o valor DL \_ STOPCURSOR, DL \_ COPYCURSOR ou DL \_ MOVECURSOR.</span><span class="sxs-lookup"><span data-stu-id="1571b-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="1571b-116">Se qualquer outro valor for retornado, o cursor não será alterado.</span><span class="sxs-lookup"><span data-stu-id="1571b-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="1571b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1571b-117">Remarks</span></span>

<span data-ttu-id="1571b-118">Um procedimento de janela normalmente processa o \_ código de notificação de arrastar da DL determinando o item sob o cursor e, em seguida, desenhando um ícone de inserção.</span><span class="sxs-lookup"><span data-stu-id="1571b-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="1571b-119">Para recuperar o item sob o cursor, use a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , especificando **true** para o parâmetro *bAutoScroll* .</span><span class="sxs-lookup"><span data-stu-id="1571b-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="1571b-120">Essa opção faz com que a caixa de listagem de arrastar role periodicamente se o cursor estiver acima ou abaixo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="1571b-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="1571b-121">Para desenhar o ícone de inserção, use a função [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .</span><span class="sxs-lookup"><span data-stu-id="1571b-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1571b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1571b-122">Requirements</span></span>



| <span data-ttu-id="1571b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1571b-123">Requirement</span></span> | <span data-ttu-id="1571b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1571b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1571b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1571b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1571b-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1571b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1571b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1571b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1571b-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1571b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1571b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1571b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1571b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1571b-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





