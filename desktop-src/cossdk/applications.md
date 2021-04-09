---
description: Contém um objeto para cada aplicativo COM+ instalado no computador local. As propriedades expostas por esses objetos contêm todas as configurações feitas no nível do aplicativo.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Coleção de aplicativos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089382"
---
# <a name="applications-collection"></a><span data-ttu-id="6c31c-104">Coleção de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6c31c-104">Applications collection</span></span>

<span data-ttu-id="6c31c-105">Contém um objeto para cada aplicativo COM+ instalado no computador local.</span><span class="sxs-lookup"><span data-stu-id="6c31c-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="6c31c-106">As propriedades expostas por esses objetos contêm todas as configurações feitas no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="6c31c-107">Defina as propriedades dos componentes em um aplicativo usando a coleção de [**componentes**](components.md) relacionados.</span><span class="sxs-lookup"><span data-stu-id="6c31c-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="6c31c-108">Você atribui funções a um aplicativo usando a coleção de [**funções**](roles.md) relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="6c31c-109">Para instalar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="6c31c-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="6c31c-110">Para instalar um aplicativo de um arquivo ou desligar ou exportar um aplicativo, use também métodos no objeto **COMAdminCatalog** .</span><span class="sxs-lookup"><span data-stu-id="6c31c-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="6c31c-111">Caso contrário, para criar um novo aplicativo, você pode adicionar um objeto à coleção de **aplicativos** .</span><span class="sxs-lookup"><span data-stu-id="6c31c-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="6c31c-112">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6c31c-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6c31c-113">Membros</span><span class="sxs-lookup"><span data-stu-id="6c31c-113">Members</span></span>

<span data-ttu-id="6c31c-114">A coleção de **aplicativos** é herdada da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="6c31c-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6c31c-115">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="6c31c-115">Related Collections</span></span>

<span data-ttu-id="6c31c-116">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="6c31c-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6c31c-117">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="6c31c-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="6c31c-118">**Componentes**</span><span class="sxs-lookup"><span data-stu-id="6c31c-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="6c31c-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6c31c-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6c31c-120">**LegacyComponents**</span><span class="sxs-lookup"><span data-stu-id="6c31c-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="6c31c-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6c31c-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6c31c-122">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="6c31c-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="6c31c-123">**Funções**</span><span class="sxs-lookup"><span data-stu-id="6c31c-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="6c31c-124">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="6c31c-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6c31c-125">**Partições**</span><span class="sxs-lookup"><span data-stu-id="6c31c-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="6c31c-126">**Básica**</span><span class="sxs-lookup"><span data-stu-id="6c31c-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="6c31c-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c31c-127">Properties</span></span>

<span data-ttu-id="6c31c-128">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="6c31c-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6c31c-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="6c31c-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="6c31c-131">Ativação</span><span class="sxs-lookup"><span data-stu-id="6c31c-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="6c31c-132">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="6c31c-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="6c31c-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="6c31c-134">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="6c31c-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="6c31c-135">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="6c31c-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="6c31c-136">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="6c31c-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="6c31c-137">Autenticação</span><span class="sxs-lookup"><span data-stu-id="6c31c-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="6c31c-138">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="6c31c-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="6c31c-139">Mutável</span><span class="sxs-lookup"><span data-stu-id="6c31c-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="6c31c-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="6c31c-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="6c31c-141">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="6c31c-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="6c31c-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="6c31c-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="6c31c-143">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="6c31c-144">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="6c31c-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="6c31c-145">Pode ser excluído</span><span class="sxs-lookup"><span data-stu-id="6c31c-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="6c31c-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-146">Description</span></span>](#description)
-   [<span data-ttu-id="6c31c-147">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="6c31c-148">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="6c31c-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="6c31c-149">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="6c31c-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="6c31c-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="6c31c-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="6c31c-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="6c31c-152">ID</span><span class="sxs-lookup"><span data-stu-id="6c31c-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="6c31c-153">Identidade</span><span class="sxs-lookup"><span data-stu-id="6c31c-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="6c31c-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="6c31c-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="6c31c-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="6c31c-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="6c31c-157">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="6c31c-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="6c31c-158">Nome</span><span class="sxs-lookup"><span data-stu-id="6c31c-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="6c31c-159">Senha</span><span class="sxs-lookup"><span data-stu-id="6c31c-159">Password</span></span>](#password)
-   [<span data-ttu-id="6c31c-160">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="6c31c-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="6c31c-161">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="6c31c-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="6c31c-162">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="6c31c-163">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="6c31c-164">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="6c31c-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="6c31c-166">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="6c31c-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="6c31c-167">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="6c31c-168">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="6c31c-169">Replicáveis</span><span class="sxs-lookup"><span data-stu-id="6c31c-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="6c31c-170">RunForever</span><span class="sxs-lookup"><span data-stu-id="6c31c-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="6c31c-171">ServiceName</span><span class="sxs-lookup"><span data-stu-id="6c31c-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="6c31c-172">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="6c31c-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="6c31c-173">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="6c31c-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="6c31c-174">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="6c31c-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="6c31c-175">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="6c31c-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="6c31c-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="6c31c-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="6c31c-177">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="6c31c-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="6c31c-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="6c31c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-180">Entry</span></span> | <span data-ttu-id="6c31c-181">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-182">Description</span></span>    | <span data-ttu-id="6c31c-183">Indica se o aplicativo pode usar 3 GB de memória em seu processo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="6c31c-184">Se isso não estiver habilitado, o aplicativo poderá usar apenas 2 GB de memória.</span><span class="sxs-lookup"><span data-stu-id="6c31c-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="6c31c-185">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-185">Access</span></span>         | <span data-ttu-id="6c31c-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="6c31c-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-187">Type</span></span>           | <span data-ttu-id="6c31c-188">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="6c31c-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-189">Default</span></span>        | <span data-ttu-id="6c31c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="6c31c-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-191">Minimum system</span></span> | <span data-ttu-id="6c31c-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="6c31c-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-193">AccessChecksLevel</span></span>



| <span data-ttu-id="6c31c-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-194">Entry</span></span> | <span data-ttu-id="6c31c-195">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-196">Description</span></span>    | <span data-ttu-id="6c31c-197">Indica se as verificações de acesso são executadas apenas no nível do processo ou no nível do processo e do componente.</span><span class="sxs-lookup"><span data-stu-id="6c31c-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="6c31c-198">É recomendável que você use as constantes na enumeração e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="6c31c-199">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-199">Access</span></span>         | <span data-ttu-id="6c31c-200">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="6c31c-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-201">Type</span></span>           | <span data-ttu-id="6c31c-202">Valores longos possíveis: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="6c31c-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="6c31c-203">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-203">Default</span></span>        | <span data-ttu-id="6c31c-204">COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="6c31c-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="6c31c-205">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-205">Minimum system</span></span> | <span data-ttu-id="6c31c-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="6c31c-207">Ativação</span><span class="sxs-lookup"><span data-stu-id="6c31c-207">Activation</span></span>



| <span data-ttu-id="6c31c-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-208">Entry</span></span> | <span data-ttu-id="6c31c-209">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-210">Description</span></span>    | <span data-ttu-id="6c31c-211">A ativação local indica que os objetos dentro do aplicativo são executados dentro de um processo de servidor local dedicado (aplicativo de servidor).</span><span class="sxs-lookup"><span data-stu-id="6c31c-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="6c31c-212">A ativação em processo indica que os objetos são executados no processo do criador (aplicativo de biblioteca).</span><span class="sxs-lookup"><span data-stu-id="6c31c-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="6c31c-213">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-213">Access</span></span>         | <span data-ttu-id="6c31c-214">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="6c31c-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-215">Type</span></span>           | <span data-ttu-id="6c31c-216">Valores longos possíveis: COMAdminActivationInproc (0) COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="6c31c-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="6c31c-217">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-217">Default</span></span>        | <span data-ttu-id="6c31c-218">COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="6c31c-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="6c31c-219">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-219">Minimum system</span></span> | <span data-ttu-id="6c31c-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="6c31c-221">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="6c31c-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-222">Entry</span></span> | <span data-ttu-id="6c31c-223">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-224">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-224">Description</span></span>    | <span data-ttu-id="6c31c-225">Indica se as verificações de acesso são executadas para o aplicativo quando os clientes fazem chamadas para ele.</span><span class="sxs-lookup"><span data-stu-id="6c31c-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="6c31c-226">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-226">Access</span></span>         | <span data-ttu-id="6c31c-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="6c31c-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-228">Type</span></span>           | <span data-ttu-id="6c31c-229">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="6c31c-230">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-230">Default</span></span>        | <span data-ttu-id="6c31c-231">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-231">True</span></span>                                                                                               |
| <span data-ttu-id="6c31c-232">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-232">Minimum system</span></span> | <span data-ttu-id="6c31c-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="6c31c-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="6c31c-234">ApplicationDirectory</span></span>



| <span data-ttu-id="6c31c-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-235">Entry</span></span> | <span data-ttu-id="6c31c-236">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-237">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-237">Description</span></span>    | <span data-ttu-id="6c31c-238">O caminho completo para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-238">The full path to the application.</span></span> <span data-ttu-id="6c31c-239">Essas informações são necessárias quando você configura assemblies do SxS (lado a lado).</span><span class="sxs-lookup"><span data-stu-id="6c31c-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="6c31c-240">Os assemblies SxS (lado a lado permitem que os aplicativos ASP especifiquem qual versão de uma DLL de sistema com suporte do SxS usar, como MSVCRT, MSXML, COMCTL, GDIPLUS e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6c31c-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="6c31c-241">Por exemplo, se o aplicativo ASP depender da versão 2,0 do MSVCRT, você poderá garantir que seu aplicativo ainda use o MSVCRT versão 2,0 mesmo depois que os Service Packs forem aplicados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6c31c-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="6c31c-242">Qualquer nova versão do MSVCRT ainda está instalada no computador, mas a versão 2,0 permanece e é usada pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="6c31c-243">As DLLs com suporte a SxS são armazenadas em% WINDIR% \\ WinSxS.</span><span class="sxs-lookup"><span data-stu-id="6c31c-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="6c31c-244">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-244">Access</span></span>         | <span data-ttu-id="6c31c-245">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6c31c-246">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-246">Type</span></span>           | <span data-ttu-id="6c31c-247">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="6c31c-248">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-248">Default</span></span>        | <span data-ttu-id="6c31c-249">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6c31c-250">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-250">Minimum system</span></span> | <span data-ttu-id="6c31c-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="6c31c-252">Somente uma versão de uma DLL do sistema pode ser usada em qualquer pool de aplicativos, embora esse recurso seja configurável no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="6c31c-253">Por exemplo, se o aplicativo App1 usar o MSVCRT, a versão 2,5 e o aplicativo App2 usarem MSVCRT, versão 2,4, App1 e App2 não deverão estar no mesmo pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="6c31c-254">Se estiverem, o aplicativo que é carregado primeiro tem sua versão do MSVCRT carregada e o outro aplicativo é forçado a usá-lo até que os aplicativos sejam descarregados.</span><span class="sxs-lookup"><span data-stu-id="6c31c-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="6c31c-255">Para obter mais informações, consulte "assemblies lado a lado" em [alterações nos serviços com+ no IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="6c31c-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="6c31c-256">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="6c31c-256">ApplicationProxy</span></span>



| <span data-ttu-id="6c31c-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-257">Entry</span></span> | <span data-ttu-id="6c31c-258">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="6c31c-259">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-259">Description</span></span>    | <span data-ttu-id="6c31c-260">Indica se o aplicativo é um proxy de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="6c31c-261">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-261">Access</span></span>         | <span data-ttu-id="6c31c-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6c31c-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="6c31c-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-263">Type</span></span>           | <span data-ttu-id="6c31c-264">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-264">Bool</span></span>                                                       |
| <span data-ttu-id="6c31c-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-265">Default</span></span>        | <span data-ttu-id="6c31c-266">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-266">False</span></span>                                                      |
| <span data-ttu-id="6c31c-267">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-267">Minimum system</span></span> | <span data-ttu-id="6c31c-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="6c31c-269">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="6c31c-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="6c31c-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-270">Entry</span></span> | <span data-ttu-id="6c31c-271">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-272">Description</span></span>    | <span data-ttu-id="6c31c-273">Um nome de servidor remoto usado ao exportar o proxy de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="6c31c-274">É esse nome de servidor que o proxy de aplicativo aponta quando está instalado em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6c31c-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="6c31c-275">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-275">Access</span></span>         | <span data-ttu-id="6c31c-276">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="6c31c-277">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-277">Type</span></span>           | <span data-ttu-id="6c31c-278">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6c31c-279">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-279">Default</span></span>        | <span data-ttu-id="6c31c-280">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6c31c-281">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-281">Minimum system</span></span> | <span data-ttu-id="6c31c-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="6c31c-283">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="6c31c-283">AppPartitionID</span></span>



| <span data-ttu-id="6c31c-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-284">Entry</span></span> | <span data-ttu-id="6c31c-285">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="6c31c-286">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-286">Description</span></span>    | <span data-ttu-id="6c31c-287">Um GUID que representa a ID da partição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="6c31c-288">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-288">Access</span></span>         | <span data-ttu-id="6c31c-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6c31c-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="6c31c-290">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-290">Type</span></span>           | <span data-ttu-id="6c31c-291">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-291">String</span></span>                                            |
| <span data-ttu-id="6c31c-292">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="6c31c-293">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-293">Minimum system</span></span> | <span data-ttu-id="6c31c-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c31c-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="6c31c-295">Autenticação</span><span class="sxs-lookup"><span data-stu-id="6c31c-295">Authentication</span></span>



| <span data-ttu-id="6c31c-296">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-296">Entry</span></span> | <span data-ttu-id="6c31c-297">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-298">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-298">Description</span></span>    | <span data-ttu-id="6c31c-299">Define o nível de autenticação para chamadas, com valores correspondentes às configurações de autenticação RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="6c31c-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="6c31c-300">Quando COMAdminAuthenticationDefault é escolhido, a configuração na propriedade DefaultAuthenticationLevel dentro da coleção [**LocalComputer**](localcomputer.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="6c31c-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="6c31c-301">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-301">Access</span></span>         | <span data-ttu-id="6c31c-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6c31c-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-303">Type</span></span>           | <span data-ttu-id="6c31c-304">Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="6c31c-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="6c31c-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-305">Default</span></span>        | <span data-ttu-id="6c31c-306">COMAdminAuthenticationPacket (4)</span><span class="sxs-lookup"><span data-stu-id="6c31c-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6c31c-307">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-307">Minimum system</span></span> | <span data-ttu-id="6c31c-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="6c31c-309">Para aplicativos de biblioteca (em processo), as únicas configurações válidas aqui são COMAdminAuthenticationDefault e COMAdminAuthenticationNone.</span><span class="sxs-lookup"><span data-stu-id="6c31c-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="6c31c-310">É recomendável que você use as constantes na enumeração e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="6c31c-311">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="6c31c-311">AuthenticationCapability</span></span>



| <span data-ttu-id="6c31c-312">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-312">Entry</span></span> | <span data-ttu-id="6c31c-313">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-314">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-314">Description</span></span>    | <span data-ttu-id="6c31c-315">Determina qual identidade é apresentada quando as chamadas são representadas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6c31c-316">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-316">Access</span></span>         | <span data-ttu-id="6c31c-317">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="6c31c-318">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-318">Type</span></span>           | <span data-ttu-id="6c31c-319">Valores longos possíveis: COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="6c31c-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="6c31c-320">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-320">Default</span></span>        | <span data-ttu-id="6c31c-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="6c31c-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="6c31c-322">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-322">Minimum system</span></span> | <span data-ttu-id="6c31c-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="6c31c-324">Mutável</span><span class="sxs-lookup"><span data-stu-id="6c31c-324">Changeable</span></span>



| <span data-ttu-id="6c31c-325">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-325">Entry</span></span> | <span data-ttu-id="6c31c-326">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-327">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-327">Description</span></span>    | <span data-ttu-id="6c31c-328">Determina se as alterações nas configurações do aplicativo ou de seus componentes são permitidas, seja por meio de programação ou por meio da ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="6c31c-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="6c31c-329">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-329">Access</span></span>         | <span data-ttu-id="6c31c-330">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6c31c-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-331">Type</span></span>           | <span data-ttu-id="6c31c-332">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="6c31c-333">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-333">Default</span></span>        | <span data-ttu-id="6c31c-334">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="6c31c-335">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-335">Minimum system</span></span> | <span data-ttu-id="6c31c-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="6c31c-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="6c31c-337">CommandLine</span></span>



| <span data-ttu-id="6c31c-338">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-338">Entry</span></span> | <span data-ttu-id="6c31c-339">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-340">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-340">Description</span></span>    | <span data-ttu-id="6c31c-341">Uma cadeia de caracteres de linha de comando para uso na depuração.</span><span class="sxs-lookup"><span data-stu-id="6c31c-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="6c31c-342">O aplicativo pode ser iniciado em um depurador com a linha de comando especificada.</span><span class="sxs-lookup"><span data-stu-id="6c31c-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="6c31c-343">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-343">Access</span></span>         | <span data-ttu-id="6c31c-344">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="6c31c-345">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-345">Type</span></span>           | <span data-ttu-id="6c31c-346">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="6c31c-347">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-347">Default</span></span>        | <span data-ttu-id="6c31c-348">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="6c31c-349">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-349">Minimum system</span></span> | <span data-ttu-id="6c31c-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="6c31c-351">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="6c31c-351">ConcurrentApps</span></span>



| <span data-ttu-id="6c31c-352">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-352">Entry</span></span> | <span data-ttu-id="6c31c-353">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-354">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-354">Description</span></span>    | <span data-ttu-id="6c31c-355">Especifica o número máximo de aplicativos em pool que podem ser executados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6c31c-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="6c31c-356">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-356">Access</span></span>         | <span data-ttu-id="6c31c-357">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="6c31c-358">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-358">Type</span></span>           | <span data-ttu-id="6c31c-359">Longo (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="6c31c-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="6c31c-360">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-360">Default</span></span>        | <span data-ttu-id="6c31c-361">1</span><span class="sxs-lookup"><span data-stu-id="6c31c-361">1</span></span>                                                                                |
| <span data-ttu-id="6c31c-362">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-362">Minimum system</span></span> | <span data-ttu-id="6c31c-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="6c31c-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="6c31c-364">CreatedBy</span></span>



| <span data-ttu-id="6c31c-365">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-365">Entry</span></span> | <span data-ttu-id="6c31c-366">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="6c31c-367">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-367">Description</span></span>    | <span data-ttu-id="6c31c-368">Cadeia de caracteres informativa para descrever quem criou o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="6c31c-369">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-369">Access</span></span>         | <span data-ttu-id="6c31c-370">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="6c31c-371">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-371">Type</span></span>           | <span data-ttu-id="6c31c-372">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-372">String</span></span>                                                        |
| <span data-ttu-id="6c31c-373">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-373">Default</span></span>        | <span data-ttu-id="6c31c-374">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-374">""</span></span>                                                            |
| <span data-ttu-id="6c31c-375">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-375">Minimum system</span></span> | <span data-ttu-id="6c31c-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="6c31c-377">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-377">CRMEnabled</span></span>



| <span data-ttu-id="6c31c-378">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-378">Entry</span></span> | <span data-ttu-id="6c31c-379">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="6c31c-380">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-380">Description</span></span>    | <span data-ttu-id="6c31c-381">Determina se o Gerenciador de recursos de compensação está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="6c31c-382">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-382">Access</span></span>         | <span data-ttu-id="6c31c-383">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="6c31c-384">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-384">Type</span></span>           | <span data-ttu-id="6c31c-385">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-385">Bool</span></span>                                                             |
| <span data-ttu-id="6c31c-386">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-386">Default</span></span>        | <span data-ttu-id="6c31c-387">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-387">False</span></span>                                                            |
| <span data-ttu-id="6c31c-388">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-388">Minimum system</span></span> | <span data-ttu-id="6c31c-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="6c31c-390">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="6c31c-390">CRMLogFile</span></span>



| <span data-ttu-id="6c31c-391">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-391">Entry</span></span> | <span data-ttu-id="6c31c-392">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-393">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-393">Description</span></span>    | <span data-ttu-id="6c31c-394">Nome e caminho do arquivo para manter o log do Gerenciador de recursos de compensação (CRM).</span><span class="sxs-lookup"><span data-stu-id="6c31c-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="6c31c-395">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-395">Access</span></span>         | <span data-ttu-id="6c31c-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="6c31c-397">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-397">Type</span></span>           | <span data-ttu-id="6c31c-398">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-398">String</span></span>                                                                                 |
| <span data-ttu-id="6c31c-399">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-399">Default</span></span>        | <span data-ttu-id="6c31c-400">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-400">""</span></span>                                                                                     |
| <span data-ttu-id="6c31c-401">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-401">Minimum system</span></span> | <span data-ttu-id="6c31c-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="6c31c-403">Pode ser excluído</span><span class="sxs-lookup"><span data-stu-id="6c31c-403">Deleteable</span></span>



| <span data-ttu-id="6c31c-404">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-404">Entry</span></span> | <span data-ttu-id="6c31c-405">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-406">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-406">Description</span></span>    | <span data-ttu-id="6c31c-407">Define se o aplicativo pode ser excluído, seja por meio de programação ou por meio da ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="6c31c-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="6c31c-408">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-408">Access</span></span>         | <span data-ttu-id="6c31c-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="6c31c-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-410">Type</span></span>           | <span data-ttu-id="6c31c-411">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="6c31c-412">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-412">Default</span></span>        | <span data-ttu-id="6c31c-413">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="6c31c-414">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-414">Minimum system</span></span> | <span data-ttu-id="6c31c-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="6c31c-416">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-416">Description</span></span>



| <span data-ttu-id="6c31c-417">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-417">Entry</span></span> | <span data-ttu-id="6c31c-418">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="6c31c-419">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-419">Description</span></span>    | <span data-ttu-id="6c31c-420">Descreve o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-420">Describes the application.</span></span> |
| <span data-ttu-id="6c31c-421">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-421">Access</span></span>         | <span data-ttu-id="6c31c-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-422">ReadWrite</span></span>                  |
| <span data-ttu-id="6c31c-423">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-423">Type</span></span>           | <span data-ttu-id="6c31c-424">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-424">String</span></span>                     |
| <span data-ttu-id="6c31c-425">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-425">Default</span></span>        | <span data-ttu-id="6c31c-426">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-426">""</span></span>                         |
| <span data-ttu-id="6c31c-427">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-427">Minimum system</span></span> | <span data-ttu-id="6c31c-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="6c31c-429">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-429">DumpEnabled</span></span>



| <span data-ttu-id="6c31c-430">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-430">Entry</span></span> | <span data-ttu-id="6c31c-431">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-432">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-432">Description</span></span>    | <span data-ttu-id="6c31c-433">Habilita o despejo do estado de um aplicativo COM+ no momento da falha em um diretório designado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="6c31c-434">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-434">Access</span></span>         | <span data-ttu-id="6c31c-435">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="6c31c-436">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-436">Type</span></span>           | <span data-ttu-id="6c31c-437">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="6c31c-438">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-438">Default</span></span>        | <span data-ttu-id="6c31c-439">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-439">False</span></span>                                                                                                 |
| <span data-ttu-id="6c31c-440">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-440">Minimum system</span></span> | <span data-ttu-id="6c31c-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="6c31c-442">A partir do Windows Server 2003, somente os administradores têm privilégios de acesso de leitura aos arquivos de despejo COM+.</span><span class="sxs-lookup"><span data-stu-id="6c31c-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="6c31c-443">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="6c31c-443">DumpOnException</span></span>



| <span data-ttu-id="6c31c-444">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-444">Entry</span></span> | <span data-ttu-id="6c31c-445">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-446">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-446">Description</span></span>    | <span data-ttu-id="6c31c-447">Habilita o despejo do estado de um aplicativo COM+ quando o aplicativo causa uma exceção sem tratamento e é encerrado pelo tempo de execução do COM+.</span><span class="sxs-lookup"><span data-stu-id="6c31c-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="6c31c-448">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-448">Access</span></span>         | <span data-ttu-id="6c31c-449">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="6c31c-450">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-450">Type</span></span>           | <span data-ttu-id="6c31c-451">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="6c31c-452">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-452">Default</span></span>        | <span data-ttu-id="6c31c-453">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="6c31c-454">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-454">Minimum system</span></span> | <span data-ttu-id="6c31c-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="6c31c-456">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="6c31c-456">DumpOnFailfast</span></span>



| <span data-ttu-id="6c31c-457">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-457">Entry</span></span> | <span data-ttu-id="6c31c-458">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-459">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-459">Description</span></span>    | <span data-ttu-id="6c31c-460">Habilita o despejo do estado de um aplicativo COM+ quando o aplicativo falha.</span><span class="sxs-lookup"><span data-stu-id="6c31c-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="6c31c-461">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-461">Access</span></span>         | <span data-ttu-id="6c31c-462">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="6c31c-463">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-463">Type</span></span>           | <span data-ttu-id="6c31c-464">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-464">Bool</span></span>                                                                            |
| <span data-ttu-id="6c31c-465">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-465">Default</span></span>        | <span data-ttu-id="6c31c-466">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-466">False</span></span>                                                                           |
| <span data-ttu-id="6c31c-467">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-467">Minimum system</span></span> | <span data-ttu-id="6c31c-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="6c31c-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="6c31c-469">DumpPath</span></span>



| <span data-ttu-id="6c31c-470">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-470">Entry</span></span> | <span data-ttu-id="6c31c-471">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="6c31c-472">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-472">Description</span></span>    | <span data-ttu-id="6c31c-473">O caminho do diretório no qual os arquivos de despejo são salvos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="6c31c-474">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-474">Access</span></span>         | <span data-ttu-id="6c31c-475">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="6c31c-476">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-476">Type</span></span>           | <span data-ttu-id="6c31c-477">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-477">String</span></span>                                                       |
| <span data-ttu-id="6c31c-478">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-478">Default</span></span>        | <span data-ttu-id="6c31c-479">"% SystemRoot% \\ System32 \\ com \\ DMP"</span><span class="sxs-lookup"><span data-stu-id="6c31c-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="6c31c-480">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-480">Minimum system</span></span> | <span data-ttu-id="6c31c-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="6c31c-482">A partir do Windows Server 2003, somente os administradores têm privilégios de acesso de leitura aos arquivos de despejo COM+.</span><span class="sxs-lookup"><span data-stu-id="6c31c-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="6c31c-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-483">EventsEnabled</span></span>



| <span data-ttu-id="6c31c-484">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-484">Entry</span></span> | <span data-ttu-id="6c31c-485">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="6c31c-486">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-486">Description</span></span>    | <span data-ttu-id="6c31c-487">Indica se os eventos estão habilitados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="6c31c-488">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-488">Access</span></span>         | <span data-ttu-id="6c31c-489">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="6c31c-490">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-490">Type</span></span>           | <span data-ttu-id="6c31c-491">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-491">Bool</span></span>                                                      |
| <span data-ttu-id="6c31c-492">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-492">Default</span></span>        | <span data-ttu-id="6c31c-493">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-493">True</span></span>                                                      |
| <span data-ttu-id="6c31c-494">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-494">Minimum system</span></span> | <span data-ttu-id="6c31c-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="6c31c-496">ID</span><span class="sxs-lookup"><span data-stu-id="6c31c-496">ID</span></span>



| <span data-ttu-id="6c31c-497">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-497">Entry</span></span> | <span data-ttu-id="6c31c-498">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-499">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-499">Description</span></span>    | <span data-ttu-id="6c31c-500">Um GUID que representa o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-500">A GUID representing the application.</span></span> <span data-ttu-id="6c31c-501">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="6c31c-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6c31c-502">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-502">Access</span></span>         | <span data-ttu-id="6c31c-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="6c31c-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="6c31c-504">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-504">Type</span></span>           | <span data-ttu-id="6c31c-505">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="6c31c-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="6c31c-507">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-507">Minimum system</span></span> | <span data-ttu-id="6c31c-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="6c31c-509">Identidade</span><span class="sxs-lookup"><span data-stu-id="6c31c-509">Identity</span></span>



| <span data-ttu-id="6c31c-510">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-510">Entry</span></span> | <span data-ttu-id="6c31c-511">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-512">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-512">Description</span></span>    | <span data-ttu-id="6c31c-513">Define a identidade do processo do servidor para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="6c31c-514">Especifique uma conta de usuário válida ou "usuário interativo" para que o aplicativo assuma a identidade do usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="6c31c-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="6c31c-515">Você também pode especificar as cadeias de caracteres "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System".</span><span class="sxs-lookup"><span data-stu-id="6c31c-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="6c31c-516">A senha padrão para essas três contas é "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="6c31c-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="6c31c-517">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-518">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-519">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-520">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-520">Minimum system</span></span> | <span data-ttu-id="6c31c-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="6c31c-522">A propriedade Identity não está habilitada para aplicativos de biblioteca, que são executados no processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="6c31c-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="6c31c-523">A propriedade password deve ser definida ao mesmo tempo que a identidade, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="6c31c-524">Se a senha e a identidade forem obtidas fora de sincronia, o aplicativo não poderá ser iniciado até que ele seja redefinido por um administrador.</span><span class="sxs-lookup"><span data-stu-id="6c31c-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="6c31c-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-525">ImpersonationLevel</span></span>



| <span data-ttu-id="6c31c-526">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-526">Entry</span></span> | <span data-ttu-id="6c31c-527">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-528">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-528">Description</span></span>    | <span data-ttu-id="6c31c-529">Define o nível de representação usado para chamadas feitas a outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="6c31c-530">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-530">Access</span></span>         | <span data-ttu-id="6c31c-531">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="6c31c-532">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-532">Type</span></span>           | <span data-ttu-id="6c31c-533">Valores longos possíveis: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="6c31c-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="6c31c-534">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-534">Default</span></span>        | <span data-ttu-id="6c31c-535">COMAdminImpersonationImpersonate (3)</span><span class="sxs-lookup"><span data-stu-id="6c31c-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="6c31c-536">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-536">Minimum system</span></span> | <span data-ttu-id="6c31c-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="6c31c-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-538">IsEnabled</span></span>



| <span data-ttu-id="6c31c-539">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-539">Entry</span></span> | <span data-ttu-id="6c31c-540">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-541">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-541">Description</span></span>    | <span data-ttu-id="6c31c-542">Se o aplicativo ou componente COM+ estiver desabilitado, IsEnabled será false.</span><span class="sxs-lookup"><span data-stu-id="6c31c-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="6c31c-543">Se o aplicativo ou componente COM+ estiver habilitado, IsEnabled será true.</span><span class="sxs-lookup"><span data-stu-id="6c31c-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="6c31c-544">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-544">Access</span></span>         | <span data-ttu-id="6c31c-545">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="6c31c-546">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-546">Type</span></span>           | <span data-ttu-id="6c31c-547">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="6c31c-548">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-548">Default</span></span>        | <span data-ttu-id="6c31c-549">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="6c31c-550">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-550">Minimum system</span></span> | <span data-ttu-id="6c31c-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="6c31c-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="6c31c-552">IsSystem</span></span>



| <span data-ttu-id="6c31c-553">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-553">Entry</span></span> | <span data-ttu-id="6c31c-554">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="6c31c-555">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-555">Description</span></span>    | <span data-ttu-id="6c31c-556">Identifica aplicativos de sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="6c31c-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="6c31c-557">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-557">Access</span></span>         | <span data-ttu-id="6c31c-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6c31c-558">ReadOnly</span></span>                             |
| <span data-ttu-id="6c31c-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-559">Type</span></span>           | <span data-ttu-id="6c31c-560">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-560">Bool</span></span>                                 |
| <span data-ttu-id="6c31c-561">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-561">Default</span></span>        | <span data-ttu-id="6c31c-562">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-562">False</span></span>                                |
| <span data-ttu-id="6c31c-563">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-563">Minimum system</span></span> | <span data-ttu-id="6c31c-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="6c31c-565">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="6c31c-565">MaxDumpCount</span></span>



| <span data-ttu-id="6c31c-566">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-566">Entry</span></span> | <span data-ttu-id="6c31c-567">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-568">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-568">Description</span></span>    | <span data-ttu-id="6c31c-569">Indica o número máximo de arquivos a serem gerados antes que a substituição ocorra.</span><span class="sxs-lookup"><span data-stu-id="6c31c-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="6c31c-570">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-570">Access</span></span>         | <span data-ttu-id="6c31c-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="6c31c-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-572">Type</span></span>           | <span data-ttu-id="6c31c-573">Longo (1-200)</span><span class="sxs-lookup"><span data-stu-id="6c31c-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="6c31c-574">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-574">Default</span></span>        | <span data-ttu-id="6c31c-575">5</span><span class="sxs-lookup"><span data-stu-id="6c31c-575">5</span></span>                                                                                |
| <span data-ttu-id="6c31c-576">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-576">Minimum system</span></span> | <span data-ttu-id="6c31c-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="6c31c-578">Nome</span><span class="sxs-lookup"><span data-stu-id="6c31c-578">Name</span></span>



| <span data-ttu-id="6c31c-579">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-579">Entry</span></span> | <span data-ttu-id="6c31c-580">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-581">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-581">Description</span></span>    | <span data-ttu-id="6c31c-582">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-582">The name of the application.</span></span> <span data-ttu-id="6c31c-583">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="6c31c-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6c31c-584">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-584">Access</span></span>         | <span data-ttu-id="6c31c-585">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="6c31c-586">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-586">Type</span></span>           | <span data-ttu-id="6c31c-587">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="6c31c-588">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-588">Default</span></span>        | <span data-ttu-id="6c31c-589">"Novo aplicativo"</span><span class="sxs-lookup"><span data-stu-id="6c31c-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-590">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-590">Minimum system</span></span> | <span data-ttu-id="6c31c-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="6c31c-592">Nomes exclusivos devem ser escolhidos para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="6c31c-593">Se vários aplicativos forem criados com o mesmo nome, ele poderá interferir na referência aos aplicativos por nome, resultando em um comportamento imprevisível.</span><span class="sxs-lookup"><span data-stu-id="6c31c-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="6c31c-594">Senha</span><span class="sxs-lookup"><span data-stu-id="6c31c-594">Password</span></span>



| <span data-ttu-id="6c31c-595">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-595">Entry</span></span> | <span data-ttu-id="6c31c-596">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-597">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-597">Description</span></span>    | <span data-ttu-id="6c31c-598">Define a senha usada pelo processo do servidor para fazer logon sob a identidade.</span><span class="sxs-lookup"><span data-stu-id="6c31c-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="6c31c-599">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-599">Access</span></span>         | <span data-ttu-id="6c31c-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="6c31c-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="6c31c-601">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-601">Type</span></span>           | <span data-ttu-id="6c31c-602">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-602">String</span></span>                                                                     |
| <span data-ttu-id="6c31c-603">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-603">Default</span></span>        | <span data-ttu-id="6c31c-604">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-604">""</span></span>                                                                         |
| <span data-ttu-id="6c31c-605">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-605">Minimum system</span></span> | <span data-ttu-id="6c31c-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="6c31c-607">A senha deve ser definida ao mesmo tempo que a identidade, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), pois a senha e a identidade são validadas antes de serem salvas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="6c31c-608">Se a senha e a identidade forem obtidas fora de sincronia, o aplicativo não poderá ser iniciado até que ele seja redefinido por um administrador.</span><span class="sxs-lookup"><span data-stu-id="6c31c-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="6c31c-609">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="6c31c-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="6c31c-610">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-610">Entry</span></span> | <span data-ttu-id="6c31c-611">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-612">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-612">Description</span></span>    | <span data-ttu-id="6c31c-613">Indica em quais circunstâncias as solicitações enfileiradas para um aplicativo são autenticadas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="6c31c-614">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-614">Access</span></span>         | <span data-ttu-id="6c31c-615">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="6c31c-616">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-616">Type</span></span>           | <span data-ttu-id="6c31c-617">Valores longos possíveis: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2)</span><span class="sxs-lookup"><span data-stu-id="6c31c-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="6c31c-618">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-618">Default</span></span>        | <span data-ttu-id="6c31c-619">COMAdminQCMessageAuthenticateSecureApps (0)</span><span class="sxs-lookup"><span data-stu-id="6c31c-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="6c31c-620">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-620">Minimum system</span></span> | <span data-ttu-id="6c31c-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="6c31c-622">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="6c31c-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="6c31c-623">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-623">Entry</span></span> | <span data-ttu-id="6c31c-624">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-625">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-625">Description</span></span>    | <span data-ttu-id="6c31c-626">Indica o número máximo de threads de ouvinte simultâneos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="6c31c-627">O intervalo válido para essa propriedade é de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="6c31c-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="6c31c-628">Para um aplicativo recém-criado, a configuração é derivada do algoritmo usado atualmente para determinar o número padrão de threads de ouvinte: 16 vezes o número de CPUs no servidor.</span><span class="sxs-lookup"><span data-stu-id="6c31c-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="6c31c-629">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-629">Access</span></span>         | <span data-ttu-id="6c31c-630">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6c31c-631">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-631">Type</span></span>           | <span data-ttu-id="6c31c-632">Longo (0-1000)</span><span class="sxs-lookup"><span data-stu-id="6c31c-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6c31c-633">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-633">Default</span></span>        | <span data-ttu-id="6c31c-634">0</span><span class="sxs-lookup"><span data-stu-id="6c31c-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6c31c-635">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-635">Minimum system</span></span> | <span data-ttu-id="6c31c-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="6c31c-637">Essa propriedade também está disponível com a funcionalidade de leitura/gravação na guia **enfileiramento** da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="6c31c-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="6c31c-638">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="6c31c-639">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-639">Entry</span></span> | <span data-ttu-id="6c31c-640">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-641">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-641">Description</span></span>    | <span data-ttu-id="6c31c-642">Indica se o ouvinte de componentes na fila está habilitado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="6c31c-643">Se habilitada, o ouvinte será iniciado quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="6c31c-644">Essa propriedade entrará em vigor somente se QueuingEnabled estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="6c31c-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="6c31c-645">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-645">Access</span></span>         | <span data-ttu-id="6c31c-646">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="6c31c-647">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-647">Type</span></span>           | <span data-ttu-id="6c31c-648">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="6c31c-649">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-649">Default</span></span>        | <span data-ttu-id="6c31c-650">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="6c31c-651">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-651">Minimum system</span></span> | <span data-ttu-id="6c31c-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="6c31c-653">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-653">QueuingEnabled</span></span>



| <span data-ttu-id="6c31c-654">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-654">Entry</span></span> | <span data-ttu-id="6c31c-655">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-656">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-656">Description</span></span>    | <span data-ttu-id="6c31c-657">Indica se o serviço de componentes em fila COM+ está habilitado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="6c31c-658">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-658">Access</span></span>         | <span data-ttu-id="6c31c-659">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="6c31c-660">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-660">Type</span></span>           | <span data-ttu-id="6c31c-661">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="6c31c-662">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-662">Default</span></span>        | <span data-ttu-id="6c31c-663">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-663">False</span></span>                                                                                |
| <span data-ttu-id="6c31c-664">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-664">Minimum system</span></span> | <span data-ttu-id="6c31c-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="6c31c-666">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="6c31c-667">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-667">Entry</span></span> | <span data-ttu-id="6c31c-668">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-669">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-669">Description</span></span>    | <span data-ttu-id="6c31c-670">Indica o número máximo de ativações de objetos configurados no aplicativo a serem aceitos antes da reciclagem do processo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="6c31c-671">O número padrão de ativações é 0.</span><span class="sxs-lookup"><span data-stu-id="6c31c-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="6c31c-672">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-672">Access</span></span>         | <span data-ttu-id="6c31c-673">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="6c31c-674">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-674">Type</span></span>           | <span data-ttu-id="6c31c-675">Longo (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="6c31c-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="6c31c-676">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-676">Default</span></span>        | <span data-ttu-id="6c31c-677">0</span><span class="sxs-lookup"><span data-stu-id="6c31c-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="6c31c-678">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-678">Minimum system</span></span> | <span data-ttu-id="6c31c-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="6c31c-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-680">RecycleCallLimit</span></span>



| <span data-ttu-id="6c31c-681">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-681">Entry</span></span> | <span data-ttu-id="6c31c-682">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-683">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-683">Description</span></span>    | <span data-ttu-id="6c31c-684">Indica o número máximo de chamadas para permitir que os objetos configurados no aplicativo sejam aceitos antes da reciclagem do processo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="6c31c-685">O número padrão de chamadas é 0.</span><span class="sxs-lookup"><span data-stu-id="6c31c-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="6c31c-686">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-686">Access</span></span>         | <span data-ttu-id="6c31c-687">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="6c31c-688">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-688">Type</span></span>           | <span data-ttu-id="6c31c-689">Longo (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="6c31c-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="6c31c-690">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-690">Default</span></span>        | <span data-ttu-id="6c31c-691">0</span><span class="sxs-lookup"><span data-stu-id="6c31c-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="6c31c-692">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-692">Minimum system</span></span> | <span data-ttu-id="6c31c-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="6c31c-694">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="6c31c-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="6c31c-695">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-695">Entry</span></span> | <span data-ttu-id="6c31c-696">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-697">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-697">Description</span></span>    | <span data-ttu-id="6c31c-698">Indica a quantidade de tempo (em minutos) para permitir que um processo reciclado seja executado antes de desligá-lo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="6c31c-699">A contagem regressiva começa imediatamente após o processo ser reciclado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="6c31c-700">O tempo limite máximo de expiração é de 1440 minutos (24 horas) e o padrão é 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="6c31c-701">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-701">Access</span></span>         | <span data-ttu-id="6c31c-702">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6c31c-703">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-703">Type</span></span>           | <span data-ttu-id="6c31c-704">Longo (1-1440)</span><span class="sxs-lookup"><span data-stu-id="6c31c-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-705">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-705">Default</span></span>        | <span data-ttu-id="6c31c-706">15</span><span class="sxs-lookup"><span data-stu-id="6c31c-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6c31c-707">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-707">Minimum system</span></span> | <span data-ttu-id="6c31c-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="6c31c-709">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="6c31c-710">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-710">Entry</span></span> | <span data-ttu-id="6c31c-711">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-712">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-712">Description</span></span>    | <span data-ttu-id="6c31c-713">Indica o número máximo de minutos para permitir que um processo seja executado antes de reciclá-lo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="6c31c-714">O limite máximo de tempo de vida é de 30240 minutos (21 dias) e o padrão é 0 minutos.</span><span class="sxs-lookup"><span data-stu-id="6c31c-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="6c31c-715">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-715">Access</span></span>         | <span data-ttu-id="6c31c-716">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6c31c-717">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-717">Type</span></span>           | <span data-ttu-id="6c31c-718">Longo (0-30240)</span><span class="sxs-lookup"><span data-stu-id="6c31c-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="6c31c-719">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-719">Default</span></span>        | <span data-ttu-id="6c31c-720">0</span><span class="sxs-lookup"><span data-stu-id="6c31c-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="6c31c-721">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-721">Minimum system</span></span> | <span data-ttu-id="6c31c-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="6c31c-723">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="6c31c-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="6c31c-724">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-724">Entry</span></span> | <span data-ttu-id="6c31c-725">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-726">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-726">Description</span></span>    | <span data-ttu-id="6c31c-727">Indica a quantidade máxima de uso de memória (em quilobytes) que permitia um processo antes de ser reciclado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="6c31c-728">Se o uso de memória do processo exceder o número especificado por um período de mais de um minuto, o processo será reciclado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="6c31c-729">A quantidade padrão de uso de memória é 0 KB.</span><span class="sxs-lookup"><span data-stu-id="6c31c-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="6c31c-730">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-730">Access</span></span>         | <span data-ttu-id="6c31c-731">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6c31c-732">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-732">Type</span></span>           | <span data-ttu-id="6c31c-733">Longo (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="6c31c-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6c31c-734">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-734">Default</span></span>        | <span data-ttu-id="6c31c-735">0</span><span class="sxs-lookup"><span data-stu-id="6c31c-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6c31c-736">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-736">Minimum system</span></span> | <span data-ttu-id="6c31c-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="6c31c-738">Replicáveis</span><span class="sxs-lookup"><span data-stu-id="6c31c-738">Replicable</span></span>



| <span data-ttu-id="6c31c-739">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-739">Entry</span></span> | <span data-ttu-id="6c31c-740">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="6c31c-741">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-741">Description</span></span>    | <span data-ttu-id="6c31c-742">Indica se o aplicativo pode ser replicado.</span><span class="sxs-lookup"><span data-stu-id="6c31c-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="6c31c-743">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-743">Access</span></span>         | <span data-ttu-id="6c31c-744">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="6c31c-745">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-745">Type</span></span>           | <span data-ttu-id="6c31c-746">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-746">Bool</span></span>                                                 |
| <span data-ttu-id="6c31c-747">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-747">Default</span></span>        | <span data-ttu-id="6c31c-748">True</span><span class="sxs-lookup"><span data-stu-id="6c31c-748">True</span></span>                                                 |
| <span data-ttu-id="6c31c-749">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-749">Minimum system</span></span> | <span data-ttu-id="6c31c-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="6c31c-751">RunForever</span><span class="sxs-lookup"><span data-stu-id="6c31c-751">RunForever</span></span>



| <span data-ttu-id="6c31c-752">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-752">Entry</span></span> | <span data-ttu-id="6c31c-753">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-754">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-754">Description</span></span>    | <span data-ttu-id="6c31c-755">Permite que um processo do servidor continue se um aplicativo estiver ocioso.</span><span class="sxs-lookup"><span data-stu-id="6c31c-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="6c31c-756">Se definido como true, o processo do servidor não é desligado quando deixado ocioso.</span><span class="sxs-lookup"><span data-stu-id="6c31c-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="6c31c-757">Se definido como false, o processo será desligado de acordo com o valor definido pela propriedade ShutdownAfter.</span><span class="sxs-lookup"><span data-stu-id="6c31c-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="6c31c-758">RunForever não está habilitado para aplicativos de biblioteca (em processo).</span><span class="sxs-lookup"><span data-stu-id="6c31c-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="6c31c-759">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-759">Access</span></span>         | <span data-ttu-id="6c31c-760">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="6c31c-761">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-761">Type</span></span>           | <span data-ttu-id="6c31c-762">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="6c31c-763">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-763">Default</span></span>        | <span data-ttu-id="6c31c-764">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-765">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-765">Minimum system</span></span> | <span data-ttu-id="6c31c-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="6c31c-767">ServiceName</span><span class="sxs-lookup"><span data-stu-id="6c31c-767">ServiceName</span></span>



| <span data-ttu-id="6c31c-768">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-768">Entry</span></span> | <span data-ttu-id="6c31c-769">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-770">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-770">Description</span></span>    | <span data-ttu-id="6c31c-771">O nome do serviço correspondente ao aplicativo configurado para ser executado como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="6c31c-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="6c31c-772">Se esse valor for **nulo**, o aplicativo não será configurado para ser executado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="6c31c-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="6c31c-773">Caso contrário, as informações de configuração para o serviço podem ser encontradas usando o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="6c31c-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="6c31c-774">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-774">Access</span></span>         | <span data-ttu-id="6c31c-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6c31c-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6c31c-776">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-776">Type</span></span>           | <span data-ttu-id="6c31c-777">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6c31c-778">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-778">Default</span></span>        | <span data-ttu-id="6c31c-779">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6c31c-780">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-780">Minimum system</span></span> | <span data-ttu-id="6c31c-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="6c31c-782">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="6c31c-782">ShutdownAfter</span></span>



| <span data-ttu-id="6c31c-783">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-783">Entry</span></span> | <span data-ttu-id="6c31c-784">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-785">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-785">Description</span></span>    | <span data-ttu-id="6c31c-786">Define o atraso antes de desligar um processo do servidor depois que ele se torna ocioso.</span><span class="sxs-lookup"><span data-stu-id="6c31c-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="6c31c-787">Intervalos de latência de desligamento de 0 a 1440 minutos (24 horas).</span><span class="sxs-lookup"><span data-stu-id="6c31c-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="6c31c-788">Se RunForever for definido como true, essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="6c31c-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="6c31c-789">ShutdownAfter não está habilitado para aplicativos de biblioteca (em processo).</span><span class="sxs-lookup"><span data-stu-id="6c31c-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="6c31c-790">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-790">Access</span></span>         | <span data-ttu-id="6c31c-791">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6c31c-792">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-792">Type</span></span>           | <span data-ttu-id="6c31c-793">Longo (0-1440)</span><span class="sxs-lookup"><span data-stu-id="6c31c-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6c31c-794">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-794">Default</span></span>        | <span data-ttu-id="6c31c-795">3</span><span class="sxs-lookup"><span data-stu-id="6c31c-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6c31c-796">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-796">Minimum system</span></span> | <span data-ttu-id="6c31c-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c31c-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="6c31c-798">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="6c31c-798">SoapActivated</span></span>



| <span data-ttu-id="6c31c-799">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-799">Entry</span></span> | <span data-ttu-id="6c31c-800">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-801">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-801">Description</span></span>    | <span data-ttu-id="6c31c-802">Indica se este aplicativo é exposto para consumo por meio do protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="6c31c-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="6c31c-803">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-803">Access</span></span>         | <span data-ttu-id="6c31c-804">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="6c31c-805">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-805">Type</span></span>           | <span data-ttu-id="6c31c-806">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="6c31c-807">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-807">Default</span></span>        | <span data-ttu-id="6c31c-808">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-808">False</span></span>                                                                                |
| <span data-ttu-id="6c31c-809">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-809">Minimum system</span></span> | <span data-ttu-id="6c31c-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c31c-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="6c31c-811">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="6c31c-811">SoapBaseUrl</span></span>



| <span data-ttu-id="6c31c-812">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-812">Entry</span></span> | <span data-ttu-id="6c31c-813">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-814">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-814">Description</span></span>    | <span data-ttu-id="6c31c-815">O ponto de extremidade de URL no qual esse aplicativo é exposto por meio do protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="6c31c-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="6c31c-816">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-816">Access</span></span>         | <span data-ttu-id="6c31c-817">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="6c31c-818">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-818">Type</span></span>           | <span data-ttu-id="6c31c-819">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-819">String</span></span>                                                                       |
| <span data-ttu-id="6c31c-820">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-820">Default</span></span>        | <span data-ttu-id="6c31c-821">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-821">""</span></span>                                                                           |
| <span data-ttu-id="6c31c-822">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-822">Minimum system</span></span> | <span data-ttu-id="6c31c-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c31c-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="6c31c-824">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="6c31c-824">SoapMailTo</span></span>



| <span data-ttu-id="6c31c-825">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-825">Entry</span></span> | <span data-ttu-id="6c31c-826">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-827">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-827">Description</span></span>    | <span data-ttu-id="6c31c-828">O endereço de email no qual esse aplicativo é exposto por meio do protocolo SOAP.</span><span class="sxs-lookup"><span data-stu-id="6c31c-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="6c31c-829">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-829">Access</span></span>         | <span data-ttu-id="6c31c-830">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="6c31c-831">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-831">Type</span></span>           | <span data-ttu-id="6c31c-832">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-832">String</span></span>                                                                        |
| <span data-ttu-id="6c31c-833">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-833">Default</span></span>        | <span data-ttu-id="6c31c-834">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-834">""</span></span>                                                                            |
| <span data-ttu-id="6c31c-835">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-835">Minimum system</span></span> | <span data-ttu-id="6c31c-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c31c-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="6c31c-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="6c31c-837">SoapVRoot</span></span>



| <span data-ttu-id="6c31c-838">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-838">Entry</span></span> | <span data-ttu-id="6c31c-839">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-840">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-840">Description</span></span>    | <span data-ttu-id="6c31c-841">O diretório raiz virtual do IIS no qual os scripts de acesso que expõem o aplicativo por meio do protocolo SOAP residem.</span><span class="sxs-lookup"><span data-stu-id="6c31c-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="6c31c-842">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-842">Access</span></span>         | <span data-ttu-id="6c31c-843">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="6c31c-844">Type</span><span class="sxs-lookup"><span data-stu-id="6c31c-844">Type</span></span>           | <span data-ttu-id="6c31c-845">String</span><span class="sxs-lookup"><span data-stu-id="6c31c-845">String</span></span>                                                                                                               |
| <span data-ttu-id="6c31c-846">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-846">Default</span></span>        | <span data-ttu-id="6c31c-847">""</span><span class="sxs-lookup"><span data-stu-id="6c31c-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="6c31c-848">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-848">Minimum system</span></span> | <span data-ttu-id="6c31c-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c31c-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="6c31c-850">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="6c31c-850">SRPEnabled</span></span>



| <span data-ttu-id="6c31c-851">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-851">Entry</span></span> | <span data-ttu-id="6c31c-852">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-853">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-853">Description</span></span>    | <span data-ttu-id="6c31c-854">Determina a política de restrição de software (SRP) para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="6c31c-855">Se definido como true, a propriedade SRPTrustLevel para o aplicativo será usada.</span><span class="sxs-lookup"><span data-stu-id="6c31c-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="6c31c-856">Se definido como false, as diretivas de restrição de software das configurações de segurança local serão usadas.</span><span class="sxs-lookup"><span data-stu-id="6c31c-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="6c31c-857">As configurações de segurança local são controladas por meio do snap-in Diretiva de segurança local do console de gerenciamento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c31c-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="6c31c-858">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-858">Access</span></span>         | <span data-ttu-id="6c31c-859">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6c31c-860">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-860">Type</span></span>           | <span data-ttu-id="6c31c-861">Bool</span><span class="sxs-lookup"><span data-stu-id="6c31c-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6c31c-862">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-862">Default</span></span>        | <span data-ttu-id="6c31c-863">Falso</span><span class="sxs-lookup"><span data-stu-id="6c31c-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6c31c-864">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-864">Minimum system</span></span> | <span data-ttu-id="6c31c-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="6c31c-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="6c31c-866">SRPTrustLevel</span></span>



| <span data-ttu-id="6c31c-867">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c31c-867">Entry</span></span> | <span data-ttu-id="6c31c-868">Valor</span><span class="sxs-lookup"><span data-stu-id="6c31c-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31c-869">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c31c-869">Description</span></span>    | <span data-ttu-id="6c31c-870">Indica o nível de confiança da política de restrição de software (SRP) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="6c31c-871">Essa propriedade será usada somente se a propriedade SRPEnabled estiver definida como true.</span><span class="sxs-lookup"><span data-stu-id="6c31c-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="6c31c-872">O nível de confiança do SRP refere-se ao nível de confiança que você está disposto a dar a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c31c-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="6c31c-873">Um nível de confiança de SRP irrestrito corresponde ao valor de \_ enumeração de FULLYTRUSTED de nível mais seguro \_ , enquanto um nível de confiança SRP não permitido corresponde ao valor de enumeração mais seguro de \_ levelid não \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="6c31c-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="6c31c-874">A enumeração para os níveis de confiança é definida em Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="6c31c-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="6c31c-875">Access</span><span class="sxs-lookup"><span data-stu-id="6c31c-875">Access</span></span>         | <span data-ttu-id="6c31c-876">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c31c-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6c31c-877">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c31c-877">Type</span></span>           | <span data-ttu-id="6c31c-878">Valores longos possíveis: nível mais seguro \_ de redistribuirid não \_ permitido (0x0) \_ FULLYTRUSTED de nível mais seguro \_ (0x40000)</span><span class="sxs-lookup"><span data-stu-id="6c31c-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c31c-879">Padrão</span><span class="sxs-lookup"><span data-stu-id="6c31c-879">Default</span></span>        | <span data-ttu-id="6c31c-880">\_FULLYTRUSTED de nívelid mais seguro \_ (0x40000)</span><span class="sxs-lookup"><span data-stu-id="6c31c-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6c31c-881">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6c31c-881">Minimum system</span></span> | <span data-ttu-id="6c31c-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c31c-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="6c31c-883">Um aplicativo para o qual você está disposto a confiar com acesso irrestrito deve ter a segurança mais rigorosa anexada a ele.</span><span class="sxs-lookup"><span data-stu-id="6c31c-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="6c31c-884">Os aplicativos que são irrestritos podem carregar apenas componentes irrestritos, enquanto os aplicativos não permitidos não poderão ser executados e, portanto, não poderão carregar nenhum componente.</span><span class="sxs-lookup"><span data-stu-id="6c31c-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c31c-885">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c31c-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c31c-886">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="6c31c-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
