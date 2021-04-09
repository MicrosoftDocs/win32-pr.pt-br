---
title: Propriedade RunningTaskCollection. Item
description: Para scripts, obtém a tarefa especificada da coleção.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de Tarefas, objeto RunningTaskCollection
- Agendador de Tarefas de objeto RunningTaskCollection, Propriedade Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085879"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="6e85e-106">Propriedade RunningTaskCollection. Item</span><span class="sxs-lookup"><span data-stu-id="6e85e-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="6e85e-107">Para scripts, obtém a tarefa especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="6e85e-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e85e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e85e-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="6e85e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e85e-109">Property value</span></span>

<span data-ttu-id="6e85e-110">Um objeto [**RunningTask**](runningtask.md) que contém o contexto solicitado.</span><span class="sxs-lookup"><span data-stu-id="6e85e-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e85e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e85e-111">Remarks</span></span>

<span data-ttu-id="6e85e-112">As coleções são baseadas em 1.</span><span class="sxs-lookup"><span data-stu-id="6e85e-112">Collections are 1-based.</span></span> <span data-ttu-id="6e85e-113">Em outras palavras, o índice do primeiro item na coleção é 1.</span><span class="sxs-lookup"><span data-stu-id="6e85e-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e85e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e85e-114">Requirements</span></span>



| <span data-ttu-id="6e85e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e85e-115">Requirement</span></span> | <span data-ttu-id="6e85e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6e85e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e85e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e85e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e85e-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6e85e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e85e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e85e-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e85e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e85e-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e85e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e85e-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e85e-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e85e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6e85e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e85e-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e85e-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e85e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e85e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e85e-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6e85e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





