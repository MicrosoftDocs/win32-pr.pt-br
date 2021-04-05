---
title: Mensagem de LVM_SORTITEMS (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SortItems do ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Controles de LVM_SORTITEMS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919246"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="24293-106">\_Mensagem SORTITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="24293-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="24293-107">Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="24293-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="24293-108">O índice de cada item é alterado para refletir a nova sequência.</span><span class="sxs-lookup"><span data-stu-id="24293-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="24293-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SortItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .</span><span class="sxs-lookup"><span data-stu-id="24293-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24293-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24293-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24293-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24293-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24293-112">Valor definido pelo aplicativo que é passado para a função de comparação.</span><span class="sxs-lookup"><span data-stu-id="24293-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="24293-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24293-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24293-114">Ponteiro para a função de comparação definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24293-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="24293-115">A função de comparação é chamada durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada.</span><span class="sxs-lookup"><span data-stu-id="24293-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24293-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24293-116">Return value</span></span>

<span data-ttu-id="24293-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="24293-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="24293-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="24293-118">Remarks</span></span>

<span data-ttu-id="24293-119">A função de comparação tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="24293-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="24293-120">O parâmetro *lParam1* é o valor associado ao primeiro item que está sendo comparado e o parâmetro *lParam2* é o valor associado ao segundo item.</span><span class="sxs-lookup"><span data-stu-id="24293-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="24293-121">Esses são os valores que foram especificados no membro **lParam** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dos itens quando eles foram inseridos na lista.</span><span class="sxs-lookup"><span data-stu-id="24293-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="24293-122">O parâmetro *wParam* do [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)é passado para a função de retorno de chamada como seu terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24293-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="24293-123">A função de comparação deve retornar um valor negativo se o primeiro item deve preceder o segundo, um valor positivo se o primeiro item deve seguir o segundo ou zero se os dois itens forem equivalentes.</span><span class="sxs-lookup"><span data-stu-id="24293-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="24293-124">Durante o processo de classificação, o conteúdo da exibição de lista é instável.</span><span class="sxs-lookup"><span data-stu-id="24293-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="24293-125">Se a função de retorno de chamada enviar todas as mensagens para o controle de exibição de lista, além do [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GETITEM**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="24293-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24293-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24293-126">Requirements</span></span>



| <span data-ttu-id="24293-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="24293-127">Requirement</span></span> | <span data-ttu-id="24293-128">Valor</span><span class="sxs-lookup"><span data-stu-id="24293-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24293-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24293-129">Minimum supported client</span></span><br/> | <span data-ttu-id="24293-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24293-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24293-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24293-131">Minimum supported server</span></span><br/> | <span data-ttu-id="24293-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24293-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24293-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24293-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="24293-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24293-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





