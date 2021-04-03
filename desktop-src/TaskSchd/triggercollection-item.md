---
title: Propriedade TriggerCollection. Item
description: Para scripts, obtém o gatilho especificado da coleção.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de tarefas, objeto disparador
- Agendador de Tarefas de objeto TriggerCollection, Propriedade Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644468"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="18999-106">Propriedade TriggerCollection. Item</span><span class="sxs-lookup"><span data-stu-id="18999-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="18999-107">Para scripts, obtém o gatilho especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="18999-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="18999-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18999-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="18999-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="18999-109">Property value</span></span>

<span data-ttu-id="18999-110">Um objeto de [**gatilho**](trigger.md) que representa o gatilho solicitado.</span><span class="sxs-lookup"><span data-stu-id="18999-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="18999-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="18999-111">Remarks</span></span>

<span data-ttu-id="18999-112">As coleções são baseadas em 1.</span><span class="sxs-lookup"><span data-stu-id="18999-112">Collections are 1-based.</span></span> <span data-ttu-id="18999-113">Em outras palavras, o índice do primeiro item na coleção é 1.</span><span class="sxs-lookup"><span data-stu-id="18999-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="18999-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18999-114">Requirements</span></span>



| <span data-ttu-id="18999-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="18999-115">Requirement</span></span> | <span data-ttu-id="18999-116">Valor</span><span class="sxs-lookup"><span data-stu-id="18999-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18999-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18999-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18999-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18999-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18999-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18999-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18999-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18999-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18999-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="18999-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="18999-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18999-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18999-123">DLL</span><span class="sxs-lookup"><span data-stu-id="18999-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18999-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18999-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18999-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="18999-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18999-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="18999-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





