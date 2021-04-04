---
title: Mensagem de LVM_SORTITEMSEX (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SortItemsEx do ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Controles de LVM_SORTITEMSEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008935"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="b0e89-106">\_Mensagem SORTITEMSEX LVM</span><span class="sxs-lookup"><span data-stu-id="b0e89-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="b0e89-107">Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b0e89-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="b0e89-108">O índice de cada item é alterado para refletir a nova sequência.</span><span class="sxs-lookup"><span data-stu-id="b0e89-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="b0e89-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SortItemsEx do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .</span><span class="sxs-lookup"><span data-stu-id="b0e89-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0e89-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0e89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e89-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0e89-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e89-112">Valor definido pelo aplicativo que é passado para a função de comparação.</span><span class="sxs-lookup"><span data-stu-id="b0e89-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="b0e89-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0e89-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e89-114">Ponteiro para uma função de comparação definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0e89-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="b0e89-115">Ele é chamado durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada.</span><span class="sxs-lookup"><span data-stu-id="b0e89-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e89-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0e89-116">Return value</span></span>

<span data-ttu-id="b0e89-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b0e89-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e89-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0e89-118">Remarks</span></span>

<span data-ttu-id="b0e89-119">A função de comparação tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b0e89-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="b0e89-120">Essa mensagem é semelhante ao [**LVM \_ SORTITEMS**](lvm-sortitems.md), exceto pelo tipo de informação passado para a função de comparação.</span><span class="sxs-lookup"><span data-stu-id="b0e89-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="b0e89-121">Com o **LVM \_ SORTITEMSEX**, *lParam1* é o índice atual do primeiro item e *lParam2* é o índice atual do segundo item.</span><span class="sxs-lookup"><span data-stu-id="b0e89-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="b0e89-122">Você pode enviar uma mensagem [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) para recuperar mais informações sobre um item, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b0e89-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="b0e89-123">A função de comparação deve retornar um valor negativo se o primeiro item deve preceder o segundo, um valor positivo se o primeiro item deve seguir o segundo ou zero se os dois itens forem equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b0e89-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="b0e89-124">Durante o processo de classificação, o conteúdo da exibição de lista é instável.</span><span class="sxs-lookup"><span data-stu-id="b0e89-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="b0e89-125">Se a função de retorno de chamada enviar todas as mensagens para o controle de exibição de lista, além do [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GETITEM**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b0e89-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0e89-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0e89-126">Requirements</span></span>



| <span data-ttu-id="b0e89-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e89-127">Requirement</span></span> | <span data-ttu-id="b0e89-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b0e89-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e89-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0e89-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e89-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0e89-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0e89-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0e89-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e89-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0e89-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0e89-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0e89-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e89-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e89-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





