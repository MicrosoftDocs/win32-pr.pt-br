---
description: Contém um objeto para cada componente não configurado na coleção de aplicativos. Os componentes não configurados não podem fazer uso de serviços COM+. As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Coleção LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646318"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="141df-105">Coleção LegacyComponents</span><span class="sxs-lookup"><span data-stu-id="141df-105">LegacyComponents collection</span></span>

<span data-ttu-id="141df-106">Contém um objeto para cada componente não configurado na coleção de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="141df-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="141df-107">Os componentes não configurados não podem fazer uso de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="141df-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="141df-108">As propriedades expostas por esses objetos mantêm as configurações feitas no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="141df-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="141df-109">Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="141df-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="141df-110">Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="141df-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="141df-111">Membros</span><span class="sxs-lookup"><span data-stu-id="141df-111">Members</span></span>

<span data-ttu-id="141df-112">A coleção **LegacyComponents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="141df-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="141df-113">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="141df-113">Related Collections</span></span>

<span data-ttu-id="141df-114">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="141df-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="141df-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="141df-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="141df-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="141df-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="141df-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="141df-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="141df-118">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="141df-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="141df-119">**Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="141df-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="141df-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="141df-120">Properties</span></span>

<span data-ttu-id="141df-121">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="141df-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="141df-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="141df-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="141df-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="141df-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="141df-124">AppID</span><span class="sxs-lookup"><span data-stu-id="141df-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="141df-125">AppName</span><span class="sxs-lookup"><span data-stu-id="141df-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="141df-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="141df-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="141df-127">Número de bits</span><span class="sxs-lookup"><span data-stu-id="141df-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="141df-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="141df-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="141df-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="141df-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="141df-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="141df-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="141df-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="141df-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="141df-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="141df-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="141df-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="141df-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="141df-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="141df-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="141df-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="141df-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="141df-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="141df-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="141df-137">Senha</span><span class="sxs-lookup"><span data-stu-id="141df-137">Password</span></span>](#password)
-   [<span data-ttu-id="141df-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="141df-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="141df-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="141df-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="141df-140">RunAs</span><span class="sxs-lookup"><span data-stu-id="141df-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="141df-141">Fileparameter</span><span class="sxs-lookup"><span data-stu-id="141df-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="141df-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="141df-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="141df-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="141df-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="141df-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="141df-144">AccessPermissions</span></span>



| <span data-ttu-id="141df-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-145">Entry</span></span> | <span data-ttu-id="141df-146">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="141df-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-147">Description</span></span>    | <span data-ttu-id="141df-148">Especifica as contas de usuário que têm o acesso permitido ou negado ao componente.</span><span class="sxs-lookup"><span data-stu-id="141df-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="141df-149">Access</span><span class="sxs-lookup"><span data-stu-id="141df-149">Access</span></span>         | <span data-ttu-id="141df-150">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="141df-151">Type</span><span class="sxs-lookup"><span data-stu-id="141df-151">Type</span></span>           | <span data-ttu-id="141df-152">String</span><span class="sxs-lookup"><span data-stu-id="141df-152">String</span></span>                                                                          |
| <span data-ttu-id="141df-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-153">Default</span></span>        | <span data-ttu-id="141df-154">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-154">N/A</span></span>                                                                             |
| <span data-ttu-id="141df-155">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-155">Minimum system</span></span> | <span data-ttu-id="141df-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="141df-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="141df-157">ActivateAtStorage</span></span>



| <span data-ttu-id="141df-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-158">Entry</span></span> | <span data-ttu-id="141df-159">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="141df-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-160">Description</span></span>    | <span data-ttu-id="141df-161">Especifica se o servidor deve ser executado no computador de armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="141df-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="141df-162">Access</span><span class="sxs-lookup"><span data-stu-id="141df-162">Access</span></span>         | <span data-ttu-id="141df-163">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="141df-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-164">Type</span></span>           | <span data-ttu-id="141df-165">Valores possíveis de cadeia de caracteres: "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="141df-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="141df-166">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-166">Default</span></span>        | <span data-ttu-id="141df-167">"N"</span><span class="sxs-lookup"><span data-stu-id="141df-167">"N"</span></span>                                                              |
| <span data-ttu-id="141df-168">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-168">Minimum system</span></span> | <span data-ttu-id="141df-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="141df-170">AppID</span><span class="sxs-lookup"><span data-stu-id="141df-170">AppID</span></span>



| <span data-ttu-id="141df-171">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-171">Entry</span></span> | <span data-ttu-id="141df-172">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="141df-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-173">Description</span></span>    | <span data-ttu-id="141df-174">A ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="141df-174">The application ID.</span></span> |
| <span data-ttu-id="141df-175">Access</span><span class="sxs-lookup"><span data-stu-id="141df-175">Access</span></span>         | <span data-ttu-id="141df-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-176">ReadOnly</span></span>            |
| <span data-ttu-id="141df-177">Type</span><span class="sxs-lookup"><span data-stu-id="141df-177">Type</span></span>           | <span data-ttu-id="141df-178">String</span><span class="sxs-lookup"><span data-stu-id="141df-178">String</span></span>              |
| <span data-ttu-id="141df-179">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-179">Default</span></span>        | <span data-ttu-id="141df-180">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-180">N/A</span></span>                 |
| <span data-ttu-id="141df-181">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-181">Minimum system</span></span> | <span data-ttu-id="141df-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="141df-183">AppName</span><span class="sxs-lookup"><span data-stu-id="141df-183">AppName</span></span>



| <span data-ttu-id="141df-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-184">Entry</span></span> | <span data-ttu-id="141df-185">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="141df-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-186">Description</span></span>    | <span data-ttu-id="141df-187">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="141df-187">The name of the application.</span></span> |
| <span data-ttu-id="141df-188">Access</span><span class="sxs-lookup"><span data-stu-id="141df-188">Access</span></span>         | <span data-ttu-id="141df-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-189">ReadOnly</span></span>                     |
| <span data-ttu-id="141df-190">Type</span><span class="sxs-lookup"><span data-stu-id="141df-190">Type</span></span>           | <span data-ttu-id="141df-191">String</span><span class="sxs-lookup"><span data-stu-id="141df-191">String</span></span>                       |
| <span data-ttu-id="141df-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-192">Default</span></span>        | <span data-ttu-id="141df-193">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-193">N/A</span></span>                          |
| <span data-ttu-id="141df-194">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-194">Minimum system</span></span> | <span data-ttu-id="141df-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="141df-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="141df-196">AuthenticationLevel</span></span>



| <span data-ttu-id="141df-197">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-197">Entry</span></span> | <span data-ttu-id="141df-198">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-199">Description</span></span>    | <span data-ttu-id="141df-200">Define o nível de autenticação para chamadas, com valores correspondentes às configurações de autenticação RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="141df-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="141df-201">Quando COMAdminAuthenticationDefault é escolhido, a configuração na propriedade DefaultAuthenticationLevel dentro da coleção [**LocalComputer**](localcomputer.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="141df-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="141df-202">Access</span><span class="sxs-lookup"><span data-stu-id="141df-202">Access</span></span>         | <span data-ttu-id="141df-203">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="141df-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-204">Type</span></span>           | <span data-ttu-id="141df-205">Valores longos possíveis: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="141df-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="141df-206">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-206">Default</span></span>        | <span data-ttu-id="141df-207">COMAdminAuthenticationDefault (0)</span><span class="sxs-lookup"><span data-stu-id="141df-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="141df-208">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-208">Minimum system</span></span> | <span data-ttu-id="141df-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="141df-210">É recomendável que você use as constantes na enumeração e não os valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="141df-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="141df-211">Número de bits</span><span class="sxs-lookup"><span data-stu-id="141df-211">Bitness</span></span>



| <span data-ttu-id="141df-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-212">Entry</span></span> | <span data-ttu-id="141df-213">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-214">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-214">Description</span></span>    | <span data-ttu-id="141df-215">Representa o tipo de bit de bits binário do componente.</span><span class="sxs-lookup"><span data-stu-id="141df-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="141df-216">Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="141df-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="141df-217">Access</span><span class="sxs-lookup"><span data-stu-id="141df-217">Access</span></span>         | <span data-ttu-id="141df-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="141df-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-219">Type</span></span>           | <span data-ttu-id="141df-220">Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="141df-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="141df-221">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-221">Default</span></span>        | <span data-ttu-id="141df-222">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="141df-223">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-223">Minimum system</span></span> | <span data-ttu-id="141df-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="141df-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="141df-225">ClassName</span></span>



| <span data-ttu-id="141df-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-226">Entry</span></span> | <span data-ttu-id="141df-227">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="141df-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-228">Description</span></span>    | <span data-ttu-id="141df-229">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="141df-229">The name of the class.</span></span> |
| <span data-ttu-id="141df-230">Access</span><span class="sxs-lookup"><span data-stu-id="141df-230">Access</span></span>         | <span data-ttu-id="141df-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-231">ReadOnly</span></span>               |
| <span data-ttu-id="141df-232">Type</span><span class="sxs-lookup"><span data-stu-id="141df-232">Type</span></span>           | <span data-ttu-id="141df-233">String</span><span class="sxs-lookup"><span data-stu-id="141df-233">String</span></span>                 |
| <span data-ttu-id="141df-234">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-234">Default</span></span>        | <span data-ttu-id="141df-235">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-235">N/A</span></span>                    |
| <span data-ttu-id="141df-236">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-236">Minimum system</span></span> | <span data-ttu-id="141df-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="141df-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="141df-238">CLSID</span></span>



| <span data-ttu-id="141df-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-239">Entry</span></span> | <span data-ttu-id="141df-240">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-241">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-241">Description</span></span>    | <span data-ttu-id="141df-242">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="141df-242">A GUID for the component.</span></span> <span data-ttu-id="141df-243">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="141df-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="141df-244">Access</span><span class="sxs-lookup"><span data-stu-id="141df-244">Access</span></span>         | <span data-ttu-id="141df-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="141df-246">Type</span><span class="sxs-lookup"><span data-stu-id="141df-246">Type</span></span>           | <span data-ttu-id="141df-247">String</span><span class="sxs-lookup"><span data-stu-id="141df-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="141df-248">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-248">Default</span></span>        | <span data-ttu-id="141df-249">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="141df-250">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-250">Minimum system</span></span> | <span data-ttu-id="141df-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="141df-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="141df-252">DllSurrogate</span></span>



| <span data-ttu-id="141df-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-253">Entry</span></span> | <span data-ttu-id="141df-254">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="141df-255">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-255">Description</span></span>    | <span data-ttu-id="141df-256">Especifica o caminho completo para um aplicativo de servidor surragate.</span><span class="sxs-lookup"><span data-stu-id="141df-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="141df-257">Access</span><span class="sxs-lookup"><span data-stu-id="141df-257">Access</span></span>         | <span data-ttu-id="141df-258">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="141df-259">Type</span><span class="sxs-lookup"><span data-stu-id="141df-259">Type</span></span>           | <span data-ttu-id="141df-260">String</span><span class="sxs-lookup"><span data-stu-id="141df-260">String</span></span>                                                     |
| <span data-ttu-id="141df-261">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-261">Default</span></span>        | <span data-ttu-id="141df-262">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-262">N/A</span></span>                                                        |
| <span data-ttu-id="141df-263">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-263">Minimum system</span></span> | <span data-ttu-id="141df-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="141df-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="141df-265">InprocHandler32</span></span>



| <span data-ttu-id="141df-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-266">Entry</span></span> | <span data-ttu-id="141df-267">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="141df-268">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-268">Description</span></span>    | <span data-ttu-id="141df-269">Especifica o caminho completo para uma DLL de manipulador personalizado em processo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="141df-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="141df-270">Access</span><span class="sxs-lookup"><span data-stu-id="141df-270">Access</span></span>         | <span data-ttu-id="141df-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="141df-272">Type</span><span class="sxs-lookup"><span data-stu-id="141df-272">Type</span></span>           | <span data-ttu-id="141df-273">String</span><span class="sxs-lookup"><span data-stu-id="141df-273">String</span></span>                                                             |
| <span data-ttu-id="141df-274">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-274">Default</span></span>        | <span data-ttu-id="141df-275">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-275">N/A</span></span>                                                                |
| <span data-ttu-id="141df-276">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-276">Minimum system</span></span> | <span data-ttu-id="141df-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="141df-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="141df-278">InprocServer32</span></span>



| <span data-ttu-id="141df-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-279">Entry</span></span> | <span data-ttu-id="141df-280">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="141df-281">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-281">Description</span></span>    | <span data-ttu-id="141df-282">Especifica o caminho completo para uma DLL de servidor em processo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="141df-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="141df-283">Access</span><span class="sxs-lookup"><span data-stu-id="141df-283">Access</span></span>         | <span data-ttu-id="141df-284">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="141df-285">Type</span><span class="sxs-lookup"><span data-stu-id="141df-285">Type</span></span>           | <span data-ttu-id="141df-286">String</span><span class="sxs-lookup"><span data-stu-id="141df-286">String</span></span>                                                     |
| <span data-ttu-id="141df-287">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-287">Default</span></span>        | <span data-ttu-id="141df-288">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-288">N/A</span></span>                                                        |
| <span data-ttu-id="141df-289">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-289">Minimum system</span></span> | <span data-ttu-id="141df-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="141df-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="141df-291">IsEnabled</span></span>



| <span data-ttu-id="141df-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-292">Entry</span></span> | <span data-ttu-id="141df-293">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-294">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-294">Description</span></span>    | <span data-ttu-id="141df-295">Se o aplicativo ou componente COM+ estiver desabilitado, IsEnabled será false.</span><span class="sxs-lookup"><span data-stu-id="141df-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="141df-296">Se o aplicativo ou componente COM+ estiver habilitado, IsEnabled será true.</span><span class="sxs-lookup"><span data-stu-id="141df-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="141df-297">Access</span><span class="sxs-lookup"><span data-stu-id="141df-297">Access</span></span>         | <span data-ttu-id="141df-298">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="141df-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-299">Type</span></span>           | <span data-ttu-id="141df-300">Bool</span><span class="sxs-lookup"><span data-stu-id="141df-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="141df-301">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-301">Default</span></span>        | <span data-ttu-id="141df-302">True</span><span class="sxs-lookup"><span data-stu-id="141df-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="141df-303">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-303">Minimum system</span></span> | <span data-ttu-id="141df-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="141df-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="141df-305">LaunchPermissions</span></span>



| <span data-ttu-id="141df-306">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-306">Entry</span></span> | <span data-ttu-id="141df-307">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-308">Description</span></span>    | <span data-ttu-id="141df-309">Especifica as contas de usuário que são permitidas ou com permissão negada para iniciar este componente.</span><span class="sxs-lookup"><span data-stu-id="141df-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="141df-310">Access</span><span class="sxs-lookup"><span data-stu-id="141df-310">Access</span></span>         | <span data-ttu-id="141df-311">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="141df-312">Type</span><span class="sxs-lookup"><span data-stu-id="141df-312">Type</span></span>           | <span data-ttu-id="141df-313">String</span><span class="sxs-lookup"><span data-stu-id="141df-313">String</span></span>                                                                                 |
| <span data-ttu-id="141df-314">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-314">Default</span></span>        | <span data-ttu-id="141df-315">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="141df-316">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-316">Minimum system</span></span> | <span data-ttu-id="141df-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="141df-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="141df-318">LocalServer32</span></span>



| <span data-ttu-id="141df-319">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-319">Entry</span></span> | <span data-ttu-id="141df-320">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-321">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-321">Description</span></span>    | <span data-ttu-id="141df-322">Especifica o caminho completo para um aplicativo de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="141df-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="141df-323">Para ajudar a proteger a segurança do sistema, use cadeias de caracteres entre aspas no caminho para indicar onde o nome do arquivo executável termina e os argumentos começam.</span><span class="sxs-lookup"><span data-stu-id="141df-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="141df-324">Por exemplo, " \\ C: \\ Program Files \\ arquivos da empresa \\Application.exe\\ " param1 param2 ".</span><span class="sxs-lookup"><span data-stu-id="141df-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="141df-325">Access</span><span class="sxs-lookup"><span data-stu-id="141df-325">Access</span></span>         | <span data-ttu-id="141df-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="141df-327">Type</span><span class="sxs-lookup"><span data-stu-id="141df-327">Type</span></span>           | <span data-ttu-id="141df-328">String</span><span class="sxs-lookup"><span data-stu-id="141df-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="141df-329">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-329">Default</span></span>        | <span data-ttu-id="141df-330">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="141df-331">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-331">Minimum system</span></span> | <span data-ttu-id="141df-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="141df-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="141df-333">LocalService</span></span>



| <span data-ttu-id="141df-334">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-334">Entry</span></span> | <span data-ttu-id="141df-335">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="141df-336">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-336">Description</span></span>    | <span data-ttu-id="141df-337">Especifica o caminho completo para o aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="141df-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="141df-338">Access</span><span class="sxs-lookup"><span data-stu-id="141df-338">Access</span></span>         | <span data-ttu-id="141df-339">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="141df-340">Type</span><span class="sxs-lookup"><span data-stu-id="141df-340">Type</span></span>           | <span data-ttu-id="141df-341">String</span><span class="sxs-lookup"><span data-stu-id="141df-341">String</span></span>                                              |
| <span data-ttu-id="141df-342">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-342">Default</span></span>        | <span data-ttu-id="141df-343">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-343">N/A</span></span>                                                 |
| <span data-ttu-id="141df-344">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-344">Minimum system</span></span> | <span data-ttu-id="141df-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="141df-346">Senha</span><span class="sxs-lookup"><span data-stu-id="141df-346">Password</span></span>



| <span data-ttu-id="141df-347">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-347">Entry</span></span> | <span data-ttu-id="141df-348">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-349">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-349">Description</span></span>    | <span data-ttu-id="141df-350">Define a senha usada pelo processo do servidor para fazer logon na identidade RunAs especificada.</span><span class="sxs-lookup"><span data-stu-id="141df-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="141df-351">A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas.</span><span class="sxs-lookup"><span data-stu-id="141df-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="141df-352">Se a senha e a identidade forem obtidas fora de sincronia, o componente não poderá ser iniciado até que eles sejam redefinidos por um administrador.</span><span class="sxs-lookup"><span data-stu-id="141df-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="141df-353">Access</span><span class="sxs-lookup"><span data-stu-id="141df-353">Access</span></span>         | <span data-ttu-id="141df-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="141df-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="141df-355">Type</span><span class="sxs-lookup"><span data-stu-id="141df-355">Type</span></span>           | <span data-ttu-id="141df-356">String</span><span class="sxs-lookup"><span data-stu-id="141df-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="141df-357">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-357">Default</span></span>        | <span data-ttu-id="141df-358">NULO</span><span class="sxs-lookup"><span data-stu-id="141df-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="141df-359">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-359">Minimum system</span></span> | <span data-ttu-id="141df-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="141df-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="141df-361">ProgID</span></span>



| <span data-ttu-id="141df-362">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-362">Entry</span></span> | <span data-ttu-id="141df-363">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-364">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-364">Description</span></span>    | <span data-ttu-id="141df-365">Um nome que identifica o componente.</span><span class="sxs-lookup"><span data-stu-id="141df-365">A name identifying the component.</span></span> <span data-ttu-id="141df-366">Essa propriedade é retornada quando o método de propriedade Name é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="141df-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="141df-367">Access</span><span class="sxs-lookup"><span data-stu-id="141df-367">Access</span></span>         | <span data-ttu-id="141df-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="141df-369">Type</span><span class="sxs-lookup"><span data-stu-id="141df-369">Type</span></span>           | <span data-ttu-id="141df-370">String</span><span class="sxs-lookup"><span data-stu-id="141df-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="141df-371">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-371">Default</span></span>        | <span data-ttu-id="141df-372">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="141df-373">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-373">Minimum system</span></span> | <span data-ttu-id="141df-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="141df-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="141df-375">RemoteServer</span></span>



| <span data-ttu-id="141df-376">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-376">Entry</span></span> | <span data-ttu-id="141df-377">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="141df-378">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-378">Description</span></span>    | <span data-ttu-id="141df-379">Especifica o computador do servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="141df-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="141df-380">Access</span><span class="sxs-lookup"><span data-stu-id="141df-380">Access</span></span>         | <span data-ttu-id="141df-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-381">ReadWrite</span></span>                             |
| <span data-ttu-id="141df-382">Type</span><span class="sxs-lookup"><span data-stu-id="141df-382">Type</span></span>           | <span data-ttu-id="141df-383">String</span><span class="sxs-lookup"><span data-stu-id="141df-383">String</span></span>                                |
| <span data-ttu-id="141df-384">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-384">Default</span></span>        | <span data-ttu-id="141df-385">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-385">N/A</span></span>                                   |
| <span data-ttu-id="141df-386">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-386">Minimum system</span></span> | <span data-ttu-id="141df-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="141df-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="141df-388">RunAs</span></span>



| <span data-ttu-id="141df-389">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-389">Entry</span></span> | <span data-ttu-id="141df-390">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-391">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-391">Description</span></span>    | <span data-ttu-id="141df-392">Especifica o usuário sob a identidade cujo componente será executado.</span><span class="sxs-lookup"><span data-stu-id="141df-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="141df-393">A senha deve ser definida ao mesmo tempo que a identidade RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque a senha e a identidade são validadas antes de serem salvas.</span><span class="sxs-lookup"><span data-stu-id="141df-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="141df-394">Se a senha e a identidade forem obtidas fora de sincronia, o componente não poderá ser iniciado até que eles sejam redefinidos por um administrador.</span><span class="sxs-lookup"><span data-stu-id="141df-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="141df-395">Access</span><span class="sxs-lookup"><span data-stu-id="141df-395">Access</span></span>         | <span data-ttu-id="141df-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="141df-397">Type</span><span class="sxs-lookup"><span data-stu-id="141df-397">Type</span></span>           | <span data-ttu-id="141df-398">String</span><span class="sxs-lookup"><span data-stu-id="141df-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="141df-399">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-399">Default</span></span>        | <span data-ttu-id="141df-400">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="141df-401">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-401">Minimum system</span></span> | <span data-ttu-id="141df-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="141df-403">Fileparameter</span><span class="sxs-lookup"><span data-stu-id="141df-403">ServiceParameter</span></span>



| <span data-ttu-id="141df-404">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-404">Entry</span></span> | <span data-ttu-id="141df-405">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-406">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-406">Description</span></span>    | <span data-ttu-id="141df-407">Especifica os parâmetros passados para o aplicativo quando chamado como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="141df-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="141df-408">Access</span><span class="sxs-lookup"><span data-stu-id="141df-408">Access</span></span>         | <span data-ttu-id="141df-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="141df-410">Type</span><span class="sxs-lookup"><span data-stu-id="141df-410">Type</span></span>           | <span data-ttu-id="141df-411">String</span><span class="sxs-lookup"><span data-stu-id="141df-411">String</span></span>                                                                                    |
| <span data-ttu-id="141df-412">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-412">Default</span></span>        | <span data-ttu-id="141df-413">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="141df-414">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-414">Minimum system</span></span> | <span data-ttu-id="141df-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="141df-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="141df-416">SRPTrustLevel</span></span>



| <span data-ttu-id="141df-417">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-417">Entry</span></span> | <span data-ttu-id="141df-418">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-419">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-419">Description</span></span>    | <span data-ttu-id="141df-420">Indica o nível de confiança da política de restrição de software (SRP) do componente.</span><span class="sxs-lookup"><span data-stu-id="141df-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="141df-421">O nível de confiança do SRP refere-se ao nível de confiança que você está disposto a dar a um componente.</span><span class="sxs-lookup"><span data-stu-id="141df-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="141df-422">Um nível de confiança de SRP irrestrito corresponde ao valor de \_ enumeração de FULLYTRUSTED de nível mais seguro \_ , enquanto um nível de confiança SRP não permitido corresponde ao valor de enumeração mais seguro de \_ levelid não \_ permitido.</span><span class="sxs-lookup"><span data-stu-id="141df-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="141df-423">A enumeração para os níveis de confiança é definida em Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="141df-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="141df-424">Access</span><span class="sxs-lookup"><span data-stu-id="141df-424">Access</span></span>         | <span data-ttu-id="141df-425">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="141df-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="141df-426">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-426">Type</span></span>           | <span data-ttu-id="141df-427">Valores longos possíveis: nível mais seguro \_ de redistribuirid não \_ permitido (0x0) \_ FULLYTRUSTED de nível mais seguro \_ (0x40000)</span><span class="sxs-lookup"><span data-stu-id="141df-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="141df-428">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-428">Default</span></span>        | <span data-ttu-id="141df-429">nível mais seguro de \_ \_ FULLYTRUSTED</span><span class="sxs-lookup"><span data-stu-id="141df-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="141df-430">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-430">Minimum system</span></span> | <span data-ttu-id="141df-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="141df-432">Um componente ao qual você está disposto a confiar com acesso irrestrito deve ter a segurança mais rigorosa anexada a ele.</span><span class="sxs-lookup"><span data-stu-id="141df-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="141df-433">Os aplicativos que são irrestritos podem carregar apenas componentes irrestritos, enquanto os aplicativos não permitidos não poderão ser executados e, portanto, não poderão carregar nenhum componente.</span><span class="sxs-lookup"><span data-stu-id="141df-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="141df-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="141df-434">ThreadingModel</span></span>



| <span data-ttu-id="141df-435">Entrada</span><span class="sxs-lookup"><span data-stu-id="141df-435">Entry</span></span> | <span data-ttu-id="141df-436">Valor</span><span class="sxs-lookup"><span data-stu-id="141df-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141df-437">Descrição</span><span class="sxs-lookup"><span data-stu-id="141df-437">Description</span></span>    | <span data-ttu-id="141df-438">Determina como as instâncias do componente são atribuídas a threads para execução do método.</span><span class="sxs-lookup"><span data-stu-id="141df-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="141df-439">Os valores correspondem aos modelos de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="141df-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="141df-440">Access</span><span class="sxs-lookup"><span data-stu-id="141df-440">Access</span></span>         | <span data-ttu-id="141df-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="141df-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="141df-442">Tipo</span><span class="sxs-lookup"><span data-stu-id="141df-442">Type</span></span>           | <span data-ttu-id="141df-443">Valores longos possíveis: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)</span><span class="sxs-lookup"><span data-stu-id="141df-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="141df-444">Padrão</span><span class="sxs-lookup"><span data-stu-id="141df-444">Default</span></span>        | <span data-ttu-id="141df-445">N/D</span><span class="sxs-lookup"><span data-stu-id="141df-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="141df-446">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="141df-446">Minimum system</span></span> | <span data-ttu-id="141df-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="141df-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="141df-448">Confira também</span><span class="sxs-lookup"><span data-stu-id="141df-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141df-449">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="141df-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
