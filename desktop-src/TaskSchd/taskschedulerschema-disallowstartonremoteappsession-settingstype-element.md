---
title: Elemento DisallowStartOnRemoteAppSession (settingstype)
description: Especifica que a tarefa não será iniciada se for disparada para execução em uma sessão integrada de aplicativos remotos (trilho).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Agendador de Tarefas do elemento DisallowStartOnRemoteAppSession
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796307"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="7c65a-104">Elemento DisallowStartOnRemoteAppSession (settingstype)</span><span class="sxs-lookup"><span data-stu-id="7c65a-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="7c65a-105">Especifica que a tarefa não será iniciada se for disparada para execução em uma sessão integrada de aplicativos remotos (trilho).</span><span class="sxs-lookup"><span data-stu-id="7c65a-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="7c65a-106">O elemento **DisallowStartOnRemoteAppSession** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7c65a-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7c65a-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="7c65a-107">Parent element</span></span>



| <span data-ttu-id="7c65a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7c65a-108">Element</span></span>                                                           | <span data-ttu-id="7c65a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7c65a-109">Derived from</span></span>                                                         | <span data-ttu-id="7c65a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c65a-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c65a-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="7c65a-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="7c65a-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="7c65a-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="7c65a-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c65a-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7c65a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c65a-114">Remarks</span></span>

<span data-ttu-id="7c65a-115">A configuração padrão para esse elemento é false.</span><span class="sxs-lookup"><span data-stu-id="7c65a-115">The default setting for this element is False.</span></span>

<span data-ttu-id="7c65a-116">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .</span><span class="sxs-lookup"><span data-stu-id="7c65a-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="7c65a-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c65a-117">Examples</span></span>

<span data-ttu-id="7c65a-118">O XML a seguir define um elemento Settings que não permite que a tarefa seja iniciada se a tarefa for disparada para ser executada em uma sessão de trilho.</span><span class="sxs-lookup"><span data-stu-id="7c65a-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="7c65a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c65a-119">Requirements</span></span>



| <span data-ttu-id="7c65a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c65a-120">Requirement</span></span> | <span data-ttu-id="7c65a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7c65a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7c65a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c65a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c65a-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7c65a-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7c65a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c65a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c65a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7c65a-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c65a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c65a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c65a-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7c65a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





