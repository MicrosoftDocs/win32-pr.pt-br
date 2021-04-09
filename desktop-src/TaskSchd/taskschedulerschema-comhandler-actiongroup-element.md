---
title: Elemento comhandlers (The actioner)
description: Especifica uma ação que dispara um manipulador.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Agendador de Tarefas de elemento do commanipulador
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918904"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="7402e-104">Elemento comhandlers (The actioner)</span><span class="sxs-lookup"><span data-stu-id="7402e-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="7402e-105">Especifica uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="7402e-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="7402e-106">O elemento **commanipulador** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="7402e-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="7402e-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="7402e-107">Parent element</span></span>



| <span data-ttu-id="7402e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7402e-108">Element</span></span>                                                         | <span data-ttu-id="7402e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7402e-109">Derived from</span></span>                                                       | <span data-ttu-id="7402e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7402e-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7402e-111">**Ações**</span><span class="sxs-lookup"><span data-stu-id="7402e-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="7402e-112">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="7402e-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="7402e-113">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="7402e-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="7402e-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7402e-114">Child elements</span></span>



| <span data-ttu-id="7402e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="7402e-115">Element</span></span>                                                               | <span data-ttu-id="7402e-116">Type</span><span class="sxs-lookup"><span data-stu-id="7402e-116">Type</span></span>                                                         | <span data-ttu-id="7402e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7402e-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="7402e-118">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="7402e-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="7402e-119">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="7402e-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="7402e-120">Especifica o identificador da classe do manipulador.</span><span class="sxs-lookup"><span data-stu-id="7402e-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="7402e-121">**Dados**</span><span class="sxs-lookup"><span data-stu-id="7402e-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="7402e-122">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="7402e-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="7402e-123">Especifica dados adicionais associados ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="7402e-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7402e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7402e-124">Remarks</span></span>

<span data-ttu-id="7402e-125">Os aplicativos definem uma ação de manipulador COM usando a interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="7402e-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="7402e-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="7402e-126">Attributes</span></span>

<span data-ttu-id="7402e-127">O atributo a seguir é definido pelo tipo complexo [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7402e-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="7402e-128">ID: identificador da ação executada pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="7402e-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="7402e-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7402e-129">Examples</span></span>

<span data-ttu-id="7402e-130">O XML a seguir define uma ação de manipulador COM.</span><span class="sxs-lookup"><span data-stu-id="7402e-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="7402e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7402e-131">Requirements</span></span>



| <span data-ttu-id="7402e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7402e-132">Requirement</span></span> | <span data-ttu-id="7402e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7402e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7402e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7402e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7402e-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7402e-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7402e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7402e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7402e-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7402e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7402e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7402e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7402e-139">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7402e-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





