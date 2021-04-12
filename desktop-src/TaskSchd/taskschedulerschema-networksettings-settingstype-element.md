---
title: Elemento NetworkSettings (settingstype)
description: Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento RunOnlyIfNetworkAvailable é definido como true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Agendador de Tarefas do elemento NetworkSettings
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455395"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="65fc1-105">Elemento NetworkSettings (settingstype)</span><span class="sxs-lookup"><span data-stu-id="65fc1-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="65fc1-106">Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="65fc1-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="65fc1-107">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="65fc1-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="65fc1-108">O elemento **NetworkSettings** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="65fc1-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="65fc1-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="65fc1-109">Parent element</span></span>



| <span data-ttu-id="65fc1-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="65fc1-110">Element</span></span>                                                                      | <span data-ttu-id="65fc1-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="65fc1-111">Derived from</span></span>                                                         | <span data-ttu-id="65fc1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="65fc1-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="65fc1-113">**Configurações (taskType)**</span><span class="sxs-lookup"><span data-stu-id="65fc1-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="65fc1-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="65fc1-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="65fc1-115">Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="65fc1-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65fc1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="65fc1-116">Remarks</span></span>

<span data-ttu-id="65fc1-117">Para desenvolvimento em C++, consulte a [**Propriedade NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="65fc1-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="65fc1-118">Para desenvolvimento de script, consulte [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="65fc1-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65fc1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65fc1-119">Requirements</span></span>



| <span data-ttu-id="65fc1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65fc1-120">Requirement</span></span> | <span data-ttu-id="65fc1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="65fc1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65fc1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65fc1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65fc1-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65fc1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65fc1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65fc1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65fc1-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65fc1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





