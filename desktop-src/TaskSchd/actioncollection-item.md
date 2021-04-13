---
title: Propriedade ActionCollection. Item
description: Para scripts, obtém uma ação especificada da coleção.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de Tarefas, objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, Propriedade Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369793"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="73179-106">Propriedade ActionCollection. Item</span><span class="sxs-lookup"><span data-stu-id="73179-106">ActionCollection.Item property</span></span>

<span data-ttu-id="73179-107">Para scripts, obtém uma ação especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="73179-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="73179-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73179-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="73179-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="73179-109">Property value</span></span>

<span data-ttu-id="73179-110">Um objeto de [**ação**](action.md) que representa a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="73179-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="73179-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="73179-111">Remarks</span></span>

<span data-ttu-id="73179-112">As coleções são baseadas em 1.</span><span class="sxs-lookup"><span data-stu-id="73179-112">Collections are 1-based.</span></span> <span data-ttu-id="73179-113">Em outras palavras, o índice do primeiro item na coleção é 1.</span><span class="sxs-lookup"><span data-stu-id="73179-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="73179-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73179-114">Requirements</span></span>



| <span data-ttu-id="73179-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="73179-115">Requirement</span></span> | <span data-ttu-id="73179-116">Valor</span><span class="sxs-lookup"><span data-stu-id="73179-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73179-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73179-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73179-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73179-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="73179-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73179-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73179-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73179-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73179-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="73179-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="73179-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73179-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73179-123">DLL</span><span class="sxs-lookup"><span data-stu-id="73179-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73179-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73179-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73179-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="73179-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73179-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="73179-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="73179-127">**Açãocollection**</span><span class="sxs-lookup"><span data-stu-id="73179-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





