---
title: Elemento RunOnlyIfNetworkAvailable (settingstype)
description: Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Agendador de Tarefas do elemento RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918940"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="25aec-104">Elemento RunOnlyIfNetworkAvailable (settingstype)</span><span class="sxs-lookup"><span data-stu-id="25aec-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="25aec-105">Especifica que a Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="25aec-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="25aec-106">O elemento **RunOnlyIfNetworkAvailable** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="25aec-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="25aec-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="25aec-107">Parent element</span></span>



| <span data-ttu-id="25aec-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="25aec-108">Element</span></span>                                                           | <span data-ttu-id="25aec-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="25aec-109">Derived from</span></span>                                                         | <span data-ttu-id="25aec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="25aec-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="25aec-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="25aec-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="25aec-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="25aec-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="25aec-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="25aec-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="25aec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25aec-114">Remarks</span></span>

<span data-ttu-id="25aec-115">Para desenvolvimento em C++, consulte a [**Propriedade RunOnlyIfNetworkAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="25aec-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="25aec-116">Para desenvolvimento de script, consulte [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="25aec-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="25aec-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25aec-117">Examples</span></span>

<span data-ttu-id="25aec-118">O XML a seguir define um elemento Settings que permite que a tarefa seja iniciada somente se uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="25aec-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="25aec-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25aec-119">Requirements</span></span>



| <span data-ttu-id="25aec-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25aec-120">Requirement</span></span> | <span data-ttu-id="25aec-121">Valor</span><span class="sxs-lookup"><span data-stu-id="25aec-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25aec-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25aec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25aec-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25aec-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25aec-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25aec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25aec-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25aec-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25aec-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="25aec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25aec-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="25aec-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





