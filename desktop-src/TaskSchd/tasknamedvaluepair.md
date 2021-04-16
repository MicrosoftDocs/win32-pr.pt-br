---
title: Objeto TaskNamedValuePair
description: Objeto de script que é usado para criar um par de nome-valor no qual o nome está associado ao valor.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Agendador de Tarefas de objeto TaskNamedValuePair
- Agendador de Tarefas de objeto TaskNamedValuePair, descrito
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761339"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="27dd9-105">Objeto TaskNamedValuePair</span><span class="sxs-lookup"><span data-stu-id="27dd9-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="27dd9-106">Objeto de script que é usado para criar um par de nome-valor no qual o nome está associado ao valor.</span><span class="sxs-lookup"><span data-stu-id="27dd9-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="27dd9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="27dd9-107">Members</span></span>

<span data-ttu-id="27dd9-108">O objeto **TaskNamedValuePair** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="27dd9-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="27dd9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27dd9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27dd9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27dd9-110">Properties</span></span>

<span data-ttu-id="27dd9-111">O objeto **TaskNamedValuePair** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="27dd9-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="27dd9-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="27dd9-112">Property</span></span>                                             | <span data-ttu-id="27dd9-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="27dd9-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="27dd9-114">**Nome**</span><span class="sxs-lookup"><span data-stu-id="27dd9-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="27dd9-115">Obtém ou define o nome associado a um valor em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="27dd9-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="27dd9-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="27dd9-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="27dd9-117">Obtém ou define o valor associado a um nome em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="27dd9-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27dd9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="27dd9-118">Remarks</span></span>

<span data-ttu-id="27dd9-119">Ao ler ou gravar seu próprio XML para uma tarefa, um par nome-valor é especificado usando o elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="27dd9-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="27dd9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27dd9-120">Requirements</span></span>



| <span data-ttu-id="27dd9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="27dd9-121">Requirement</span></span> | <span data-ttu-id="27dd9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="27dd9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27dd9-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27dd9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27dd9-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27dd9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="27dd9-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27dd9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27dd9-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27dd9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27dd9-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="27dd9-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="27dd9-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="27dd9-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="27dd9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="27dd9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27dd9-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27dd9-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27dd9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="27dd9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27dd9-132">**TaskNamedValueCollection**</span><span class="sxs-lookup"><span data-stu-id="27dd9-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





