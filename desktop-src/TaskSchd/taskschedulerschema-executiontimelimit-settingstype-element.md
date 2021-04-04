---
title: Elemento ExecutionTimeLimit (settingstype)
description: Quantidade de tempo permitido para concluir a tarefa.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Agendador de Tarefas do elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824236"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="c0ea4-104">Elemento ExecutionTimeLimit (settingstype)</span><span class="sxs-lookup"><span data-stu-id="c0ea4-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="c0ea4-105">Quantidade de tempo permitido para concluir a tarefa. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="c0ea4-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c0ea4-106">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="c0ea4-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="c0ea4-107">Um valor de PT0S permitirá que a tarefa seja executada indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="c0ea4-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="c0ea4-108">O elemento **ExecutionTimeLimit** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ea4-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c0ea4-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c0ea4-109">Parent element</span></span>



| <span data-ttu-id="c0ea4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0ea4-110">Element</span></span>                                                           | <span data-ttu-id="c0ea4-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c0ea4-111">Derived from</span></span>                                                         | <span data-ttu-id="c0ea4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0ea4-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0ea4-113">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c0ea4-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c0ea4-115">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c0ea4-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c0ea4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0ea4-116">Remarks</span></span>

<span data-ttu-id="c0ea4-117">Para desenvolvimento em C++, consulte a [**Propriedade ExecutionTimeLimit de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="c0ea4-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="c0ea4-118">Para o desenvolvimento de scripts, consulte [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="c0ea4-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ea4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0ea4-119">Requirements</span></span>



| <span data-ttu-id="c0ea4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ea4-120">Requirement</span></span> | <span data-ttu-id="c0ea4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c0ea4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0ea4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0ea4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ea4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0ea4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0ea4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0ea4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ea4-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0ea4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0ea4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0ea4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ea4-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c0ea4-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





