---
title: Objeto NetworkSettings
description: Para scripts, o fornece as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Agendador de Tarefas de objeto NetworkSettings
- Agendador de Tarefas de objeto NetworkSettings, descrito
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455308"
---
# <a name="networksettings-object"></a><span data-ttu-id="34ed0-105">Objeto NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="34ed0-105">NetworkSettings object</span></span>

<span data-ttu-id="34ed0-106">Para scripts, o fornece as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="34ed0-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="34ed0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="34ed0-107">Members</span></span>

<span data-ttu-id="34ed0-108">O objeto **NetworkSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="34ed0-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="34ed0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34ed0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34ed0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34ed0-110">Properties</span></span>

<span data-ttu-id="34ed0-111">O objeto **NetworkSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="34ed0-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="34ed0-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="34ed0-112">Property</span></span>                                        | <span data-ttu-id="34ed0-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="34ed0-113">Access type</span></span>           | <span data-ttu-id="34ed0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="34ed0-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34ed0-115">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="34ed0-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="34ed0-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34ed0-116">Read/write</span></span><br/> | <span data-ttu-id="34ed0-117">Obtém ou define um valor de GUID que identifica um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="34ed0-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="34ed0-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="34ed0-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="34ed0-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34ed0-119">Read/write</span></span><br/> | <span data-ttu-id="34ed0-120">Obtém ou define o nome de um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="34ed0-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="34ed0-121">O nome é usado para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="34ed0-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="34ed0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="34ed0-122">Remarks</span></span>

<span data-ttu-id="34ed0-123">Ao ler ou gravar seu próprio XML para uma tarefa, as configurações de rede são especificadas usando o elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="34ed0-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ed0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34ed0-124">Requirements</span></span>



| <span data-ttu-id="34ed0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ed0-125">Requirement</span></span> | <span data-ttu-id="34ed0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="34ed0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34ed0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34ed0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="34ed0-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34ed0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="34ed0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34ed0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="34ed0-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34ed0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34ed0-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="34ed0-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="34ed0-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34ed0-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34ed0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="34ed0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34ed0-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34ed0-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34ed0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="34ed0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ed0-136">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="34ed0-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="34ed0-137">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="34ed0-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





