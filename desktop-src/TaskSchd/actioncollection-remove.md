---
title: Método ActionCollection. Remove
description: Para scripts, remove a ação especificada da coleção.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Remover o método Agendador de Tarefas
- Método Remove Agendador de Tarefas, objeto ActionCollection
- Método de ação Agendador de Tarefas do objeto, remover
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644890"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="f643d-106">Método ActionCollection. Remove</span><span class="sxs-lookup"><span data-stu-id="f643d-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="f643d-107">Para scripts, remove a ação especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="f643d-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f643d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f643d-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="f643d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f643d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f643d-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f643d-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f643d-111">O índice da ação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f643d-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f643d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f643d-112">Return value</span></span>

<span data-ttu-id="f643d-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f643d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f643d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f643d-114">Remarks</span></span>

<span data-ttu-id="f643d-115">Ao remover itens, observe que o índice do primeiro item na coleção é 1 e o índice do último item é o valor da propriedade [**ActionCollection. Count**](actioncollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="f643d-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f643d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f643d-116">Requirements</span></span>



| <span data-ttu-id="f643d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f643d-117">Requirement</span></span> | <span data-ttu-id="f643d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f643d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f643d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f643d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f643d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f643d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f643d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f643d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f643d-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f643d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f643d-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f643d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f643d-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f643d-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f643d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f643d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f643d-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f643d-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f643d-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f643d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f643d-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f643d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f643d-129">**Açãocollection**</span><span class="sxs-lookup"><span data-stu-id="f643d-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





