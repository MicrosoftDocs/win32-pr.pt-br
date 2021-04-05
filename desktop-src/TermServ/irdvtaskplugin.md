---
title: Interface IRDVTaskPlugin
description: A interface IRDVTaskPlugin é implementada por um agente de tarefa de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota da interface IRDVTaskPlugin, descrita
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919134"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="83dc6-105">Interface IRDVTaskPlugin</span><span class="sxs-lookup"><span data-stu-id="83dc6-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="83dc6-106">A interface **IRDVTaskPlugin** é implementada por um agente de *tarefa* de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83dc6-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="83dc6-107">Essa interface é usada pelo *agente de gatilho*, que é implementado pelo sistema host.</span><span class="sxs-lookup"><span data-stu-id="83dc6-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="83dc6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="83dc6-108">Members</span></span>

<span data-ttu-id="83dc6-109">A interface **IRDVTaskPlugin** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="83dc6-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="83dc6-110">**IRDVTaskPlugin** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83dc6-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="83dc6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="83dc6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="83dc6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83dc6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83dc6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="83dc6-113">Methods</span></span>

<span data-ttu-id="83dc6-114">A interface **IRDVTaskPlugin** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="83dc6-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="83dc6-115">Método</span><span class="sxs-lookup"><span data-stu-id="83dc6-115">Method</span></span>                                          | <span data-ttu-id="83dc6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="83dc6-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="83dc6-117">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="83dc6-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="83dc6-118">Chamado para inicializar o agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="83dc6-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="83dc6-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="83dc6-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="83dc6-120">Chamado para iniciar a tarefa de atualização na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83dc6-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="83dc6-121">**Encerrar**</span><span class="sxs-lookup"><span data-stu-id="83dc6-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="83dc6-122">Chamado quando o agente de tarefa está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="83dc6-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="83dc6-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83dc6-123">Properties</span></span>

<span data-ttu-id="83dc6-124">A interface **IRDVTaskPlugin** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="83dc6-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="83dc6-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="83dc6-125">Property</span></span>                                                   | <span data-ttu-id="83dc6-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="83dc6-126">Access type</span></span>          | <span data-ttu-id="83dc6-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="83dc6-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="83dc6-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="83dc6-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="83dc6-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83dc6-129">Read-only</span></span><br/> | <span data-ttu-id="83dc6-130">Contém o nome de exibição do agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="83dc6-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83dc6-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="83dc6-131">Remarks</span></span>

<span data-ttu-id="83dc6-132">O agente de tarefa é executado na máquina virtual quando essa máquina virtual está agendada para uma atualização do sistema.</span><span class="sxs-lookup"><span data-stu-id="83dc6-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="83dc6-133">O agente de tarefa atualiza a máquina virtual quando o método [**StartTask**](irdvtaskplugin-starttask.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="83dc6-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="83dc6-134">Para registrar o agente de tarefa, adicione a seguinte chave ao registro da máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="83dc6-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="83dc6-135">**HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ plugins da **tarefa** \\  \\ **TaskAgentName**</span><span class="sxs-lookup"><span data-stu-id="83dc6-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="83dc6-136">Nessa chave do registro, adicione os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="83dc6-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="83dc6-137">Nome</span><span class="sxs-lookup"><span data-stu-id="83dc6-137">Name</span></span>                     | <span data-ttu-id="83dc6-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="83dc6-138">Type</span></span>                      | <span data-ttu-id="83dc6-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="83dc6-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="83dc6-140">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="83dc6-140">**CLSID**</span></span><br/>     | <span data-ttu-id="83dc6-141">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="83dc6-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="83dc6-142">Uma cadeia de caracteres que representa o **CLSID** do agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="83dc6-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="83dc6-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="83dc6-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="83dc6-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="83dc6-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="83dc6-145">0 se o agente de tarefa estiver desabilitado ou 1 se o agente de tarefa estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="83dc6-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="83dc6-146">Mais de um agente de tarefa pode ser registrado, mas apenas um agente de tarefa será usado.</span><span class="sxs-lookup"><span data-stu-id="83dc6-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="83dc6-147">Se mais de um agente de tarefa estiver habilitado, somente o primeiro encontrado será usado.</span><span class="sxs-lookup"><span data-stu-id="83dc6-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="83dc6-148">Embora essa interface tenha suporte nos sistemas operacionais identificados nos requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="83dc6-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="83dc6-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83dc6-149">Requirements</span></span>



| <span data-ttu-id="83dc6-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="83dc6-150">Requirement</span></span> | <span data-ttu-id="83dc6-151">Valor</span><span class="sxs-lookup"><span data-stu-id="83dc6-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="83dc6-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83dc6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="83dc6-153">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="83dc6-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="83dc6-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83dc6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="83dc6-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83dc6-155">Windows Server 2008 R2</span></span><br/> |



 

