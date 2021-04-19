---
title: Método RegisteredTask. Run
description: Para scripts, o executa a tarefa registrada imediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Agendador de Tarefas do método de execução
- Método Run Agendador de Tarefas, objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, método Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810990"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="79669-106">Método RegisteredTask. Run</span><span class="sxs-lookup"><span data-stu-id="79669-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="79669-107">Para scripts, o executa a tarefa registrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="79669-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="79669-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79669-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="79669-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79669-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79669-110">*parâmetros* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79669-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79669-111">Os parâmetros usados como valores nas ações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="79669-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="79669-112">Para não especificar nenhum valor de parâmetro para as ações de tarefa, defina esse parâmetro como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="79669-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="79669-113">Caso contrário, um único valor de cadeia de caracteres ou uma matriz de valores de cadeia de caracteres pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="79669-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="79669-114">Os valores de cadeia de caracteres que você especifica são emparelhados com nomes e armazenados como pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="79669-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="79669-115">Se você especificar um único valor de cadeia de caracteres, Arg0 será o nome atribuído ao valor.</span><span class="sxs-lookup"><span data-stu-id="79669-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="79669-116">O valor pode ser usado na ação da tarefa em que a variável $ (Arg0) é usada nas propriedades da ação.</span><span class="sxs-lookup"><span data-stu-id="79669-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="79669-117">Se você passar valores como "0", "100" e "250" como uma matriz de valores de cadeia de caracteres, "0" substituirá as variáveis $ (Arg0), "100" substituirá as variáveis $ (arg1) e "250" substituirá as variáveis $ (arg2) usadas nas propriedades da ação.</span><span class="sxs-lookup"><span data-stu-id="79669-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="79669-118">Um máximo de 32 valores de cadeia de caracteres podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="79669-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="79669-119">Para obter mais informações e uma lista de propriedades de ação que podem usar as variáveis $ (Arg0), $ (arg1),..., $ (Arg32) em seus valores, consulte [ações de tarefas](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="79669-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="79669-120">*ppRunningTask* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="79669-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79669-121">Um objeto [**RunningTask**](runningtask.md) que define a nova instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="79669-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79669-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79669-122">Return value</span></span>

<span data-ttu-id="79669-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="79669-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79669-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="79669-124">Remarks</span></span>

<span data-ttu-id="79669-125">A função **RegisteredTask. Run** é equivalente à função [**RegisteredTask. RunEx**](registeredtask-runex.md) com o parâmetro flags igual a 0 e nada especificado para o parâmetro User.</span><span class="sxs-lookup"><span data-stu-id="79669-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="79669-126">Esse método retornará sem erro, mas a tarefa não será executada se a propriedade [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) for definida como false para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="79669-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="79669-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79669-127">Requirements</span></span>



| <span data-ttu-id="79669-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="79669-128">Requirement</span></span> | <span data-ttu-id="79669-129">Valor</span><span class="sxs-lookup"><span data-stu-id="79669-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79669-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79669-130">Minimum supported client</span></span><br/> | <span data-ttu-id="79669-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79669-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79669-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79669-132">Minimum supported server</span></span><br/> | <span data-ttu-id="79669-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79669-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79669-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79669-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="79669-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79669-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79669-136">DLL</span><span class="sxs-lookup"><span data-stu-id="79669-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79669-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79669-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79669-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="79669-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79669-139">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="79669-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="79669-140">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="79669-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





