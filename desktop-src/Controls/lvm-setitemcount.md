---
title: Mensagem de LVM_SETITEMCOUNT (commctrl. h)
description: Faz com que o controle de exibição de lista aloque memória para o número especificado de itens ou define o número virtual de itens em um controle de exibição de lista virtual.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Controles de LVM_SETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085337"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="affd2-104">Mensagem do LVM \_ SETitemcount</span><span class="sxs-lookup"><span data-stu-id="affd2-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="affd2-105">Faz com que o controle de exibição de lista aloque memória para o número especificado de itens ou define o número virtual de itens em um [controle de exibição de lista virtual](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="affd2-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="affd2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="affd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="affd2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="affd2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="affd2-108">O número de itens que o controle de exibição de lista contém, em última instância.</span><span class="sxs-lookup"><span data-stu-id="affd2-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="affd2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="affd2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="affd2-110">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="affd2-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="affd2-111">Valores que especificam o comportamento do controle de exibição de lista depois de redefinir a contagem de itens.</span><span class="sxs-lookup"><span data-stu-id="affd2-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="affd2-112">Esse valor pode ser uma combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="affd2-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="affd2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="affd2-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="affd2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="affd2-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="affd2-115"><dt>**LVSICF \_ NOINVALIDATEALL**</dt></span><span class="sxs-lookup"><span data-stu-id="affd2-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="affd2-116">O controle de exibição de lista não será redesenhado a menos que os itens afetados estejam atualmente em exibição.</span><span class="sxs-lookup"><span data-stu-id="affd2-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="affd2-117"><dt>**LVSICF \_ NOscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="affd2-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="affd2-118">O controle de exibição de lista não alterará a posição de rolagem quando a contagem de itens for alterada.</span><span class="sxs-lookup"><span data-stu-id="affd2-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="affd2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="affd2-119">Return value</span></span>

<span data-ttu-id="affd2-120">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="affd2-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="affd2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="affd2-121">Remarks</span></span>

<span data-ttu-id="affd2-122">A forma como a memória é alocada depende de como o controle de exibição de lista foi criado.</span><span class="sxs-lookup"><span data-stu-id="affd2-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="affd2-123">Você pode enviar essa mensagem explicitamente ou usar as macros de [**ListView \_ setitemcount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) ou [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .</span><span class="sxs-lookup"><span data-stu-id="affd2-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="affd2-124">Para obter mais informações, consulte [estilo de List-View virtual](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="affd2-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="affd2-125">Se o controle de exibição de lista tiver sido criado sem o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , o envio dessa mensagem fará com que o controle aloque suas estruturas de dados internas para o número de itens especificado.</span><span class="sxs-lookup"><span data-stu-id="affd2-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="affd2-126">Isso impede que o controle tenha que alocar as estruturas de dados toda vez que um item é adicionado.</span><span class="sxs-lookup"><span data-stu-id="affd2-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="affd2-127">Se o controle de exibição de lista tiver sido criado com o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) (uma exibição de lista virtual), o envio dessa mensagem definirá o número virtual de itens que o controle contém.</span><span class="sxs-lookup"><span data-stu-id="affd2-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="affd2-128">O parâmetro *lParam* destina-se somente a controles de exibição de lista que usam os estilos de [**LVS \_ OWNERDATA**](list-view-window-styles.md) e [**LVS \_**](list-view-window-styles.md) de [**\_ lista de LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="affd2-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="affd2-129">Quando a exibição de lista de controle comum é uma exibição de lista virtualizada ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), há um limite de 100 milhões itens na exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="affd2-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="affd2-130">Nesse cenário, o **LVM \_ setitemcount** retornará false quando tiver um *wParam* de 100.000.001.</span><span class="sxs-lookup"><span data-stu-id="affd2-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="affd2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="affd2-131">Requirements</span></span>



| <span data-ttu-id="affd2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="affd2-132">Requirement</span></span> | <span data-ttu-id="affd2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="affd2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="affd2-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="affd2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="affd2-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="affd2-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="affd2-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="affd2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="affd2-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="affd2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="affd2-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="affd2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="affd2-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="affd2-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

