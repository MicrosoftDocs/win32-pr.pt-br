---
title: Elemento habilitado (settingstype)
description: Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Elemento habilitado Agendador de Tarefas
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757605"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="a1a1c-105">Elemento habilitado (settingstype)</span><span class="sxs-lookup"><span data-stu-id="a1a1c-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="a1a1c-106">Especifica que a tarefa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="a1a1c-107">A tarefa pode ser executada somente quando essa configuração for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="a1a1c-108">O elemento **Enabled** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1a1c-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a1a1c-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a1a1c-109">Parent element</span></span>



| <span data-ttu-id="a1a1c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a1a1c-110">Element</span></span>                                                           | <span data-ttu-id="a1a1c-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a1a1c-111">Derived from</span></span>                                                         | <span data-ttu-id="a1a1c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1a1c-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1a1c-113">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="a1a1c-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a1a1c-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="a1a1c-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a1a1c-115">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a1a1c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1a1c-116">Remarks</span></span>

<span data-ttu-id="a1a1c-117">Para desenvolvimento em C++, consulte a [**Propriedade Enabled de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="a1a1c-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="a1a1c-118">Para desenvolvimento de script, consulte [**TaskSettings. Enabled**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="a1a1c-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a1a1c-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1a1c-119">Examples</span></span>

<span data-ttu-id="a1a1c-120">Para obter um exemplo completo do XML para uma tarefa habilitada, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="a1a1c-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a1c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1a1c-121">Requirements</span></span>



| <span data-ttu-id="a1a1c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a1c-122">Requirement</span></span> | <span data-ttu-id="a1a1c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a1a1c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1a1c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1a1c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a1c-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1a1c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1a1c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1a1c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a1c-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1a1c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





