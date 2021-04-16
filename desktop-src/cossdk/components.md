---
description: Contém um objeto para cada componente no aplicativo relacionado.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Coleção de componentes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501091"
---
# <a name="components-collection"></a><span data-ttu-id="307b8-103">Coleção de componentes</span><span class="sxs-lookup"><span data-stu-id="307b8-103">Components collection</span></span>

<span data-ttu-id="307b8-104">Contém um objeto para cada componente no aplicativo relacionado.</span><span class="sxs-lookup"><span data-stu-id="307b8-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="307b8-105">A coleção de **componentes** está sempre relacionada a um objeto na coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="307b8-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="307b8-106">As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="307b8-107">Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="307b8-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="307b8-108">Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="307b8-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="307b8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="307b8-109">Members</span></span>

<span data-ttu-id="307b8-110">A coleção de **componentes** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="307b8-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="307b8-111">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="307b8-111">Related Collections</span></span>

<span data-ttu-id="307b8-112">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="307b8-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="307b8-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="307b8-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="307b8-114">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="307b8-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="307b8-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="307b8-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="307b8-116">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="307b8-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="307b8-117">**RolesForComponent**</span><span class="sxs-lookup"><span data-stu-id="307b8-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="307b8-118">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="307b8-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="307b8-119">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="307b8-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="307b8-120">**Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="307b8-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="307b8-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="307b8-121">Properties</span></span>

<span data-ttu-id="307b8-122">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="307b8-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="307b8-123">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="307b8-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="307b8-124">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="307b8-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="307b8-125">Número de bits</span><span class="sxs-lookup"><span data-stu-id="307b8-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="307b8-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="307b8-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="307b8-127">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="307b8-128">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="307b8-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="307b8-129">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="307b8-130">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="307b8-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="307b8-131">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="307b8-132">Construtorstring</span><span class="sxs-lookup"><span data-stu-id="307b8-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="307b8-133">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="307b8-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="307b8-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-134">Description</span></span>](#description)
-   [<span data-ttu-id="307b8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="307b8-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="307b8-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="307b8-137">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="307b8-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="307b8-138">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="307b8-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="307b8-139">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="307b8-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="307b8-140">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="307b8-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="307b8-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="307b8-142">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="307b8-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="307b8-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="307b8-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="307b8-144">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="307b8-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="307b8-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="307b8-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="307b8-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="307b8-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="307b8-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="307b8-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="307b8-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="307b8-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="307b8-149">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="307b8-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="307b8-150">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="307b8-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="307b8-151">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="307b8-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="307b8-152">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="307b8-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="307b8-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="307b8-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="307b8-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="307b8-155">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="307b8-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="307b8-156">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="307b8-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="307b8-157">Sincronização</span><span class="sxs-lookup"><span data-stu-id="307b8-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="307b8-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="307b8-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="307b8-159">Transação</span><span class="sxs-lookup"><span data-stu-id="307b8-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="307b8-160">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="307b8-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="307b8-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="307b8-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="307b8-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="307b8-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="307b8-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="307b8-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="307b8-164">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="307b8-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="307b8-165">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="307b8-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="307b8-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-166">Entry</span></span> | <span data-ttu-id="307b8-167">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="307b8-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-168">Description</span></span>    | <span data-ttu-id="307b8-169">Habilita os assinantes do processo se o componente for uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="307b8-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="307b8-170">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-170">Access</span></span>         | <span data-ttu-id="307b8-171">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="307b8-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-172">Type</span></span>           | <span data-ttu-id="307b8-173">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-173">Bool</span></span>                                                               |
| <span data-ttu-id="307b8-174">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-174">Default</span></span>        | <span data-ttu-id="307b8-175">True</span><span class="sxs-lookup"><span data-stu-id="307b8-175">True</span></span>                                                               |
| <span data-ttu-id="307b8-176">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-176">Minimum system</span></span> | <span data-ttu-id="307b8-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="307b8-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="307b8-178">ApplicationID</span></span>



| <span data-ttu-id="307b8-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-179">Entry</span></span> | <span data-ttu-id="307b8-180">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-181">Description</span></span>    | <span data-ttu-id="307b8-182">O GUID do aplicativo que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="307b8-183">Deve ser um GUID de aplicativo válido, que é verificado antes que [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="307b8-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="307b8-184">Se esse valor for alterado para ser um GUID para um aplicativo diferente, o componente será movido para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="307b8-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="307b8-185">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-185">Access</span></span>         | <span data-ttu-id="307b8-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="307b8-187">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-187">Type</span></span>           | <span data-ttu-id="307b8-188">String</span><span class="sxs-lookup"><span data-stu-id="307b8-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="307b8-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-189">Default</span></span>        | <span data-ttu-id="307b8-190">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="307b8-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-191">Minimum system</span></span> | <span data-ttu-id="307b8-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="307b8-193">Número de bits</span><span class="sxs-lookup"><span data-stu-id="307b8-193">Bitness</span></span>



| <span data-ttu-id="307b8-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-194">Entry</span></span> | <span data-ttu-id="307b8-195">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-196">Description</span></span>    | <span data-ttu-id="307b8-197">Representa o tipo de bit de bits binário de um componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="307b8-198">Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="307b8-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="307b8-199">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-199">Access</span></span>         | <span data-ttu-id="307b8-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="307b8-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-201">Type</span></span>           | <span data-ttu-id="307b8-202">Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="307b8-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="307b8-203">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-203">Default</span></span>        | <span data-ttu-id="307b8-204">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="307b8-205">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-205">Minimum system</span></span> | <span data-ttu-id="307b8-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="307b8-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="307b8-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="307b8-207">CLSID</span></span>



| <span data-ttu-id="307b8-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-208">Entry</span></span> | <span data-ttu-id="307b8-209">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-210">Description</span></span>    | <span data-ttu-id="307b8-211">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-211">A GUID for the component.</span></span> <span data-ttu-id="307b8-212">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="307b8-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="307b8-213">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-213">Access</span></span>         | <span data-ttu-id="307b8-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="307b8-215">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-215">Type</span></span>           | <span data-ttu-id="307b8-216">String</span><span class="sxs-lookup"><span data-stu-id="307b8-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="307b8-217">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-217">Default</span></span>        | <span data-ttu-id="307b8-218">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="307b8-219">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-219">Minimum system</span></span> | <span data-ttu-id="307b8-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="307b8-221">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="307b8-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-222">Entry</span></span> | <span data-ttu-id="307b8-223">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-224">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-224">Description</span></span>    | <span data-ttu-id="307b8-225">Indica se as verificações de acesso baseado em função são executadas em chamadas no componente e funcionam em conjunto com as propriedades AccessChecksLevel e ApplicationAccessChecksEnabled no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="307b8-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="307b8-226">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-226">Access</span></span>         | <span data-ttu-id="307b8-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="307b8-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-228">Type</span></span>           | <span data-ttu-id="307b8-229">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="307b8-230">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-230">Default</span></span>        | <span data-ttu-id="307b8-231">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="307b8-232">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-232">Minimum system</span></span> | <span data-ttu-id="307b8-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="307b8-234">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="307b8-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="307b8-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-235">Entry</span></span> | <span data-ttu-id="307b8-236">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-237">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-237">Description</span></span>    | <span data-ttu-id="307b8-238">Quando usado em uma transação, especifica o período de tempo em que esse componente faz com que a transação expire. O padrão é 60 segundos e não pode ter mais de 3600 segundos (1 hora).</span><span class="sxs-lookup"><span data-stu-id="307b8-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="307b8-239">O valor de tempo limite pode ser definido como 0, especificando um período de tempo limite de transação infinito.</span><span class="sxs-lookup"><span data-stu-id="307b8-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="307b8-240">Para que essa propriedade seja usada, ComponentTransactionTimeoutEnabled deve ser true.</span><span class="sxs-lookup"><span data-stu-id="307b8-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="307b8-241">O valor dessa propriedade substitui o tempo limite da transação global especificado pela propriedade TransactionTimeout da coleção [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="307b8-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="307b8-242">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-242">Access</span></span>         | <span data-ttu-id="307b8-243">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="307b8-244">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-244">Type</span></span>           | <span data-ttu-id="307b8-245">Longo (0-3600)</span><span class="sxs-lookup"><span data-stu-id="307b8-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="307b8-246">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-246">Default</span></span>        | <span data-ttu-id="307b8-247">60</span><span class="sxs-lookup"><span data-stu-id="307b8-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="307b8-248">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-248">Minimum system</span></span> | <span data-ttu-id="307b8-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="307b8-250">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="307b8-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-251">Entry</span></span> | <span data-ttu-id="307b8-252">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-253">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-253">Description</span></span>    | <span data-ttu-id="307b8-254">Especifica se o período de tempo limite da transação está habilitado para este componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="307b8-255">Por padrão, o recurso de tempo limite da transação é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="307b8-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="307b8-256">Quando essa propriedade é true, o tempo limite especificado por ComponentTransactionTimeout é usado.</span><span class="sxs-lookup"><span data-stu-id="307b8-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="307b8-257">Quando essa propriedade é falsa, o tempo limite especificado pela propriedade TransactionTimeout da coleção [**LocalComputer**](localcomputer.md) é usado.</span><span class="sxs-lookup"><span data-stu-id="307b8-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="307b8-258">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-258">Access</span></span>         | <span data-ttu-id="307b8-259">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="307b8-260">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-260">Type</span></span>           | <span data-ttu-id="307b8-261">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="307b8-262">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-262">Default</span></span>        | <span data-ttu-id="307b8-263">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="307b8-264">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-264">Minimum system</span></span> | <span data-ttu-id="307b8-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="307b8-266">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="307b8-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="307b8-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-267">Entry</span></span> | <span data-ttu-id="307b8-268">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-269">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-269">Description</span></span>    | <span data-ttu-id="307b8-270">Habilita a passagem de propriedades de contexto do COMTI (integrador de transações COM) para o contexto desta classe.</span><span class="sxs-lookup"><span data-stu-id="307b8-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="307b8-271">A COMTI facilita a tarefa de encapsular as transações de mainframe e a lógica de negócios como componentes COM.</span><span class="sxs-lookup"><span data-stu-id="307b8-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="307b8-272">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-272">Access</span></span>         | <span data-ttu-id="307b8-273">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="307b8-274">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-274">Type</span></span>           | <span data-ttu-id="307b8-275">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="307b8-276">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-276">Default</span></span>        | <span data-ttu-id="307b8-277">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="307b8-278">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-278">Minimum system</span></span> | <span data-ttu-id="307b8-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="307b8-280">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-280">ConstructionEnabled</span></span>



| <span data-ttu-id="307b8-281">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-281">Entry</span></span> | <span data-ttu-id="307b8-282">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-283">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-283">Description</span></span>    | <span data-ttu-id="307b8-284">Determina se constructorString são passados para o objeto quando ele é construído.</span><span class="sxs-lookup"><span data-stu-id="307b8-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="307b8-285">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-285">Access</span></span>         | <span data-ttu-id="307b8-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="307b8-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-287">Type</span></span>           | <span data-ttu-id="307b8-288">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="307b8-289">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-289">Default</span></span>        | <span data-ttu-id="307b8-290">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-290">False</span></span>                                                                                    |
| <span data-ttu-id="307b8-291">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-291">Minimum system</span></span> | <span data-ttu-id="307b8-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="307b8-293">Construtorstring</span><span class="sxs-lookup"><span data-stu-id="307b8-293">ConstructorString</span></span>



| <span data-ttu-id="307b8-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-294">Entry</span></span> | <span data-ttu-id="307b8-295">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-296">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-296">Description</span></span>    | <span data-ttu-id="307b8-297">Cadeia de inicialização para construção de componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-297">Initialization string for component construction.</span></span> <span data-ttu-id="307b8-298">Você pode criar objetos diferentes do mesmo componente genérico usando cadeias de caracteres do construtor de objetos.</span><span class="sxs-lookup"><span data-stu-id="307b8-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="307b8-299">Se ConstructionEnabled for false, essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="307b8-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="307b8-300">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-300">Access</span></span>         | <span data-ttu-id="307b8-301">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="307b8-302">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-302">Type</span></span>           | <span data-ttu-id="307b8-303">String</span><span class="sxs-lookup"><span data-stu-id="307b8-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="307b8-304">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-304">Default</span></span>        | <span data-ttu-id="307b8-305">""</span><span class="sxs-lookup"><span data-stu-id="307b8-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="307b8-306">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-306">Minimum system</span></span> | <span data-ttu-id="307b8-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="307b8-308">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="307b8-308">CreationTimeout</span></span>



| <span data-ttu-id="307b8-309">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-309">Entry</span></span> | <span data-ttu-id="307b8-310">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-311">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-311">Description</span></span>    | <span data-ttu-id="307b8-312">Ao criar o objeto, o número de milissegundos antes de um erro de tempo limite é retornado.</span><span class="sxs-lookup"><span data-stu-id="307b8-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="307b8-313">O tempo limite máximo é de 2147483647 milissegundos (cerca de 25 dias).</span><span class="sxs-lookup"><span data-stu-id="307b8-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="307b8-314">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-314">Access</span></span>         | <span data-ttu-id="307b8-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="307b8-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-316">Type</span></span>           | <span data-ttu-id="307b8-317">Longo (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="307b8-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="307b8-318">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-318">Default</span></span>        | <span data-ttu-id="307b8-319">0</span><span class="sxs-lookup"><span data-stu-id="307b8-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="307b8-320">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-320">Minimum system</span></span> | <span data-ttu-id="307b8-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="307b8-322">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-322">Description</span></span>



| <span data-ttu-id="307b8-323">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-323">Entry</span></span> | <span data-ttu-id="307b8-324">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="307b8-325">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-325">Description</span></span>    | <span data-ttu-id="307b8-326">Descreve o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-326">Describes the component.</span></span> |
| <span data-ttu-id="307b8-327">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-327">Access</span></span>         | <span data-ttu-id="307b8-328">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-328">ReadWrite</span></span>                |
| <span data-ttu-id="307b8-329">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-329">Type</span></span>           | <span data-ttu-id="307b8-330">String</span><span class="sxs-lookup"><span data-stu-id="307b8-330">String</span></span>                   |
| <span data-ttu-id="307b8-331">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-331">Default</span></span>        | <span data-ttu-id="307b8-332">""</span><span class="sxs-lookup"><span data-stu-id="307b8-332">""</span></span>                       |
| <span data-ttu-id="307b8-333">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-333">Minimum system</span></span> | <span data-ttu-id="307b8-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="307b8-335">DLL</span><span class="sxs-lookup"><span data-stu-id="307b8-335">DLL</span></span>



| <span data-ttu-id="307b8-336">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-336">Entry</span></span> | <span data-ttu-id="307b8-337">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="307b8-338">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-338">Description</span></span>    | <span data-ttu-id="307b8-339">O nome e o caminho do arquivo que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="307b8-340">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-340">Access</span></span>         | <span data-ttu-id="307b8-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="307b8-342">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-342">Type</span></span>           | <span data-ttu-id="307b8-343">String</span><span class="sxs-lookup"><span data-stu-id="307b8-343">String</span></span>                                                  |
| <span data-ttu-id="307b8-344">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-344">Default</span></span>        | <span data-ttu-id="307b8-345">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-345">N/A</span></span>                                                     |
| <span data-ttu-id="307b8-346">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-346">Minimum system</span></span> | <span data-ttu-id="307b8-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="307b8-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="307b8-349">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-349">Entry</span></span> | <span data-ttu-id="307b8-350">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-351">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-351">Description</span></span>    | <span data-ttu-id="307b8-352">Determina se os eventos são rastreados.</span><span class="sxs-lookup"><span data-stu-id="307b8-352">Determines whether events are tracked.</span></span> <span data-ttu-id="307b8-353">Os eventos incluem ações como o desligamento do aplicativo; criação e liberação de objeto; referências de objeto, consistência, ativação e desativação; chamadas de método, retornos e exceções; inicialização da transação, preparação para confirmação e anulação; conexão, alocação e reciclagem de dispensadores de recursos; alocação e reciclagem de threads.</span><span class="sxs-lookup"><span data-stu-id="307b8-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="307b8-354">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-354">Access</span></span>         | <span data-ttu-id="307b8-355">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="307b8-356">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-356">Type</span></span>           | <span data-ttu-id="307b8-357">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="307b8-358">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-358">Default</span></span>        | <span data-ttu-id="307b8-359">True</span><span class="sxs-lookup"><span data-stu-id="307b8-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="307b8-360">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-360">Minimum system</span></span> | <span data-ttu-id="307b8-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="307b8-362">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="307b8-362">ExceptionClass</span></span>



| <span data-ttu-id="307b8-363">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-363">Entry</span></span> | <span data-ttu-id="307b8-364">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-365">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-365">Description</span></span>    | <span data-ttu-id="307b8-366">O CLSID, que pode ser um GUID ou uma cadeia de caracteres do moniker, para ativar um programa alternativo durante o processo de lidar com um programa de componentes enfileirados com falha repetidamente.</span><span class="sxs-lookup"><span data-stu-id="307b8-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="307b8-367">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-367">Access</span></span>         | <span data-ttu-id="307b8-368">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="307b8-369">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-369">Type</span></span>           | <span data-ttu-id="307b8-370">String</span><span class="sxs-lookup"><span data-stu-id="307b8-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="307b8-371">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-371">Default</span></span>        | <span data-ttu-id="307b8-372">""</span><span class="sxs-lookup"><span data-stu-id="307b8-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="307b8-373">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-373">Minimum system</span></span> | <span data-ttu-id="307b8-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="307b8-375">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="307b8-375">FireInParallel</span></span>



| <span data-ttu-id="307b8-376">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-376">Entry</span></span> | <span data-ttu-id="307b8-377">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="307b8-378">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-378">Description</span></span>    | <span data-ttu-id="307b8-379">Habilita eventos a serem acionados em paralelo se o componente for uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="307b8-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="307b8-380">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-380">Access</span></span>         | <span data-ttu-id="307b8-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="307b8-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-382">Type</span></span>           | <span data-ttu-id="307b8-383">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-383">Bool</span></span>                                                                       |
| <span data-ttu-id="307b8-384">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-384">Default</span></span>        | <span data-ttu-id="307b8-385">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-385">False</span></span>                                                                      |
| <span data-ttu-id="307b8-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-386">Minimum system</span></span> | <span data-ttu-id="307b8-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="307b8-388">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="307b8-388">IISIntrinsics</span></span>



| <span data-ttu-id="307b8-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-389">Entry</span></span> | <span data-ttu-id="307b8-390">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-391">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-391">Description</span></span>    | <span data-ttu-id="307b8-392">Habilita a passagem de propriedades de contexto do IIS, como um objeto de sessão de aplicativo ou um objeto de sessão de usuário, para o contexto dessa classe.</span><span class="sxs-lookup"><span data-stu-id="307b8-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="307b8-393">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-393">Access</span></span>         | <span data-ttu-id="307b8-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="307b8-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-395">Type</span></span>           | <span data-ttu-id="307b8-396">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="307b8-397">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-397">Default</span></span>        | <span data-ttu-id="307b8-398">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="307b8-399">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-399">Minimum system</span></span> | <span data-ttu-id="307b8-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="307b8-401">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="307b8-401">InitializeServerApplication</span></span>



| <span data-ttu-id="307b8-402">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-402">Entry</span></span> | <span data-ttu-id="307b8-403">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="307b8-404">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-404">Description</span></span>    | <span data-ttu-id="307b8-405">Indica se o componente é usado para inicializar um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="307b8-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="307b8-406">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-406">Access</span></span>         | <span data-ttu-id="307b8-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="307b8-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-408">Type</span></span>           | <span data-ttu-id="307b8-409">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-409">Bool</span></span>                                                                        |
| <span data-ttu-id="307b8-410">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-410">Default</span></span>        | <span data-ttu-id="307b8-411">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-411">False</span></span>                                                                       |
| <span data-ttu-id="307b8-412">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-412">Minimum system</span></span> | <span data-ttu-id="307b8-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="307b8-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="307b8-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-414">IsEnabled</span></span>



| <span data-ttu-id="307b8-415">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-415">Entry</span></span> | <span data-ttu-id="307b8-416">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-417">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-417">Description</span></span>    | <span data-ttu-id="307b8-418">False se o aplicativo ou componente COM+ estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="307b8-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="307b8-419">Se o aplicativo ou componente COM+ estiver habilitado, IsEnabled será true.</span><span class="sxs-lookup"><span data-stu-id="307b8-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="307b8-420">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-420">Access</span></span>         | <span data-ttu-id="307b8-421">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="307b8-422">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-422">Type</span></span>           | <span data-ttu-id="307b8-423">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="307b8-424">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-424">Default</span></span>        | <span data-ttu-id="307b8-425">True</span><span class="sxs-lookup"><span data-stu-id="307b8-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="307b8-426">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-426">Minimum system</span></span> | <span data-ttu-id="307b8-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="307b8-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="307b8-428">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="307b8-428">IsEventClass</span></span>



| <span data-ttu-id="307b8-429">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-429">Entry</span></span> | <span data-ttu-id="307b8-430">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="307b8-431">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-431">Description</span></span>    | <span data-ttu-id="307b8-432">Indica se o componente é uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="307b8-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="307b8-433">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-433">Access</span></span>         | <span data-ttu-id="307b8-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="307b8-435">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-435">Type</span></span>           | <span data-ttu-id="307b8-436">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-436">Bool</span></span>                                               |
| <span data-ttu-id="307b8-437">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-437">Default</span></span>        | <span data-ttu-id="307b8-438">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-438">False</span></span>                                              |
| <span data-ttu-id="307b8-439">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-439">Minimum system</span></span> | <span data-ttu-id="307b8-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="307b8-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="307b8-441">IsInstalled</span></span>



| <span data-ttu-id="307b8-442">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-442">Entry</span></span> | <span data-ttu-id="307b8-443">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="307b8-444">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-444">Description</span></span>    | <span data-ttu-id="307b8-445">Indica se o componente está instalado em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="307b8-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="307b8-446">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-446">Access</span></span>         | <span data-ttu-id="307b8-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="307b8-448">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-448">Type</span></span>           | <span data-ttu-id="307b8-449">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-449">Bool</span></span>                                                            |
| <span data-ttu-id="307b8-450">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-450">Default</span></span>        | <span data-ttu-id="307b8-451">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-451">False</span></span>                                                           |
| <span data-ttu-id="307b8-452">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-452">Minimum system</span></span> | <span data-ttu-id="307b8-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="307b8-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="307b8-454">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="307b8-454">IsPrivateComponent</span></span>



| <span data-ttu-id="307b8-455">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-455">Entry</span></span> | <span data-ttu-id="307b8-456">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-457">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-457">Description</span></span>    | <span data-ttu-id="307b8-458">Determina se um aplicativo de servidor é um componente particular.</span><span class="sxs-lookup"><span data-stu-id="307b8-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="307b8-459">Um componente particular em um aplicativo de servidor pode ser ativado somente de dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="307b8-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="307b8-460">Por exemplo, se você chamar [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em um componente particular, ele falhará de fora do processo, mas terá êxito no processo.</span><span class="sxs-lookup"><span data-stu-id="307b8-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="307b8-461">Por outro lado, se você chamar **CoCreateInstance** em um componente público, ele terá sucesso em processo e fora do processo.</span><span class="sxs-lookup"><span data-stu-id="307b8-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="307b8-462">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-462">Access</span></span>         | <span data-ttu-id="307b8-463">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="307b8-464">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-464">Type</span></span>           | <span data-ttu-id="307b8-465">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="307b8-466">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-466">Default</span></span>        | <span data-ttu-id="307b8-467">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="307b8-468">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-468">Minimum system</span></span> | <span data-ttu-id="307b8-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="307b8-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="307b8-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="307b8-470">JustInTimeActivation</span></span>



| <span data-ttu-id="307b8-471">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-471">Entry</span></span> | <span data-ttu-id="307b8-472">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-473">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-473">Description</span></span>    | <span data-ttu-id="307b8-474">Determina se a [ativação JIT](enabling-jit-activation-for-a-component.md) está habilitada para o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="307b8-475">Essa propriedade é definida como true quando o [suporte à transação](setting-the-transaction-attribute.md) é definido como Required, requer novo ou tem suporte.</span><span class="sxs-lookup"><span data-stu-id="307b8-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="307b8-476">Quando JustInTimeActivation é definido como true, o [suporte à sincronização](setting-the-synchronization-attribute.md) deve ser definido como Required (o padrão) ou requer New.</span><span class="sxs-lookup"><span data-stu-id="307b8-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="307b8-477">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-477">Access</span></span>         | <span data-ttu-id="307b8-478">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="307b8-479">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-479">Type</span></span>           | <span data-ttu-id="307b8-480">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="307b8-481">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-481">Default</span></span>        | <span data-ttu-id="307b8-482">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="307b8-483">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-483">Minimum system</span></span> | <span data-ttu-id="307b8-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="307b8-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="307b8-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="307b8-486">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-486">Entry</span></span> | <span data-ttu-id="307b8-487">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-488">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-488">Description</span></span>    | <span data-ttu-id="307b8-489">Se o serviço de balanceamento de carga do componente estiver instalado e habilitado no servidor, o determinará se o componente participa do balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="307b8-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="307b8-490">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-490">Access</span></span>         | <span data-ttu-id="307b8-491">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="307b8-492">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-492">Type</span></span>           | <span data-ttu-id="307b8-493">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="307b8-494">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-494">Default</span></span>        | <span data-ttu-id="307b8-495">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="307b8-496">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-496">Minimum system</span></span> | <span data-ttu-id="307b8-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="307b8-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="307b8-498">MaxPoolSize</span></span>



| <span data-ttu-id="307b8-499">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-499">Entry</span></span> | <span data-ttu-id="307b8-500">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="307b8-501">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-501">Description</span></span>    | <span data-ttu-id="307b8-502">Número máximo de objetos agrupados.</span><span class="sxs-lookup"><span data-stu-id="307b8-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="307b8-503">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-503">Access</span></span>         | <span data-ttu-id="307b8-504">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-504">ReadWrite</span></span>                         |
| <span data-ttu-id="307b8-505">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-505">Type</span></span>           | <span data-ttu-id="307b8-506">Longo (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="307b8-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="307b8-507">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-507">Default</span></span>        | <span data-ttu-id="307b8-508">1048576</span><span class="sxs-lookup"><span data-stu-id="307b8-508">1048576</span></span>                           |
| <span data-ttu-id="307b8-509">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-509">Minimum system</span></span> | <span data-ttu-id="307b8-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="307b8-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="307b8-511">MinPoolSize</span></span>



| <span data-ttu-id="307b8-512">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-512">Entry</span></span> | <span data-ttu-id="307b8-513">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="307b8-514">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-514">Description</span></span>    | <span data-ttu-id="307b8-515">Número mínimo de objetos agrupados.</span><span class="sxs-lookup"><span data-stu-id="307b8-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="307b8-516">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-516">Access</span></span>         | <span data-ttu-id="307b8-517">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-517">ReadWrite</span></span>                         |
| <span data-ttu-id="307b8-518">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-518">Type</span></span>           | <span data-ttu-id="307b8-519">Longo (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="307b8-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="307b8-520">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-520">Default</span></span>        | <span data-ttu-id="307b8-521">0</span><span class="sxs-lookup"><span data-stu-id="307b8-521">0</span></span>                                 |
| <span data-ttu-id="307b8-522">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-522">Minimum system</span></span> | <span data-ttu-id="307b8-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="307b8-524">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="307b8-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="307b8-525">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-525">Entry</span></span> | <span data-ttu-id="307b8-526">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="307b8-527">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-527">Description</span></span>    | <span data-ttu-id="307b8-528">CLSID para o filtro de editor usado se o componente for uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="307b8-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="307b8-529">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-529">Access</span></span>         | <span data-ttu-id="307b8-530">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="307b8-531">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-531">Type</span></span>           | <span data-ttu-id="307b8-532">String</span><span class="sxs-lookup"><span data-stu-id="307b8-532">String</span></span>                                                                  |
| <span data-ttu-id="307b8-533">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-533">Default</span></span>        | <span data-ttu-id="307b8-534">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-534">N/A</span></span>                                                                     |
| <span data-ttu-id="307b8-535">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-535">Minimum system</span></span> | <span data-ttu-id="307b8-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="307b8-537">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="307b8-537">MustRunInClientContext</span></span>



| <span data-ttu-id="307b8-538">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-538">Entry</span></span> | <span data-ttu-id="307b8-539">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-540">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-540">Description</span></span>    | <span data-ttu-id="307b8-541">Indica que o componente deve ser ativado no contexto do chamador original.</span><span class="sxs-lookup"><span data-stu-id="307b8-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="307b8-542">Caso contrário, a ativação falhará.</span><span class="sxs-lookup"><span data-stu-id="307b8-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="307b8-543">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-543">Access</span></span>         | <span data-ttu-id="307b8-544">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="307b8-545">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-545">Type</span></span>           | <span data-ttu-id="307b8-546">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="307b8-547">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-547">Default</span></span>        | <span data-ttu-id="307b8-548">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-548">False</span></span>                                                                                                     |
| <span data-ttu-id="307b8-549">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-549">Minimum system</span></span> | <span data-ttu-id="307b8-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="307b8-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="307b8-551">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="307b8-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="307b8-552">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-552">Entry</span></span> | <span data-ttu-id="307b8-553">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-554">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-554">Description</span></span>    | <span data-ttu-id="307b8-555">Indica que o componente deve ser ativado no contexto do chamador padrão.</span><span class="sxs-lookup"><span data-stu-id="307b8-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="307b8-556">Caso contrário, a ativação falhará.</span><span class="sxs-lookup"><span data-stu-id="307b8-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="307b8-557">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-557">Access</span></span>         | <span data-ttu-id="307b8-558">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="307b8-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-559">Type</span></span>           | <span data-ttu-id="307b8-560">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="307b8-561">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-561">Default</span></span>        | <span data-ttu-id="307b8-562">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-562">False</span></span>                                                                                                        |
| <span data-ttu-id="307b8-563">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-563">Minimum system</span></span> | <span data-ttu-id="307b8-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="307b8-565">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="307b8-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="307b8-566">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-566">Entry</span></span> | <span data-ttu-id="307b8-567">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-568">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-568">Description</span></span>    | <span data-ttu-id="307b8-569">Determina se o [pool de objetos com+](com--object-pooling.md) está habilitado para o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="307b8-570">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-570">Access</span></span>         | <span data-ttu-id="307b8-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="307b8-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-572">Type</span></span>           | <span data-ttu-id="307b8-573">Bool</span><span class="sxs-lookup"><span data-stu-id="307b8-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="307b8-574">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-574">Default</span></span>        | <span data-ttu-id="307b8-575">Falso</span><span class="sxs-lookup"><span data-stu-id="307b8-575">False</span></span>                                                                                           |
| <span data-ttu-id="307b8-576">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-576">Minimum system</span></span> | <span data-ttu-id="307b8-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="307b8-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="307b8-578">ProgID</span></span>



| <span data-ttu-id="307b8-579">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-579">Entry</span></span> | <span data-ttu-id="307b8-580">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-581">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-581">Description</span></span>    | <span data-ttu-id="307b8-582">Um nome amigável usado para identificar o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="307b8-583">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="307b8-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="307b8-584">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-584">Access</span></span>         | <span data-ttu-id="307b8-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="307b8-586">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-586">Type</span></span>           | <span data-ttu-id="307b8-587">String</span><span class="sxs-lookup"><span data-stu-id="307b8-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="307b8-588">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-588">Default</span></span>        | <span data-ttu-id="307b8-589">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="307b8-590">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-590">Minimum system</span></span> | <span data-ttu-id="307b8-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="307b8-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="307b8-592">PublisherID</span></span>



| <span data-ttu-id="307b8-593">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-593">Entry</span></span> | <span data-ttu-id="307b8-594">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="307b8-595">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-595">Description</span></span>    | <span data-ttu-id="307b8-596">Identificador do editor de eventos se o componente for uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="307b8-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="307b8-597">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-597">Access</span></span>         | <span data-ttu-id="307b8-598">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="307b8-599">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-599">Type</span></span>           | <span data-ttu-id="307b8-600">String</span><span class="sxs-lookup"><span data-stu-id="307b8-600">String</span></span>                                                                 |
| <span data-ttu-id="307b8-601">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-601">Default</span></span>        | <span data-ttu-id="307b8-602">""</span><span class="sxs-lookup"><span data-stu-id="307b8-602">""</span></span>                                                                     |
| <span data-ttu-id="307b8-603">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-603">Minimum system</span></span> | <span data-ttu-id="307b8-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="307b8-605">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="307b8-605">SoapAssemblyName</span></span>



| <span data-ttu-id="307b8-606">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-606">Entry</span></span> | <span data-ttu-id="307b8-607">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-608">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-608">Description</span></span>    | <span data-ttu-id="307b8-609">Um GUID que identifica o assembly GAC que é executado quando o componente é invocado como um serviço SOAP.</span><span class="sxs-lookup"><span data-stu-id="307b8-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="307b8-610">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-610">Access</span></span>         | <span data-ttu-id="307b8-611">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="307b8-612">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-612">Type</span></span>           | <span data-ttu-id="307b8-613">String</span><span class="sxs-lookup"><span data-stu-id="307b8-613">String</span></span>                                                                                           |
| <span data-ttu-id="307b8-614">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-614">Default</span></span>        | <span data-ttu-id="307b8-615">NULO</span><span class="sxs-lookup"><span data-stu-id="307b8-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="307b8-616">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-616">Minimum system</span></span> | <span data-ttu-id="307b8-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="307b8-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="307b8-618">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="307b8-618">SoapTypeName</span></span>



| <span data-ttu-id="307b8-619">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-619">Entry</span></span> | <span data-ttu-id="307b8-620">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-621">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-621">Description</span></span>    | <span data-ttu-id="307b8-622">O nome do tipo gerenciado para um componente que pode ser invocado como um serviço SOAP.</span><span class="sxs-lookup"><span data-stu-id="307b8-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="307b8-623">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-623">Access</span></span>         | <span data-ttu-id="307b8-624">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="307b8-625">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-625">Type</span></span>           | <span data-ttu-id="307b8-626">String</span><span class="sxs-lookup"><span data-stu-id="307b8-626">String</span></span>                                                                       |
| <span data-ttu-id="307b8-627">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-627">Default</span></span>        | <span data-ttu-id="307b8-628">NULO</span><span class="sxs-lookup"><span data-stu-id="307b8-628">NULL</span></span>                                                                         |
| <span data-ttu-id="307b8-629">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-629">Minimum system</span></span> | <span data-ttu-id="307b8-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="307b8-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="307b8-631">Sincronização</span><span class="sxs-lookup"><span data-stu-id="307b8-631">Synchronization</span></span>



| <span data-ttu-id="307b8-632">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-632">Entry</span></span> | <span data-ttu-id="307b8-633">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-634">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-634">Description</span></span>    | <span data-ttu-id="307b8-635">Determina a [sincronização](setting-the-synchronization-attribute.md) de chamadas para o componente.</span><span class="sxs-lookup"><span data-stu-id="307b8-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="307b8-636">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-636">Access</span></span>         | <span data-ttu-id="307b8-637">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="307b8-638">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-638">Type</span></span>           | <span data-ttu-id="307b8-639">Valores longos possíveis: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="307b8-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="307b8-640">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-640">Default</span></span>        | <span data-ttu-id="307b8-641">COMAdminSynchronizationIgnored (0)</span><span class="sxs-lookup"><span data-stu-id="307b8-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="307b8-642">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-642">Minimum system</span></span> | <span data-ttu-id="307b8-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="307b8-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="307b8-644">ThreadingModel</span></span>



| <span data-ttu-id="307b8-645">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-645">Entry</span></span> | <span data-ttu-id="307b8-646">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-647">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-647">Description</span></span>    | <span data-ttu-id="307b8-648">Determina como as instâncias do componente são atribuídas a threads para execução do método.</span><span class="sxs-lookup"><span data-stu-id="307b8-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="307b8-649">Os valores correspondem aos modelos de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="307b8-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="307b8-650">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-650">Access</span></span>         | <span data-ttu-id="307b8-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="307b8-652">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-652">Type</span></span>           | <span data-ttu-id="307b8-653">Valores longos possíveis: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)</span><span class="sxs-lookup"><span data-stu-id="307b8-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="307b8-654">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-654">Default</span></span>        | <span data-ttu-id="307b8-655">N/D</span><span class="sxs-lookup"><span data-stu-id="307b8-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="307b8-656">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-656">Minimum system</span></span> | <span data-ttu-id="307b8-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="307b8-658">Transação</span><span class="sxs-lookup"><span data-stu-id="307b8-658">Transaction</span></span>



| <span data-ttu-id="307b8-659">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-659">Entry</span></span> | <span data-ttu-id="307b8-660">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-661">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-661">Description</span></span>    | <span data-ttu-id="307b8-662">Determina como um componente dá suporte a [Transações](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="307b8-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="307b8-663">É recomendável que você use as constantes na enumeração e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="307b8-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="307b8-664">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-664">Access</span></span>         | <span data-ttu-id="307b8-665">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="307b8-666">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-666">Type</span></span>           | <span data-ttu-id="307b8-667">Valores longos possíveis: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="307b8-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="307b8-668">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-668">Default</span></span>        | <span data-ttu-id="307b8-669">COMAdminTransactionNone (1)</span><span class="sxs-lookup"><span data-stu-id="307b8-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="307b8-670">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-670">Minimum system</span></span> | <span data-ttu-id="307b8-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="307b8-672">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="307b8-672">TxIsolationLevel</span></span>



| <span data-ttu-id="307b8-673">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-673">Entry</span></span> | <span data-ttu-id="307b8-674">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b8-675">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-675">Description</span></span>    | <span data-ttu-id="307b8-676">Indica os níveis de isolamento da transação.</span><span class="sxs-lookup"><span data-stu-id="307b8-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="307b8-677">Há cinco níveis de isolamento: nenhum, leitura não confirmada, leitura confirmada, leitura repetida e serializada.</span><span class="sxs-lookup"><span data-stu-id="307b8-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="307b8-678">O nível de isolamento padrão é serializado.</span><span class="sxs-lookup"><span data-stu-id="307b8-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="307b8-679">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-679">Access</span></span>         | <span data-ttu-id="307b8-680">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="307b8-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="307b8-681">Tipo</span><span class="sxs-lookup"><span data-stu-id="307b8-681">Type</span></span>           | <span data-ttu-id="307b8-682">Valores longos possíveis: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="307b8-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="307b8-683">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-683">Default</span></span>        | <span data-ttu-id="307b8-684">COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="307b8-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="307b8-685">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-685">Minimum system</span></span> | <span data-ttu-id="307b8-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="307b8-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="307b8-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="307b8-687">VersionBuild</span></span>



| <span data-ttu-id="307b8-688">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-688">Entry</span></span> | <span data-ttu-id="307b8-689">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="307b8-690">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-690">Description</span></span>    | <span data-ttu-id="307b8-691">Identificador de compilação da versão.</span><span class="sxs-lookup"><span data-stu-id="307b8-691">Version build identifier.</span></span> |
| <span data-ttu-id="307b8-692">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-692">Access</span></span>         | <span data-ttu-id="307b8-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-693">ReadOnly</span></span>                  |
| <span data-ttu-id="307b8-694">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-694">Type</span></span>           | <span data-ttu-id="307b8-695">String</span><span class="sxs-lookup"><span data-stu-id="307b8-695">String</span></span>                    |
| <span data-ttu-id="307b8-696">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-696">Default</span></span>        | <span data-ttu-id="307b8-697">""</span><span class="sxs-lookup"><span data-stu-id="307b8-697">""</span></span>                        |
| <span data-ttu-id="307b8-698">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-698">Minimum system</span></span> | <span data-ttu-id="307b8-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="307b8-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="307b8-700">VersionMajor</span></span>



| <span data-ttu-id="307b8-701">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-701">Entry</span></span> | <span data-ttu-id="307b8-702">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="307b8-703">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-703">Description</span></span>    | <span data-ttu-id="307b8-704">Identificador de versão.</span><span class="sxs-lookup"><span data-stu-id="307b8-704">Version identifier.</span></span> |
| <span data-ttu-id="307b8-705">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-705">Access</span></span>         | <span data-ttu-id="307b8-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-706">ReadOnly</span></span>            |
| <span data-ttu-id="307b8-707">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-707">Type</span></span>           | <span data-ttu-id="307b8-708">String</span><span class="sxs-lookup"><span data-stu-id="307b8-708">String</span></span>              |
| <span data-ttu-id="307b8-709">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-709">Default</span></span>        | <span data-ttu-id="307b8-710">""</span><span class="sxs-lookup"><span data-stu-id="307b8-710">""</span></span>                  |
| <span data-ttu-id="307b8-711">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-711">Minimum system</span></span> | <span data-ttu-id="307b8-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="307b8-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="307b8-713">VersionMinor</span></span>



| <span data-ttu-id="307b8-714">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-714">Entry</span></span> | <span data-ttu-id="307b8-715">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="307b8-716">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-716">Description</span></span>    | <span data-ttu-id="307b8-717">Subidentificador de versão.</span><span class="sxs-lookup"><span data-stu-id="307b8-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="307b8-718">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-718">Access</span></span>         | <span data-ttu-id="307b8-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-719">ReadOnly</span></span>                |
| <span data-ttu-id="307b8-720">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-720">Type</span></span>           | <span data-ttu-id="307b8-721">String</span><span class="sxs-lookup"><span data-stu-id="307b8-721">String</span></span>                  |
| <span data-ttu-id="307b8-722">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-722">Default</span></span>        | <span data-ttu-id="307b8-723">""</span><span class="sxs-lookup"><span data-stu-id="307b8-723">""</span></span>                      |
| <span data-ttu-id="307b8-724">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-724">Minimum system</span></span> | <span data-ttu-id="307b8-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="307b8-726">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="307b8-726">VersionSubBuild</span></span>



| <span data-ttu-id="307b8-727">Entrada</span><span class="sxs-lookup"><span data-stu-id="307b8-727">Entry</span></span> | <span data-ttu-id="307b8-728">Valor</span><span class="sxs-lookup"><span data-stu-id="307b8-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="307b8-729">Descrição</span><span class="sxs-lookup"><span data-stu-id="307b8-729">Description</span></span>    | <span data-ttu-id="307b8-730">Identificador de subcompilação de versão.</span><span class="sxs-lookup"><span data-stu-id="307b8-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="307b8-731">Access</span><span class="sxs-lookup"><span data-stu-id="307b8-731">Access</span></span>         | <span data-ttu-id="307b8-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="307b8-732">ReadOnly</span></span>                      |
| <span data-ttu-id="307b8-733">Type</span><span class="sxs-lookup"><span data-stu-id="307b8-733">Type</span></span>           | <span data-ttu-id="307b8-734">String</span><span class="sxs-lookup"><span data-stu-id="307b8-734">String</span></span>                        |
| <span data-ttu-id="307b8-735">Padrão</span><span class="sxs-lookup"><span data-stu-id="307b8-735">Default</span></span>        | <span data-ttu-id="307b8-736">""</span><span class="sxs-lookup"><span data-stu-id="307b8-736">""</span></span>                            |
| <span data-ttu-id="307b8-737">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="307b8-737">Minimum system</span></span> | <span data-ttu-id="307b8-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307b8-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="307b8-739">Confira também</span><span class="sxs-lookup"><span data-stu-id="307b8-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307b8-740">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="307b8-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
