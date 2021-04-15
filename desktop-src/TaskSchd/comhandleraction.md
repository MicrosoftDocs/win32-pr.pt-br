---
title: Objeto comhandleaction
description: Objeto de script que representa uma ação que dispara um manipulador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Ação do manipulador COM Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto comhandleaction
- Agendador de Tarefas de objeto comhandleaction, descrito
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454589"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="5b5a5-106">Objeto comhandleaction</span><span class="sxs-lookup"><span data-stu-id="5b5a5-106">ComHandlerAction object</span></span>

<span data-ttu-id="5b5a5-107">Objeto de script que representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="5b5a5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5b5a5-108">Members</span></span>

<span data-ttu-id="5b5a5-109">O objeto **Comhandleaction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b5a5-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="5b5a5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b5a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b5a5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b5a5-111">Properties</span></span>

<span data-ttu-id="5b5a5-112">O objeto **Comhandleaction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="5b5a5-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5a5-113">Property</span></span>                                               | <span data-ttu-id="5b5a5-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5b5a5-114">Access type</span></span>           | <span data-ttu-id="5b5a5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b5a5-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b5a5-116">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="5b5a5-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="5b5a5-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5a5-117">Read/write</span></span><br/> | <span data-ttu-id="5b5a5-118">Obtém ou define o identificador da classe do manipulador.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="5b5a5-119">**Dados**</span><span class="sxs-lookup"><span data-stu-id="5b5a5-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="5b5a5-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5a5-120">Read/write</span></span><br/> | <span data-ttu-id="5b5a5-121">Obtém ou define dados adicionais associados ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="5b5a5-122">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="5b5a5-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="5b5a5-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5a5-123">Read/write</span></span><br/> | <span data-ttu-id="5b5a5-124">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="5b5a5-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="5b5a5-125">Obtém ou define o identificador da ação.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="5b5a5-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b5a5-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="5b5a5-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b5a5-127">Read-only</span></span><br/>  | <span data-ttu-id="5b5a5-128">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="5b5a5-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="5b5a5-129">Obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="5b5a5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b5a5-130">Remarks</span></span>

<span data-ttu-id="5b5a5-131">Os manipuladores COM devem implementar a interface [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para o Agendador de tarefas Iniciar e parar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="5b5a5-132">Por sua vez, o manipulador COM usa os métodos do objeto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar o status de volta para o Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="5b5a5-133">Ao ler ou gravar XML, uma ação de manipulador COM é especificada no elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="5b5a5-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5a5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5a5-134">Requirements</span></span>



| <span data-ttu-id="5b5a5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5a5-135">Requirement</span></span> | <span data-ttu-id="5b5a5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5a5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5a5-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5a5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5a5-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b5a5-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5b5a5-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5a5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5a5-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b5a5-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b5a5-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b5a5-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b5a5-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b5a5-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b5a5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5b5a5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5a5-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b5a5-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5a5-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5a5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5a5-146">**TaskHandlerStatus**</span><span class="sxs-lookup"><span data-stu-id="5b5a5-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="5b5a5-147">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5b5a5-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="5b5a5-148">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5b5a5-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





