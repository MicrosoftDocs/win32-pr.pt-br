---
title: Elemento ID (networkSettingsType)
description: Contém um valor de GUID que identifica um perfil de rede.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento de ID Agendador de Tarefas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086452"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="07017-104">Elemento ID (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="07017-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="07017-105">Contém um valor de GUID que identifica um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="07017-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="07017-106">O elemento **ID** é definido pelo tipo complexo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="07017-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="07017-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="07017-107">Parent element</span></span>



| <span data-ttu-id="07017-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="07017-108">Element</span></span>                                                                                            | <span data-ttu-id="07017-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="07017-109">Derived from</span></span>                                                                       | <span data-ttu-id="07017-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="07017-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07017-111">**NetworkSettings (settingstype)**</span><span class="sxs-lookup"><span data-stu-id="07017-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="07017-112">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="07017-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="07017-113">Contém as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="07017-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="07017-114">O serviço de Agendador de Tarefas verifica a disponibilidade dessa rede quando o elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="07017-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="07017-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07017-115">Remarks</span></span>

<span data-ttu-id="07017-116">Para desenvolvimento em C++, consulte a [**Propriedade ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="07017-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="07017-117">Para o desenvolvimento de scripts, consulte [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="07017-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07017-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07017-118">Requirements</span></span>



| <span data-ttu-id="07017-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07017-119">Requirement</span></span> | <span data-ttu-id="07017-120">Valor</span><span class="sxs-lookup"><span data-stu-id="07017-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07017-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07017-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07017-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07017-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07017-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07017-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07017-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07017-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





