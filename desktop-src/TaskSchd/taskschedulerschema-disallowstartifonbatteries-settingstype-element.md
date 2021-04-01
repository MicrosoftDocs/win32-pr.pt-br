---
title: Elemento DisallowStartIfOnBatteries (settingstype)
description: Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Agendador de Tarefas do elemento DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645218"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="5a9cd-104">Elemento DisallowStartIfOnBatteries (settingstype)</span><span class="sxs-lookup"><span data-stu-id="5a9cd-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="5a9cd-105">Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="5a9cd-106">O elemento **DisallowStartIfOnBatteries** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9cd-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5a9cd-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5a9cd-107">Parent element</span></span>



| <span data-ttu-id="5a9cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a9cd-108">Element</span></span>                                                           | <span data-ttu-id="5a9cd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5a9cd-109">Derived from</span></span>                                                         | <span data-ttu-id="5a9cd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a9cd-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a9cd-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5a9cd-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="5a9cd-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5a9cd-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a9cd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a9cd-114">Remarks</span></span>

<span data-ttu-id="5a9cd-115">A configuração padrão para esse elemento é true.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-115">The default setting for this element is True.</span></span>

<span data-ttu-id="5a9cd-116">Para o desenvolvimento de scripts, essas informações são acessadas por meio da propriedade [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9cd-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="5a9cd-117">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="5a9cd-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5a9cd-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a9cd-118">Examples</span></span>

<span data-ttu-id="5a9cd-119">O XML a seguir define um elemento Settings que não permite que a tarefa seja executada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="5a9cd-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="5a9cd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a9cd-120">Requirements</span></span>



| <span data-ttu-id="5a9cd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a9cd-121">Requirement</span></span> | <span data-ttu-id="5a9cd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a9cd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a9cd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a9cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9cd-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a9cd-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a9cd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a9cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9cd-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a9cd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a9cd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a9cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9cd-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5a9cd-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





