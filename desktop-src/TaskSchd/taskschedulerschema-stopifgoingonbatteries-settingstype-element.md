---
title: Elemento StopIfGoingOnBatteries (settingstype)
description: Especifica que a tarefa será interrompida se o computador estiver indo para baterias.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Agendador de Tarefas do elemento StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759950"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="b97f2-104">Elemento StopIfGoingOnBatteries (settingstype)</span><span class="sxs-lookup"><span data-stu-id="b97f2-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="b97f2-105">Especifica que a tarefa será interrompida se o computador estiver indo para baterias.</span><span class="sxs-lookup"><span data-stu-id="b97f2-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="b97f2-106">O elemento **StopIfGoingOnBatteries** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b97f2-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b97f2-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="b97f2-107">Parent element</span></span>



| <span data-ttu-id="b97f2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b97f2-108">Element</span></span>                                                           | <span data-ttu-id="b97f2-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b97f2-109">Derived from</span></span>                                                         | <span data-ttu-id="b97f2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b97f2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b97f2-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="b97f2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="b97f2-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="b97f2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="b97f2-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b97f2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b97f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b97f2-114">Remarks</span></span>

<span data-ttu-id="b97f2-115">A configuração padrão para esse elemento é false.</span><span class="sxs-lookup"><span data-stu-id="b97f2-115">The default setting for this element is False.</span></span> <span data-ttu-id="b97f2-116">Observe que o valor padrão foi alterado de versões anteriores do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="b97f2-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="b97f2-117">Para o desenvolvimento de scripts, essa configuração é especificada usando a propriedade [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="b97f2-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="b97f2-118">Para desenvolvimento em C++, essa configuração é especificada usando a propriedade [**ITaskSettings:: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="b97f2-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b97f2-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b97f2-119">Examples</span></span>

<span data-ttu-id="b97f2-120">O XML a seguir define um elemento de configurações que permite um encerramento rígido da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b97f2-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="b97f2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b97f2-121">Requirements</span></span>



| <span data-ttu-id="b97f2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b97f2-122">Requirement</span></span> | <span data-ttu-id="b97f2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b97f2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b97f2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b97f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b97f2-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b97f2-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b97f2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b97f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b97f2-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b97f2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b97f2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b97f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97f2-129">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b97f2-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





