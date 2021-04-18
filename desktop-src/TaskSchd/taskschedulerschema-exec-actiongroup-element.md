---
title: Elemento exec (actionproperty)
description: Especifica uma ação que executa uma operação de linha de comando.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Agendador de Tarefas do elemento exec
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810114"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="98acd-104">Elemento exec (actionproperty)</span><span class="sxs-lookup"><span data-stu-id="98acd-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="98acd-105">Especifica uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="98acd-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="98acd-106">O elemento **exec** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="98acd-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="98acd-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="98acd-107">Parent element</span></span>



| <span data-ttu-id="98acd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="98acd-108">Element</span></span>                                                         | <span data-ttu-id="98acd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="98acd-109">Derived from</span></span>                                                       | <span data-ttu-id="98acd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="98acd-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="98acd-111">**Ações**</span><span class="sxs-lookup"><span data-stu-id="98acd-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="98acd-112">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="98acd-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="98acd-113">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="98acd-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="98acd-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="98acd-114">Child elements</span></span>



| <span data-ttu-id="98acd-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="98acd-115">Element</span></span>                                                                           | <span data-ttu-id="98acd-116">Type</span><span class="sxs-lookup"><span data-stu-id="98acd-116">Type</span></span>       | <span data-ttu-id="98acd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="98acd-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98acd-118">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="98acd-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="98acd-119">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98acd-119">**string**</span></span> | <span data-ttu-id="98acd-120">Especifica os argumentos associados à operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="98acd-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="98acd-121">**Comando**</span><span class="sxs-lookup"><span data-stu-id="98acd-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="98acd-122">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98acd-122">**string**</span></span> | <span data-ttu-id="98acd-123">Especifica o arquivo ou documento executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="98acd-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="98acd-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="98acd-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="98acd-125">string</span><span class="sxs-lookup"><span data-stu-id="98acd-125">string</span></span>     | <span data-ttu-id="98acd-126">Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.</span><span class="sxs-lookup"><span data-stu-id="98acd-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="98acd-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="98acd-127">Attributes</span></span>



| <span data-ttu-id="98acd-128">Nome</span><span class="sxs-lookup"><span data-stu-id="98acd-128">Name</span></span> | <span data-ttu-id="98acd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="98acd-129">Type</span></span>       | <span data-ttu-id="98acd-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="98acd-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="98acd-131">id</span><span class="sxs-lookup"><span data-stu-id="98acd-131">id</span></span>   | <span data-ttu-id="98acd-132">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98acd-132">**string**</span></span> | <span data-ttu-id="98acd-133">O identificador da ação executada pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="98acd-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="98acd-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="98acd-134">Remarks</span></span>

<span data-ttu-id="98acd-135">Os elementos filho listados acima são definidos pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="98acd-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="98acd-136">Para o desenvolvimento de script, uma ação de execução é definida pelo objeto [**execaction**](execaction.md) .</span><span class="sxs-lookup"><span data-stu-id="98acd-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="98acd-137">Para desenvolvimento em C++, uma ação de execução é definida pela interface [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .</span><span class="sxs-lookup"><span data-stu-id="98acd-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="98acd-138">Se as variáveis de ambiente forem usadas nos elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)ou [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , os valores das variáveis de ambiente serão armazenados em cache e usados quando a Taskeng.exe (o mecanismo de tarefa) for iniciada.</span><span class="sxs-lookup"><span data-stu-id="98acd-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="98acd-139">As alterações nas variáveis de ambiente que ocorrem após a inicialização do mecanismo de tarefa não serão usadas pelo mecanismo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="98acd-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="98acd-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98acd-140">Examples</span></span>

<span data-ttu-id="98acd-141">Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="98acd-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98acd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98acd-142">Requirements</span></span>



| <span data-ttu-id="98acd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="98acd-143">Requirement</span></span> | <span data-ttu-id="98acd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="98acd-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98acd-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98acd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="98acd-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98acd-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98acd-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98acd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="98acd-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98acd-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98acd-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="98acd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98acd-150">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="98acd-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





