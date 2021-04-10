---
title: Interfaces de virtualização Área de Trabalho Remota
description: A API de virtualização Área de Trabalho Remota dá suporte às seguintes interfaces.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294261"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="56c9d-103">Interfaces de virtualização Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="56c9d-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="56c9d-104">A API de virtualização Área de Trabalho Remota dá suporte às seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="56c9d-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="56c9d-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="56c9d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="56c9d-106">**ITsSbBaseNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-107">Expõe métodos que relatam status e mensagens de erro para Conexão de Área de Trabalho Remota Agente (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="56c9d-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-108">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="56c9d-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="56c9d-109">Expõe métodos e propriedades que armazenam informações de estado sobre uma solicitação de conexão de entrada de um cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="56c9d-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-110">**ITsSbClientConnectionPropertySet**</span><span class="sxs-lookup"><span data-stu-id="56c9d-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="56c9d-111">Pode ser usado para definir propriedades personalizadas de uma conexão de cliente conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-112">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="56c9d-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="56c9d-113">Expõe métodos e propriedades que contêm informações sobre o ambiente que hospeda o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="56c9d-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="56c9d-114">Essa interface pode ser usada para armazenar informações sobre um servidor físico que hospeda máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56c9d-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-115">**ITsSbEnvironmentPropertySet**</span><span class="sxs-lookup"><span data-stu-id="56c9d-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="56c9d-116">Pode ser usado para definir propriedades personalizadas de um ambiente que hospeda computadores de destino conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-117">**ITsSbFilterPluginStore**</span><span class="sxs-lookup"><span data-stu-id="56c9d-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="56c9d-118">Filtrar repositório de plug-in</span><span class="sxs-lookup"><span data-stu-id="56c9d-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-119">**ITsSbGenericNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-120">Expõe métodos que relatam a conclusão e recebem o tempo de espera do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="56c9d-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-121">**ITsSbGlobalStore**</span><span class="sxs-lookup"><span data-stu-id="56c9d-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="56c9d-122">Expõe métodos que consultam computadores de destino, sessões, ambientes e farms que foram adicionados ao armazenamento do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="56c9d-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-123">**ITsSbLoadBalanceResult**</span><span class="sxs-lookup"><span data-stu-id="56c9d-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="56c9d-124">Expõe métodos e propriedades que armazenam o nome de destino retornado por um algoritmo de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="56c9d-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-125">**ITsSbLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="56c9d-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="56c9d-126">Expõe métodos que você pode usar para fornecer um algoritmo de balanceamento de carga personalizado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-127">**ITsSbLoadBalancingNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-128">Expõe métodos que retornam o resultado de um algoritmo de balanceamento de carga para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="56c9d-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-129">**ITsSbOrchestration**</span><span class="sxs-lookup"><span data-stu-id="56c9d-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="56c9d-130">Expõe os métodos que o agente de conexão RD usa para garantir que o destino esteja pronto antes que um cliente seja redirecionado para ele.</span><span class="sxs-lookup"><span data-stu-id="56c9d-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-131">**ITsSbOrchestrationNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-132">Expõe métodos que retornam um objeto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) para o agente de conexão RD depois que o destino é preparado com êxito para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="56c9d-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-133">**ITsSbPlacement**</span><span class="sxs-lookup"><span data-stu-id="56c9d-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="56c9d-134">Expõe métodos que preparam o ambiente (o computador que hospeda a máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="56c9d-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-135">**ITsSbPlacementNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-136">Expõe métodos que retornam informações sobre ambientes para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="56c9d-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-137">**ITsSbPlugin**</span><span class="sxs-lookup"><span data-stu-id="56c9d-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="56c9d-138">Expõe métodos que inicializam e encerram plug-ins.</span><span class="sxs-lookup"><span data-stu-id="56c9d-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-139">**ITsSbPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-140">Expõe métodos que notificam o agente de conexão RD sobre a inicialização ou o encerramento de um plug-in.</span><span class="sxs-lookup"><span data-stu-id="56c9d-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-141">**ITsSbPluginPropertySet**</span><span class="sxs-lookup"><span data-stu-id="56c9d-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="56c9d-142">Pode ser usado para definir propriedades de plug-in personalizadas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-143">**ITsSbPropertySet**</span><span class="sxs-lookup"><span data-stu-id="56c9d-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="56c9d-144">Pode ser usado para definir propriedades personalizadas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-145">**ITsSbProvider**</span><span class="sxs-lookup"><span data-stu-id="56c9d-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="56c9d-146">Expõe métodos que criam implementações padrão de objetos que são usados na virtualização Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="56c9d-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-147">**ITsSbProvisioning**</span><span class="sxs-lookup"><span data-stu-id="56c9d-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="56c9d-148">Expõe métodos que criam e mantêm máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56c9d-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-149">**ITsSbProvisioningPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-150">Expõe métodos que notificam o agente de conexão RD sobre o provisionamento de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56c9d-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-151">**ITsSbResourceNotification**</span><span class="sxs-lookup"><span data-stu-id="56c9d-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="56c9d-152">Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de qualquer alteração de estado que ocorra nos objetos de conexão de sessão, destino e cliente.</span><span class="sxs-lookup"><span data-stu-id="56c9d-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-153">**ITsSbResourceNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="56c9d-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="56c9d-154">Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de qualquer alteração de estado que ocorra nos objetos de conexão de sessão, destino e cliente.</span><span class="sxs-lookup"><span data-stu-id="56c9d-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-155">**ITsSbResourcePlugin**</span><span class="sxs-lookup"><span data-stu-id="56c9d-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="56c9d-156">Expõe métodos que estendem os recursos do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="56c9d-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-157">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="56c9d-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="56c9d-158">Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.</span><span class="sxs-lookup"><span data-stu-id="56c9d-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-159">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="56c9d-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="56c9d-160">Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.</span><span class="sxs-lookup"><span data-stu-id="56c9d-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-161">**ITsSbServiceNotification**</span><span class="sxs-lookup"><span data-stu-id="56c9d-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="56c9d-162">Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de alterações de estado que ocorrem no próprio agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="56c9d-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-163">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="56c9d-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="56c9d-164">Expõe propriedades que armazenam informações sobre uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="56c9d-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-165">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="56c9d-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="56c9d-166">Expõe propriedades que armazenam informações de configuração e estado sobre um destino.</span><span class="sxs-lookup"><span data-stu-id="56c9d-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-167">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="56c9d-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="56c9d-168">Expõe propriedades que armazenam informações de configuração e estado sobre um destino.</span><span class="sxs-lookup"><span data-stu-id="56c9d-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-169">**ITsSbTargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="56c9d-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="56c9d-170">Derive desta interface para definir um conjunto de propriedades de destino personalizado.</span><span class="sxs-lookup"><span data-stu-id="56c9d-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-171">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="56c9d-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="56c9d-172">Expõe as propriedades que o agente de Conexão de Área de Trabalho Remota usa para definir a fila de um plug-in.</span><span class="sxs-lookup"><span data-stu-id="56c9d-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-173">**ITsSbTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="56c9d-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="56c9d-174">Expõe métodos que atualizam a fila de tarefas para plug-ins do Conexão de Área de Trabalho Remota Broker.</span><span class="sxs-lookup"><span data-stu-id="56c9d-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-175">**ITsSbTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="56c9d-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="56c9d-176">Expõe métodos que relatam status e mensagens de erro sobre tarefas para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="56c9d-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="56c9d-177">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="56c9d-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="56c9d-178">Usado para estender os recursos do agente de sessão de serviços de terminal (agente de Sessão TS).</span><span class="sxs-lookup"><span data-stu-id="56c9d-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="56c9d-179">Implemente essa interface quando desejar fornecer um plug-in que substitua a lógica de redirecionamento do agente de Sessão TS.</span><span class="sxs-lookup"><span data-stu-id="56c9d-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 