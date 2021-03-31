---
title: Elemento NetworkProfileName (settingstype)
description: Contém o nome de um perfil de rede. O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento RunOnlyIfNetworkAvailable é definido como true. O nome é usado para fins de exibição.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Agendador de Tarefas do elemento NetworkProfileName
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644814"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="a2054-106">Elemento NetworkProfileName (settingstype)</span><span class="sxs-lookup"><span data-stu-id="a2054-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="a2054-107">Contém o nome de um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="a2054-107">Contains the name of a network profile.</span></span> <span data-ttu-id="a2054-108">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a2054-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="a2054-109">O nome é usado para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="a2054-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="a2054-110">O elemento **NetworkProfileName** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a2054-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a2054-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a2054-111">Parent element</span></span>



| <span data-ttu-id="a2054-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="a2054-112">Element</span></span>                                                                      | <span data-ttu-id="a2054-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a2054-113">Derived from</span></span>                                                         | <span data-ttu-id="a2054-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2054-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2054-115">**Configurações (taskType)**</span><span class="sxs-lookup"><span data-stu-id="a2054-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a2054-116">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="a2054-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a2054-117">Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a2054-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a2054-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2054-118">Requirements</span></span>



| <span data-ttu-id="a2054-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2054-119">Requirement</span></span> | <span data-ttu-id="a2054-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2054-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2054-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2054-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2054-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2054-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2054-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2054-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2054-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2054-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





