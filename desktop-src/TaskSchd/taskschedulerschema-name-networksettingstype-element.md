---
title: Elemento Name (networkSettingsType)
description: Contém o nome de um perfil de rede. O nome é usado para fins de exibição.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Elemento Name Agendador de Tarefas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499472"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="a23cf-105">Elemento Name (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="a23cf-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="a23cf-106">Contém o nome de um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="a23cf-106">Contains the name of a network profile.</span></span> <span data-ttu-id="a23cf-107">O nome é usado para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="a23cf-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="a23cf-108">O elemento **Name** é definido pelo tipo complexo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a23cf-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a23cf-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a23cf-109">Parent element</span></span>



| <span data-ttu-id="a23cf-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a23cf-110">Element</span></span>                                                                                            | <span data-ttu-id="a23cf-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a23cf-111">Derived from</span></span>                                                                       | <span data-ttu-id="a23cf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a23cf-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a23cf-113">**NetworkSettings (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="a23cf-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="a23cf-114">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a23cf-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="a23cf-115">Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="a23cf-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="a23cf-116">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a23cf-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a23cf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a23cf-117">Remarks</span></span>

<span data-ttu-id="a23cf-118">Para desenvolvimento em C++, consulte a [**Propriedade Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="a23cf-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="a23cf-119">Para o desenvolvimento de scripts, consulte [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="a23cf-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a23cf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a23cf-120">Requirements</span></span>



| <span data-ttu-id="a23cf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a23cf-121">Requirement</span></span> | <span data-ttu-id="a23cf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a23cf-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a23cf-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a23cf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a23cf-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a23cf-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a23cf-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a23cf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a23cf-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a23cf-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





