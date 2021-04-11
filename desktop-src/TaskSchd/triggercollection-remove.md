---
title: Método TriggerCollection. Remove
description: Para scripts, remove o gatilho especificado da coleção de gatilhos usados pela tarefa.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- disparadores Agendador de Tarefas, removendo
- Remover o método Agendador de Tarefas
- Método Remove Agendador de tarefas, objeto disparador
- Agendador de Tarefas de objeto TriggerCollection, método remove
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295770"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="23141-107">Método TriggerCollection. Remove</span><span class="sxs-lookup"><span data-stu-id="23141-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="23141-108">Para scripts, remove o gatilho especificado da coleção de gatilhos usados pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="23141-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="23141-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23141-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="23141-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23141-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23141-111">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="23141-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23141-112">O índice do gatilho a ser removido.</span><span class="sxs-lookup"><span data-stu-id="23141-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23141-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23141-113">Return value</span></span>

<span data-ttu-id="23141-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="23141-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23141-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="23141-115">Remarks</span></span>

<span data-ttu-id="23141-116">Ao remover itens, observe que o índice do primeiro item na coleção é 1 e o índice do último item é o valor da propriedade [**TriggerCollection. Count**](triggercollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="23141-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="23141-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23141-117">Requirements</span></span>



| <span data-ttu-id="23141-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="23141-118">Requirement</span></span> | <span data-ttu-id="23141-119">Valor</span><span class="sxs-lookup"><span data-stu-id="23141-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23141-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23141-120">Minimum supported client</span></span><br/> | <span data-ttu-id="23141-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23141-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23141-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23141-122">Minimum supported server</span></span><br/> | <span data-ttu-id="23141-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23141-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23141-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="23141-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="23141-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23141-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23141-126">DLL</span><span class="sxs-lookup"><span data-stu-id="23141-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23141-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23141-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23141-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="23141-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23141-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="23141-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





