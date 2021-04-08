---
title: Objeto RegisteredTaskCollection
description: Objeto de script que contém todas as tarefas registradas.
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- Agendador de Tarefas de objeto RegisteredTaskCollection
- Agendador de Tarefas de objeto RegisteredTaskCollection, descrito
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009045"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="60ef5-105">Objeto RegisteredTaskCollection</span><span class="sxs-lookup"><span data-stu-id="60ef5-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="60ef5-106">Objeto de script que contém todas as tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="60ef5-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="60ef5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="60ef5-107">Members</span></span>

<span data-ttu-id="60ef5-108">O objeto **RegisteredTaskCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="60ef5-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="60ef5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60ef5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60ef5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60ef5-110">Properties</span></span>

<span data-ttu-id="60ef5-111">O objeto **RegisteredTaskCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="60ef5-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="60ef5-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="60ef5-112">Property</span></span>                                                   | <span data-ttu-id="60ef5-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="60ef5-113">Access type</span></span>          | <span data-ttu-id="60ef5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ef5-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="60ef5-115">**Contar**</span><span class="sxs-lookup"><span data-stu-id="60ef5-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="60ef5-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60ef5-116">Read-only</span></span><br/> | <span data-ttu-id="60ef5-117">Obtém o número de tarefas registradas na coleção.</span><span class="sxs-lookup"><span data-stu-id="60ef5-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="60ef5-118">**Item**</span><span class="sxs-lookup"><span data-stu-id="60ef5-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="60ef5-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60ef5-119">Read-only</span></span><br/> | <span data-ttu-id="60ef5-120">Obtém a tarefa registrada especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="60ef5-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="60ef5-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60ef5-121">Examples</span></span>

<span data-ttu-id="60ef5-122">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exibindo nomes de tarefas e Estados (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="60ef5-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ef5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ef5-123">Requirements</span></span>



| <span data-ttu-id="60ef5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ef5-124">Requirement</span></span> | <span data-ttu-id="60ef5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="60ef5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60ef5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ef5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="60ef5-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60ef5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="60ef5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ef5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="60ef5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60ef5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60ef5-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="60ef5-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="60ef5-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60ef5-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60ef5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="60ef5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60ef5-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60ef5-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ef5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="60ef5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ef5-135">**TaskFolder. gettasks**</span><span class="sxs-lookup"><span data-stu-id="60ef5-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





