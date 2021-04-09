---
title: Método RegisteredTask. RunEx
description: Para scripts, o executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Agendador de Tarefas do método RunEx
- Método RunEx Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085883"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="eeee6-106">Método RegisteredTask. RunEx</span><span class="sxs-lookup"><span data-stu-id="eeee6-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="eeee6-107">Para scripts, o executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="eeee6-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeee6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eeee6-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="eeee6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eeee6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeee6-110">*parâmetros* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee6-111">Os parâmetros usados como valores nas ações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="eeee6-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="eeee6-112">Para não especificar nenhum valor de parâmetro para as ações de tarefa, defina esse parâmetro como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="eeee6-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="eeee6-113">Caso contrário, um único valor de cadeia de caracteres ou uma matriz de valores de cadeia de caracteres pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="eeee6-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="eeee6-114">Os valores de cadeia de caracteres que você especifica são emparelhados com nomes e armazenados como pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="eeee6-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="eeee6-115">Se você especificar um único valor de cadeia de caracteres, Arg0 será o nome atribuído ao valor.</span><span class="sxs-lookup"><span data-stu-id="eeee6-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="eeee6-116">O valor pode ser usado na ação da tarefa em que a variável $ (Arg0) é usada nas propriedades da ação.</span><span class="sxs-lookup"><span data-stu-id="eeee6-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="eeee6-117">Se você passar valores como "0", "100" e "250" como uma matriz de valores de cadeia de caracteres, "0" substituirá as variáveis $ (Arg0), "100" substituirá as variáveis $ (arg1) e "250" substituirá as variáveis $ (arg2) usadas nas propriedades da ação.</span><span class="sxs-lookup"><span data-stu-id="eeee6-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="eeee6-118">Um máximo de 32 valores de cadeia de caracteres podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="eeee6-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="eeee6-119">Para obter mais informações e uma lista de propriedades de ação que podem usar as variáveis $ (Arg0), $ (arg1),..., $ (Arg32) em seus valores, consulte [ações de tarefas](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="eeee6-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="eeee6-120">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee6-121">Uma constante de [ \_ \_ sinalizadores de execução de tarefa](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define como a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="eeee6-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="eeee6-122">*SessionID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee6-123">A sessão do Terminal Server na qual você deseja iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="eeee6-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="eeee6-124">Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ (0x4) não for passada para o parâmetro *flags* , o valor especificado nesse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="eeee6-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="eeee6-125">Se a execução da tarefa \_ \_ usar \_ \_ constante de ID de sessão for passada para o parâmetro *flags* e o valor SessionID for menor ou igual a 0, um erro de argumento inválido será retornado.</span><span class="sxs-lookup"><span data-stu-id="eeee6-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="eeee6-126">Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ for passada para o parâmetro *flags* e o valor SessionID for uma ID de sessão válida maior que 0 e se nenhum valor for especificado para o parâmetro *User* , o serviço de Agendador de tarefas tentará iniciar a tarefa interativamente como o usuário que fez logon na sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="eeee6-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="eeee6-127">Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ for passada para o parâmetro *flags* e o valor SessionID for uma ID de sessão válida maior que 0 e se um usuário for especificado no parâmetro *User* , o serviço de Agendador de tarefas tentará iniciar a tarefa interativamente como o usuário que é especificado no parâmetro *User* .</span><span class="sxs-lookup"><span data-stu-id="eeee6-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="eeee6-128">*runningTask* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee6-129">Um objeto [**RunningTask**](runningtask.md) que define a nova instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="eeee6-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeee6-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eeee6-130">Return value</span></span>

<span data-ttu-id="eeee6-131">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eeee6-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeee6-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeee6-132">Remarks</span></span>

<span data-ttu-id="eeee6-133">Esse método retornará sem erro, mas a tarefa não será executada se a propriedade [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) for definida como false para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="eeee6-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeee6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeee6-134">Requirements</span></span>



| <span data-ttu-id="eeee6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeee6-135">Requirement</span></span> | <span data-ttu-id="eeee6-136">Valor</span><span class="sxs-lookup"><span data-stu-id="eeee6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeee6-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeee6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eeee6-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eeee6-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeee6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eeee6-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eeee6-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eeee6-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eeee6-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="eeee6-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eeee6-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eeee6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="eeee6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeee6-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeee6-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeee6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="eeee6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeee6-146">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="eeee6-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="eeee6-147">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="eeee6-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





