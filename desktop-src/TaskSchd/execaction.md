---
title: Objeto execaction
description: Objeto de script que representa uma ação que executa uma operação de linha de comando.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- executar Agendador de Tarefas de ação, interface
- Agendador de Tarefas de objeto execaction
- Agendador de Tarefas de objeto execaction, descrito
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086226"
---
# <a name="execaction-object"></a><span data-ttu-id="a24d8-106">Objeto execaction</span><span class="sxs-lookup"><span data-stu-id="a24d8-106">ExecAction object</span></span>

<span data-ttu-id="a24d8-107">Objeto de script que representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a24d8-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="a24d8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a24d8-108">Members</span></span>

<span data-ttu-id="a24d8-109">O objeto **execaction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a24d8-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="a24d8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a24d8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a24d8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a24d8-111">Properties</span></span>

<span data-ttu-id="a24d8-112">O objeto **execaction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a24d8-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="a24d8-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a24d8-113">Property</span></span>                                                            | <span data-ttu-id="a24d8-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="a24d8-114">Access type</span></span>           | <span data-ttu-id="a24d8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a24d8-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a24d8-116">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="a24d8-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="a24d8-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a24d8-117">Read/write</span></span><br/> | <span data-ttu-id="a24d8-118">Obtém ou define os argumentos associados à operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a24d8-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="a24d8-119">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="a24d8-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="a24d8-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a24d8-120">Read/write</span></span><br/> | <span data-ttu-id="a24d8-121">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="a24d8-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="a24d8-122">Obtém ou define o identificador da ação.</span><span class="sxs-lookup"><span data-stu-id="a24d8-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="a24d8-123">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="a24d8-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="a24d8-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a24d8-124">Read/write</span></span><br/> | <span data-ttu-id="a24d8-125">Obtém ou define o caminho para um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="a24d8-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="a24d8-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a24d8-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="a24d8-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a24d8-127">Read-only</span></span><br/>  | <span data-ttu-id="a24d8-128">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="a24d8-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="a24d8-129">Obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="a24d8-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="a24d8-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="a24d8-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="a24d8-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a24d8-131">Read/write</span></span><br/> | <span data-ttu-id="a24d8-132">Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="a24d8-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a24d8-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a24d8-133">Remarks</span></span>

<span data-ttu-id="a24d8-134">Se as variáveis de ambiente forem usadas nas propriedades [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)ou [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , os valores das variáveis de ambiente serão armazenados em cache e usados quando a Taskeng.exe (o mecanismo de tarefa) for iniciada.</span><span class="sxs-lookup"><span data-stu-id="a24d8-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="a24d8-135">As alterações nas variáveis de ambiente que ocorrem após a inicialização do mecanismo de tarefa não serão usadas pelo mecanismo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="a24d8-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="a24d8-136">Essa ação executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a24d8-136">This action performs a command-line operation.</span></span> <span data-ttu-id="a24d8-137">Por exemplo, a ação pode executar um script ou iniciar um executável.</span><span class="sxs-lookup"><span data-stu-id="a24d8-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="a24d8-138">Ao ler ou gravar XML, uma ação de execução é especificada no elemento [**exec**](taskschedulerschema-exec-actiongroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a24d8-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a24d8-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a24d8-139">Examples</span></span>

<span data-ttu-id="a24d8-140">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="a24d8-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a24d8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a24d8-141">Requirements</span></span>



| <span data-ttu-id="a24d8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a24d8-142">Requirement</span></span> | <span data-ttu-id="a24d8-143">Valor</span><span class="sxs-lookup"><span data-stu-id="a24d8-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a24d8-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a24d8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a24d8-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a24d8-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a24d8-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a24d8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a24d8-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a24d8-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a24d8-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a24d8-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="a24d8-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a24d8-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a24d8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a24d8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a24d8-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a24d8-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





