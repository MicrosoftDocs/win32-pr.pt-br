---
title: Elemento DeleteExpiredTaskAfter (settingstype)
description: Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Agendador de Tarefas do elemento DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761809"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="803a0-104">Elemento DeleteExpiredTaskAfter (settingstype)</span><span class="sxs-lookup"><span data-stu-id="803a0-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="803a0-105">Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.</span><span class="sxs-lookup"><span data-stu-id="803a0-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="803a0-106">Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas não excluirá a tarefa.</span><span class="sxs-lookup"><span data-stu-id="803a0-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="803a0-107">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="803a0-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="803a0-108">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="803a0-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="803a0-109">O elemento **DeleteExpiredTaskAfter** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="803a0-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="803a0-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="803a0-110">Parent element</span></span>



| <span data-ttu-id="803a0-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="803a0-111">Element</span></span>                                                           | <span data-ttu-id="803a0-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="803a0-112">Derived from</span></span>                                                         | <span data-ttu-id="803a0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="803a0-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="803a0-114">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="803a0-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="803a0-115">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="803a0-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="803a0-116">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="803a0-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="803a0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="803a0-117">Remarks</span></span>

<span data-ttu-id="803a0-118">Para desenvolvimento em C++, consulte a [**Propriedade DeleteExpiredTaskAfter de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="803a0-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="803a0-119">Para desenvolvimento de script, consulte [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="803a0-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="803a0-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="803a0-120">Examples</span></span>

<span data-ttu-id="803a0-121">O XML a seguir define um elemento de configurações que exclui uma tarefa expirada após uma semana.</span><span class="sxs-lookup"><span data-stu-id="803a0-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="803a0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="803a0-122">Requirements</span></span>



| <span data-ttu-id="803a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="803a0-123">Requirement</span></span> | <span data-ttu-id="803a0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="803a0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="803a0-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="803a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="803a0-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="803a0-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="803a0-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="803a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="803a0-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="803a0-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="803a0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="803a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803a0-130">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="803a0-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





