---
title: DL_DROPPED código de notificação (commctrl. h)
description: Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte arrastar mensagens da caixa de listagem.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824870"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="055e2-106">\_Código de notificação removido da DL</span><span class="sxs-lookup"><span data-stu-id="055e2-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="055e2-107">Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="055e2-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="055e2-108">Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista.</span><span class="sxs-lookup"><span data-stu-id="055e2-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="055e2-109">Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="055e2-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="055e2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="055e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="055e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="055e2-112">Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o \_ código de notificação DL removido, o identificador para a caixa de listagem de arrastar e a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="055e2-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="055e2-113">Return value</span></span>

<span data-ttu-id="055e2-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="055e2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="055e2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="055e2-115">Remarks</span></span>

<span data-ttu-id="055e2-116">Esse código de notificação normalmente é processado pela inserção do item que está sendo arrastado para a lista na frente do item sob o cursor.</span><span class="sxs-lookup"><span data-stu-id="055e2-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="055e2-117">Para recuperar o índice do item na posição do cursor, use a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="055e2-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="055e2-118">Observe que o \_ código de notificação DL removido é enviado mesmo que o cursor não esteja em um item de lista.</span><span class="sxs-lookup"><span data-stu-id="055e2-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="055e2-119">Nesse caso, **LBItemFromPt** retorna-1.</span><span class="sxs-lookup"><span data-stu-id="055e2-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="055e2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="055e2-120">Requirements</span></span>



| <span data-ttu-id="055e2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="055e2-121">Requirement</span></span> | <span data-ttu-id="055e2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="055e2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="055e2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="055e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="055e2-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="055e2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="055e2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="055e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="055e2-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="055e2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="055e2-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="055e2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="055e2-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="055e2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





