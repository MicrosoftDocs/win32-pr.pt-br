---
description: Contém um único objeto que corresponde ao computador cujo catálogo você está acessando. Esse objeto contém informações de configurações no nível do computador.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Coleção de LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646524"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="772cf-104">Coleção de LocalComputer</span><span class="sxs-lookup"><span data-stu-id="772cf-104">LocalComputer collection</span></span>

<span data-ttu-id="772cf-105">Contém um único objeto que corresponde ao computador cujo catálogo você está acessando.</span><span class="sxs-lookup"><span data-stu-id="772cf-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="772cf-106">Esse objeto contém informações de configurações no nível do computador.</span><span class="sxs-lookup"><span data-stu-id="772cf-106">This object holds computer level settings information.</span></span> <span data-ttu-id="772cf-107">Se você chamar o método [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) em um objeto criado a partir da classe [**COMAdminCatalog**](comadmincatalog.md) , o objeto na coleção **LocalComputer** conterá informações sobre o computador remoto cujo catálogo você está acessando.</span><span class="sxs-lookup"><span data-stu-id="772cf-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="772cf-108">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="772cf-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="772cf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="772cf-109">Members</span></span>

<span data-ttu-id="772cf-110">A coleção **LocalComputer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="772cf-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="772cf-111">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="772cf-111">Related Collections</span></span>

<span data-ttu-id="772cf-112">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="772cf-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="772cf-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="772cf-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="772cf-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="772cf-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="772cf-115">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="772cf-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="772cf-116">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="772cf-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="772cf-117">**Básica**</span><span class="sxs-lookup"><span data-stu-id="772cf-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="772cf-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="772cf-118">Properties</span></span>

<span data-ttu-id="772cf-119">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="772cf-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="772cf-120">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="772cf-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="772cf-121">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="772cf-122">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="772cf-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="772cf-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="772cf-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="772cf-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="772cf-125">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="772cf-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="772cf-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-126">Description</span></span>](#description)
-   [<span data-ttu-id="772cf-127">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="772cf-128">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="772cf-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="772cf-129">Isroteador</span><span class="sxs-lookup"><span data-stu-id="772cf-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="772cf-130">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="772cf-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="772cf-131">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="772cf-132">Nome</span><span class="sxs-lookup"><span data-stu-id="772cf-132">Name</span></span>](#name)
-   [<span data-ttu-id="772cf-133">Operacional</span><span class="sxs-lookup"><span data-stu-id="772cf-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="772cf-134">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="772cf-135">Portas</span><span class="sxs-lookup"><span data-stu-id="772cf-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="772cf-136">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="772cf-137">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="772cf-138">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="772cf-139">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="772cf-140">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="772cf-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="772cf-141">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="772cf-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="772cf-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="772cf-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="772cf-143">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="772cf-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="772cf-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-144">Entry</span></span> | <span data-ttu-id="772cf-145">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="772cf-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-146">Description</span></span>    | <span data-ttu-id="772cf-147">Nome do servidor remoto usado por proxies de aplicativo por padrão.</span><span class="sxs-lookup"><span data-stu-id="772cf-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="772cf-148">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-148">Access</span></span>         | <span data-ttu-id="772cf-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="772cf-150">Type</span><span class="sxs-lookup"><span data-stu-id="772cf-150">Type</span></span>           | <span data-ttu-id="772cf-151">String</span><span class="sxs-lookup"><span data-stu-id="772cf-151">String</span></span>                                                     |
| <span data-ttu-id="772cf-152">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-152">Default</span></span>        | <span data-ttu-id="772cf-153">""</span><span class="sxs-lookup"><span data-stu-id="772cf-153">""</span></span>                                                         |
| <span data-ttu-id="772cf-154">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-154">Minimum system</span></span> | <span data-ttu-id="772cf-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="772cf-156">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-156">CISEnabled</span></span>



| <span data-ttu-id="772cf-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-157">Entry</span></span> | <span data-ttu-id="772cf-158">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="772cf-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-159">Description</span></span>    | <span data-ttu-id="772cf-160">Indica se os serviços da Internet COM estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="772cf-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="772cf-161">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-161">Access</span></span>         | <span data-ttu-id="772cf-162">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="772cf-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-163">Type</span></span>           | <span data-ttu-id="772cf-164">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-164">Bool</span></span>                                                |
| <span data-ttu-id="772cf-165">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-165">Default</span></span>        | <span data-ttu-id="772cf-166">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-166">False</span></span>                                               |
| <span data-ttu-id="772cf-167">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-167">Minimum system</span></span> | <span data-ttu-id="772cf-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="772cf-169">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-169">DCOMEnabled</span></span>



| <span data-ttu-id="772cf-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-170">Entry</span></span> | <span data-ttu-id="772cf-171">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="772cf-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-172">Description</span></span>    | <span data-ttu-id="772cf-173">Defina como true para habilitar o DCOM no computador.</span><span class="sxs-lookup"><span data-stu-id="772cf-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="772cf-174">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-174">Access</span></span>         | <span data-ttu-id="772cf-175">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="772cf-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-176">Type</span></span>           | <span data-ttu-id="772cf-177">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-177">Bool</span></span>                                        |
| <span data-ttu-id="772cf-178">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-178">Default</span></span>        | <span data-ttu-id="772cf-179">True</span><span class="sxs-lookup"><span data-stu-id="772cf-179">True</span></span>                                        |
| <span data-ttu-id="772cf-180">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-180">Minimum system</span></span> | <span data-ttu-id="772cf-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="772cf-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="772cf-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="772cf-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-183">Entry</span></span> | <span data-ttu-id="772cf-184">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-185">Description</span></span>    | <span data-ttu-id="772cf-186">Nível de autenticação usado por aplicativos que têm a autenticação definida como padrão.</span><span class="sxs-lookup"><span data-stu-id="772cf-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="772cf-187">Os valores correspondem às configurações de autenticação RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="772cf-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="772cf-188">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-188">Access</span></span>         | <span data-ttu-id="772cf-189">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="772cf-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-190">Type</span></span>           | <span data-ttu-id="772cf-191">Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="772cf-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="772cf-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-192">Default</span></span>        | <span data-ttu-id="772cf-193">COMAdminAuthenticationConnect (2)</span><span class="sxs-lookup"><span data-stu-id="772cf-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="772cf-194">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-194">Minimum system</span></span> | <span data-ttu-id="772cf-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="772cf-196">COMAdminAuthenticationDefault é mapeado para COMAdminAuthenticationConnect quando o COM chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="772cf-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="772cf-197">É recomendável que você use as constantes na enumeração e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="772cf-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="772cf-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="772cf-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="772cf-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-199">Entry</span></span> | <span data-ttu-id="772cf-200">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-201">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-201">Description</span></span>    | <span data-ttu-id="772cf-202">Nível de representação para permitir se um não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="772cf-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="772cf-203">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-203">Access</span></span>         | <span data-ttu-id="772cf-204">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="772cf-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-205">Type</span></span>           | <span data-ttu-id="772cf-206">Valores longos possíveis: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="772cf-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="772cf-207">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-207">Default</span></span>        | <span data-ttu-id="772cf-208">COMAdminImpersonationIdentify (2)</span><span class="sxs-lookup"><span data-stu-id="772cf-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="772cf-209">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-209">Minimum system</span></span> | <span data-ttu-id="772cf-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="772cf-211">É recomendável que você use as constantes na enumeração, e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="772cf-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="772cf-212">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="772cf-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="772cf-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-213">Entry</span></span> | <span data-ttu-id="772cf-214">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-215">Description</span></span>    | <span data-ttu-id="772cf-216">Determina se o tipo de porta padrão fornecido deve ser Internet (true) ou intranet (false).</span><span class="sxs-lookup"><span data-stu-id="772cf-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="772cf-217">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-217">Access</span></span>         | <span data-ttu-id="772cf-218">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="772cf-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-219">Type</span></span>           | <span data-ttu-id="772cf-220">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="772cf-221">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-221">Default</span></span>        | <span data-ttu-id="772cf-222">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-222">False</span></span>                                                                                               |
| <span data-ttu-id="772cf-223">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-223">Minimum system</span></span> | <span data-ttu-id="772cf-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="772cf-225">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-225">Description</span></span>



| <span data-ttu-id="772cf-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-226">Entry</span></span> | <span data-ttu-id="772cf-227">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="772cf-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-228">Description</span></span>    | <span data-ttu-id="772cf-229">Uma descrição do computador.</span><span class="sxs-lookup"><span data-stu-id="772cf-229">A description of the computer.</span></span> |
| <span data-ttu-id="772cf-230">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-230">Access</span></span>         | <span data-ttu-id="772cf-231">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-231">ReadWrite</span></span>                      |
| <span data-ttu-id="772cf-232">Type</span><span class="sxs-lookup"><span data-stu-id="772cf-232">Type</span></span>           | <span data-ttu-id="772cf-233">String</span><span class="sxs-lookup"><span data-stu-id="772cf-233">String</span></span>                         |
| <span data-ttu-id="772cf-234">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-234">Default</span></span>        | <span data-ttu-id="772cf-235">""</span><span class="sxs-lookup"><span data-stu-id="772cf-235">""</span></span>                             |
| <span data-ttu-id="772cf-236">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-236">Minimum system</span></span> | <span data-ttu-id="772cf-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="772cf-238">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="772cf-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-239">Entry</span></span> | <span data-ttu-id="772cf-240">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-241">Description</span></span>    | <span data-ttu-id="772cf-242">Indica se o usuário dos mapeamentos de partição é verificado no repositório de domínio.</span><span class="sxs-lookup"><span data-stu-id="772cf-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="772cf-243">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-243">Access</span></span>         | <span data-ttu-id="772cf-244">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="772cf-245">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-245">Type</span></span>           | <span data-ttu-id="772cf-246">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="772cf-247">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-247">Default</span></span>        | <span data-ttu-id="772cf-248">True</span><span class="sxs-lookup"><span data-stu-id="772cf-248">True</span></span>                                                                                   |
| <span data-ttu-id="772cf-249">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-249">Minimum system</span></span> | <span data-ttu-id="772cf-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="772cf-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="772cf-251">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="772cf-251">InternetPortsListed</span></span>



| <span data-ttu-id="772cf-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-252">Entry</span></span> | <span data-ttu-id="772cf-253">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-254">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-254">Description</span></span>    | <span data-ttu-id="772cf-255">Determina se as portas listadas na propriedade portas devem ser usadas para Internet (true) ou para intranet (false).</span><span class="sxs-lookup"><span data-stu-id="772cf-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="772cf-256">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-256">Access</span></span>         | <span data-ttu-id="772cf-257">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="772cf-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-258">Type</span></span>           | <span data-ttu-id="772cf-259">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="772cf-260">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-260">Default</span></span>        | <span data-ttu-id="772cf-261">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="772cf-262">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-262">Minimum system</span></span> | <span data-ttu-id="772cf-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="772cf-264">Isroteador</span><span class="sxs-lookup"><span data-stu-id="772cf-264">IsRouter</span></span>



| <span data-ttu-id="772cf-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-265">Entry</span></span> | <span data-ttu-id="772cf-266">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-267">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-267">Description</span></span>    | <span data-ttu-id="772cf-268">Defina como true se o computador for um roteador para o serviço CLB (balanceamento de carga do componente).</span><span class="sxs-lookup"><span data-stu-id="772cf-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="772cf-269">Essa propriedade pode ser definida como true somente se o serviço de balanceamento de carga do componente estiver atualmente instalado no computador; caso contrário, os erros de ti com COMAdmin \_ E \_ exigirão uma \_ \_ plataforma diferente.</span><span class="sxs-lookup"><span data-stu-id="772cf-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="772cf-270">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-270">Access</span></span>         | <span data-ttu-id="772cf-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="772cf-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-272">Type</span></span>           | <span data-ttu-id="772cf-273">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="772cf-274">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-274">Default</span></span>        | <span data-ttu-id="772cf-275">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="772cf-276">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-276">Minimum system</span></span> | <span data-ttu-id="772cf-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="772cf-278">Se essa propriedade for definida como true, o servidor CLB será configurado e começará na inicialização.</span><span class="sxs-lookup"><span data-stu-id="772cf-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="772cf-279">O servidor será adicionado à coleção ApplicationCluster se ainda não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="772cf-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="772cf-280">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="772cf-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="772cf-281">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-281">Entry</span></span> | <span data-ttu-id="772cf-282">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="772cf-283">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-283">Description</span></span>    | <span data-ttu-id="772cf-284">O CLSID do objeto a ser balanceado.</span><span class="sxs-lookup"><span data-stu-id="772cf-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="772cf-285">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-285">Access</span></span>         | <span data-ttu-id="772cf-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-286">ReadWrite</span></span>                           |
| <span data-ttu-id="772cf-287">Type</span><span class="sxs-lookup"><span data-stu-id="772cf-287">Type</span></span>           | <span data-ttu-id="772cf-288">String</span><span class="sxs-lookup"><span data-stu-id="772cf-288">String</span></span>                              |
| <span data-ttu-id="772cf-289">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-289">Default</span></span>        | <span data-ttu-id="772cf-290">NULO</span><span class="sxs-lookup"><span data-stu-id="772cf-290">NULL</span></span>                                |
| <span data-ttu-id="772cf-291">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-291">Minimum system</span></span> | <span data-ttu-id="772cf-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="772cf-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="772cf-293">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="772cf-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-294">Entry</span></span> | <span data-ttu-id="772cf-295">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-296">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-296">Description</span></span>    | <span data-ttu-id="772cf-297">Indica se o usuário dos mapeamentos de partição é verificado no repositório local.</span><span class="sxs-lookup"><span data-stu-id="772cf-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="772cf-298">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-298">Access</span></span>         | <span data-ttu-id="772cf-299">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="772cf-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-300">Type</span></span>           | <span data-ttu-id="772cf-301">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="772cf-302">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-302">Default</span></span>        | <span data-ttu-id="772cf-303">True</span><span class="sxs-lookup"><span data-stu-id="772cf-303">True</span></span>                                                                                  |
| <span data-ttu-id="772cf-304">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-304">Minimum system</span></span> | <span data-ttu-id="772cf-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="772cf-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="772cf-306">Nome</span><span class="sxs-lookup"><span data-stu-id="772cf-306">Name</span></span>



| <span data-ttu-id="772cf-307">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-307">Entry</span></span> | <span data-ttu-id="772cf-308">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-309">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-309">Description</span></span>    | <span data-ttu-id="772cf-310">O nome do computador.</span><span class="sxs-lookup"><span data-stu-id="772cf-310">The name of the computer.</span></span> <span data-ttu-id="772cf-311">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="772cf-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="772cf-312">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-312">Access</span></span>         | <span data-ttu-id="772cf-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="772cf-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="772cf-314">Type</span><span class="sxs-lookup"><span data-stu-id="772cf-314">Type</span></span>           | <span data-ttu-id="772cf-315">String</span><span class="sxs-lookup"><span data-stu-id="772cf-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="772cf-316">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-316">Default</span></span>        | <span data-ttu-id="772cf-317">"Meu Computador"</span><span class="sxs-lookup"><span data-stu-id="772cf-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="772cf-318">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-318">Minimum system</span></span> | <span data-ttu-id="772cf-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="772cf-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="772cf-320">OperatingSystem</span></span>



| <span data-ttu-id="772cf-321">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-321">Entry</span></span> | <span data-ttu-id="772cf-322">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-323">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-323">Description</span></span>    | <span data-ttu-id="772cf-324">O sistema operacional instalado no computador local.</span><span class="sxs-lookup"><span data-stu-id="772cf-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="772cf-325">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-325">Access</span></span>         | <span data-ttu-id="772cf-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="772cf-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-327">Type</span></span>           | <span data-ttu-id="772cf-328">Valores longos possíveis: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)</span><span class="sxs-lookup"><span data-stu-id="772cf-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="772cf-329">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-329">Default</span></span>        | <span data-ttu-id="772cf-330">COMAdminOSNotInitialized (0)</span><span class="sxs-lookup"><span data-stu-id="772cf-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="772cf-331">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-331">Minimum system</span></span> | <span data-ttu-id="772cf-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="772cf-333">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-333">PartitionsEnabled</span></span>



| <span data-ttu-id="772cf-334">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-334">Entry</span></span> | <span data-ttu-id="772cf-335">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-336">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-336">Description</span></span>    | <span data-ttu-id="772cf-337">Indica se as partições COM+ podem ser usadas no computador local.</span><span class="sxs-lookup"><span data-stu-id="772cf-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="772cf-338">Se essa propriedade for falsa, qualquer tentativa de usar partições COM+ resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="772cf-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="772cf-339">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-339">Access</span></span>         | <span data-ttu-id="772cf-340">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="772cf-341">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-341">Type</span></span>           | <span data-ttu-id="772cf-342">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="772cf-343">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-343">Default</span></span>        | <span data-ttu-id="772cf-344">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="772cf-345">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-345">Minimum system</span></span> | <span data-ttu-id="772cf-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="772cf-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="772cf-347">Portas</span><span class="sxs-lookup"><span data-stu-id="772cf-347">Ports</span></span>



| <span data-ttu-id="772cf-348">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-348">Entry</span></span> | <span data-ttu-id="772cf-349">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-350">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-350">Description</span></span>    | <span data-ttu-id="772cf-351">Uma cadeia de caracteres que descreve as portas que são usadas para a Internet ou intranet, dependendo da propriedade InternetPortsListed; por exemplo, "500-599:600-800".</span><span class="sxs-lookup"><span data-stu-id="772cf-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="772cf-352">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-352">Access</span></span>         | <span data-ttu-id="772cf-353">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="772cf-354">Type</span><span class="sxs-lookup"><span data-stu-id="772cf-354">Type</span></span>           | <span data-ttu-id="772cf-355">String</span><span class="sxs-lookup"><span data-stu-id="772cf-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="772cf-356">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-356">Default</span></span>        | <span data-ttu-id="772cf-357">""</span><span class="sxs-lookup"><span data-stu-id="772cf-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="772cf-358">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-358">Minimum system</span></span> | <span data-ttu-id="772cf-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="772cf-360">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="772cf-361">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-361">Entry</span></span> | <span data-ttu-id="772cf-362">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="772cf-363">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-363">Description</span></span>    | <span data-ttu-id="772cf-364">Habilita o uso de dispensadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="772cf-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="772cf-365">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-365">Access</span></span>         | <span data-ttu-id="772cf-366">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-366">ReadWrite</span></span>                           |
| <span data-ttu-id="772cf-367">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-367">Type</span></span>           | <span data-ttu-id="772cf-368">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-368">Bool</span></span>                                |
| <span data-ttu-id="772cf-369">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-369">Default</span></span>        | <span data-ttu-id="772cf-370">True</span><span class="sxs-lookup"><span data-stu-id="772cf-370">True</span></span>                                |
| <span data-ttu-id="772cf-371">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-371">Minimum system</span></span> | <span data-ttu-id="772cf-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="772cf-373">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="772cf-374">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-374">Entry</span></span> | <span data-ttu-id="772cf-375">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-376">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-376">Description</span></span>    | <span data-ttu-id="772cf-377">Controla se o proxy RPC do IIS está habilitado.</span><span class="sxs-lookup"><span data-stu-id="772cf-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="772cf-378">O proxy RPC do IIS é usado em conjunto com o IIS para encaminhar chamadas para o mecanismo RPC do IIS e é uma das partes principais dos serviços de Internet COM, que é habilitada definindo CISEnabled como true.</span><span class="sxs-lookup"><span data-stu-id="772cf-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="772cf-379">Para obter mais informações sobre o RPCProxyEnabled, consulte [segurança http RPC](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="772cf-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="772cf-380">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-380">Access</span></span>         | <span data-ttu-id="772cf-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="772cf-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-382">Type</span></span>           | <span data-ttu-id="772cf-383">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="772cf-384">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-384">Default</span></span>        | <span data-ttu-id="772cf-385">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="772cf-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-386">Minimum system</span></span> | <span data-ttu-id="772cf-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="772cf-388">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="772cf-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-389">Entry</span></span> | <span data-ttu-id="772cf-390">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-391">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-391">Description</span></span>    | <span data-ttu-id="772cf-392">Impõe em computadores DCOM que as chamadas entre processos para os métodos [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) são protegidas.</span><span class="sxs-lookup"><span data-stu-id="772cf-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="772cf-393">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-393">Access</span></span>         | <span data-ttu-id="772cf-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="772cf-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-395">Type</span></span>           | <span data-ttu-id="772cf-396">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="772cf-397">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-397">Default</span></span>        | <span data-ttu-id="772cf-398">Falso</span><span class="sxs-lookup"><span data-stu-id="772cf-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="772cf-399">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-399">Minimum system</span></span> | <span data-ttu-id="772cf-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="772cf-401">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="772cf-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="772cf-402">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-402">Entry</span></span> | <span data-ttu-id="772cf-403">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="772cf-404">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-404">Description</span></span>    | <span data-ttu-id="772cf-405">Defina como verdadeiro se o rastreamento de segurança estiver habilitado em objetos.</span><span class="sxs-lookup"><span data-stu-id="772cf-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="772cf-406">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-406">Access</span></span>         | <span data-ttu-id="772cf-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="772cf-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-408">Type</span></span>           | <span data-ttu-id="772cf-409">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-409">Bool</span></span>                                                    |
| <span data-ttu-id="772cf-410">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-410">Default</span></span>        | <span data-ttu-id="772cf-411">True</span><span class="sxs-lookup"><span data-stu-id="772cf-411">True</span></span>                                                    |
| <span data-ttu-id="772cf-412">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-412">Minimum system</span></span> | <span data-ttu-id="772cf-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="772cf-414">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="772cf-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="772cf-415">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-415">Entry</span></span> | <span data-ttu-id="772cf-416">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-417">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-417">Description</span></span>    | <span data-ttu-id="772cf-418">Determina como a diretiva de restrição de software (SRP) lida com conexões Activate as-Activator.</span><span class="sxs-lookup"><span data-stu-id="772cf-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="772cf-419">Se definido como true, o nível de confiança SRP configurado para o objeto Server é comparado com o nível de confiança SRP do objeto Client e o nível de confiança superior (mais estrito) é usado para executar o objeto Server.</span><span class="sxs-lookup"><span data-stu-id="772cf-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="772cf-420">Se definido como false, o objeto Server é executado com o nível de confiança SRP do objeto Client, independentemente do nível de confiança SRP com o qual o servidor está configurado.</span><span class="sxs-lookup"><span data-stu-id="772cf-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="772cf-421">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-421">Access</span></span>         | <span data-ttu-id="772cf-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="772cf-423">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-423">Type</span></span>           | <span data-ttu-id="772cf-424">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="772cf-425">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-425">Default</span></span>        | <span data-ttu-id="772cf-426">True</span><span class="sxs-lookup"><span data-stu-id="772cf-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="772cf-427">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-427">Minimum system</span></span> | <span data-ttu-id="772cf-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="772cf-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="772cf-429">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="772cf-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="772cf-430">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-430">Entry</span></span> | <span data-ttu-id="772cf-431">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-432">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-432">Description</span></span>    | <span data-ttu-id="772cf-433">Determina como a política de restrição de software (SRP) trata tentativas de conexões com os processos existentes.</span><span class="sxs-lookup"><span data-stu-id="772cf-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="772cf-434">Se definido como false, as tentativas de conexão com objetos em execução não serão verificadas em relação aos níveis de confiança do SRP apropriados.</span><span class="sxs-lookup"><span data-stu-id="772cf-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="772cf-435">Se definido como true, o objeto em execução deverá ter um nível de confiança do SRP igual ou maior (mais estrito) do que o objeto do cliente.</span><span class="sxs-lookup"><span data-stu-id="772cf-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="772cf-436">Por exemplo, um objeto de cliente com um nível de confiança SRP irrestrito não pode se conectar a um objeto em execução com um nível de confiança SRP não permitido.</span><span class="sxs-lookup"><span data-stu-id="772cf-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="772cf-437">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-437">Access</span></span>         | <span data-ttu-id="772cf-438">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="772cf-439">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-439">Type</span></span>           | <span data-ttu-id="772cf-440">Bool</span><span class="sxs-lookup"><span data-stu-id="772cf-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="772cf-441">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-441">Default</span></span>        | <span data-ttu-id="772cf-442">True</span><span class="sxs-lookup"><span data-stu-id="772cf-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="772cf-443">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-443">Minimum system</span></span> | <span data-ttu-id="772cf-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="772cf-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="772cf-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="772cf-445">TransactionTimeout</span></span>



| <span data-ttu-id="772cf-446">Entrada</span><span class="sxs-lookup"><span data-stu-id="772cf-446">Entry</span></span> | <span data-ttu-id="772cf-447">Valor</span><span class="sxs-lookup"><span data-stu-id="772cf-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772cf-448">Descrição</span><span class="sxs-lookup"><span data-stu-id="772cf-448">Description</span></span>    | <span data-ttu-id="772cf-449">Deve ser definido como um valor suficiente em segundos se você estiver fazendo várias operações em uma transação.</span><span class="sxs-lookup"><span data-stu-id="772cf-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="772cf-450">O período de tempo limite padrão é de 60 segundos e o período de tempo limite máximo é de 3600 segundos (1 hora).</span><span class="sxs-lookup"><span data-stu-id="772cf-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="772cf-451">A definição dessa propriedade como 0 desabilita o tempo limite da transação.</span><span class="sxs-lookup"><span data-stu-id="772cf-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="772cf-452">Essa propriedade pode ser substituída por componentes individuais usando a propriedade ComponentTransactionTimeout da coleção [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="772cf-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="772cf-453">Access</span><span class="sxs-lookup"><span data-stu-id="772cf-453">Access</span></span>         | <span data-ttu-id="772cf-454">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="772cf-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="772cf-455">Tipo</span><span class="sxs-lookup"><span data-stu-id="772cf-455">Type</span></span>           | <span data-ttu-id="772cf-456">Longo (0-3600)</span><span class="sxs-lookup"><span data-stu-id="772cf-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="772cf-457">Padrão</span><span class="sxs-lookup"><span data-stu-id="772cf-457">Default</span></span>        | <span data-ttu-id="772cf-458">60</span><span class="sxs-lookup"><span data-stu-id="772cf-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="772cf-459">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="772cf-459">Minimum system</span></span> | <span data-ttu-id="772cf-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="772cf-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="772cf-461">Exemplo</span><span class="sxs-lookup"><span data-stu-id="772cf-461">Example</span></span>

<span data-ttu-id="772cf-462">O exemplo a seguir da Microsoft Visual Basic demonstra como se conectar a um computador remoto e obter sua propriedade SecurityTrackingEnabled usando a coleção **LocalComputer** do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="772cf-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="772cf-463">Para usar este exemplo, adicione a biblioteca de tipos de administrador do COM+ como uma referência ao seu projeto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="772cf-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="772cf-464">Para usar a função, forneça um valor de cadeia de caracteres para o nome do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="772cf-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="772cf-465">O código de Visual Basic a seguir mostra como se conectar ao computador chamado "RemoteComputerName".</span><span class="sxs-lookup"><span data-stu-id="772cf-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="772cf-466">Confira também</span><span class="sxs-lookup"><span data-stu-id="772cf-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772cf-467">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="772cf-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
