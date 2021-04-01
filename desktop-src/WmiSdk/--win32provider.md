---
description: Registra informações sobre a implementação física de um provedor no WMI. Provedores que não definem a Propriedade HostingModel são carregados, por padrão, para serem executados em um processo de Wmiprvse.exe como NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922603"
---
# <a name="__win32provider-class"></a><span data-ttu-id="908ce-104">\_\_Classe Win32Provider</span><span class="sxs-lookup"><span data-stu-id="908ce-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="908ce-105">A classe de sistema **\_ \_ Win32Provider** registra informações sobre a implementação física de um provedor no WMI.</span><span class="sxs-lookup"><span data-stu-id="908ce-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="908ce-106">Provedores que não definem a propriedade **HostingModel** são carregados, por padrão, para serem executados em um processo de Wmiprvse.exe como **NetworkServiceHostOrSelfHost**.</span><span class="sxs-lookup"><span data-stu-id="908ce-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="908ce-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="908ce-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="908ce-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="908ce-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="908ce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="908ce-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="908ce-110">Membros</span><span class="sxs-lookup"><span data-stu-id="908ce-110">Members</span></span>

<span data-ttu-id="908ce-111">A classe **\_ \_ Win32Provider** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="908ce-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="908ce-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="908ce-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="908ce-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="908ce-113">Properties</span></span>

<span data-ttu-id="908ce-114">A classe **\_ \_ Win32Provider** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="908ce-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="908ce-115">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="908ce-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-118">Identificador de classe que o WMI usa para determinar se um provedor de alto desempenho deve ou não ser carregado no processo do cliente ou no processo WMI.</span><span class="sxs-lookup"><span data-stu-id="908ce-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="908ce-119">Se o provedor e o cliente estiverem localizados no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="908ce-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="908ce-120">Quando o provedor e o cliente estão localizados em computadores diferentes, o WMI carrega o provedor em processo para o WMI.</span><span class="sxs-lookup"><span data-stu-id="908ce-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="908ce-121">O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.</span><span class="sxs-lookup"><span data-stu-id="908ce-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="908ce-122">Para obter mais informações, consulte [registrando um provedor de High-Performance.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="908ce-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="908ce-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="908ce-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-126">O **GUID** que representa o identificador de classe (**CLSID**) do objeto com do provedor.</span><span class="sxs-lookup"><span data-stu-id="908ce-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="908ce-127">Esse objeto COM deve conter uma implementação da interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="908ce-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-128">**Simultaneidade**</span><span class="sxs-lookup"><span data-stu-id="908ce-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="908ce-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-131">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-132">**Defaultmachinename**</span><span class="sxs-lookup"><span data-stu-id="908ce-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-135">Identifica o computador no qual o provedor deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="908ce-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="908ce-136">Se o provedor for executado no computador local, ele será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="908ce-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="908ce-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-140">Se for **true**, essa instância será habilitada e poderá ser usada para concluir as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="908ce-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-141">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="908ce-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-144">Essa propriedade é composta de valores das propriedades de **hospedagem** e **HostingSpecification** de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="908ce-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="908ce-145">O valor dessa propriedade especifica como o WMI carrega o provedor e a conta de segurança na qual ele é executado.</span><span class="sxs-lookup"><span data-stu-id="908ce-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="908ce-146">Para obter mais informações sobre como definir a propriedade **HostingModel** , consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md) e [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="908ce-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="908ce-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="908ce-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-148">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="908ce-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-150">Reservado.</span><span class="sxs-lookup"><span data-stu-id="908ce-150">Reserved.</span></span> <span data-ttu-id="908ce-151">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="908ce-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="908ce-152">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="908ce-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="908ce-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-155">Conjunto de sinalizadores que fornecem informações sobre a serialização.</span><span class="sxs-lookup"><span data-stu-id="908ce-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="908ce-156">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="908ce-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="908ce-157">0</span><span class="sxs-lookup"><span data-stu-id="908ce-157">0</span></span>
</dt> <dd>

<span data-ttu-id="908ce-158">Todas as inicializações desse provedor devem ser serializadas.</span><span class="sxs-lookup"><span data-stu-id="908ce-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-159">1</span><span class="sxs-lookup"><span data-stu-id="908ce-159">1</span></span>
</dt> <dd>

<span data-ttu-id="908ce-160">Todas as inicializações deste provedor no mesmo namespace devem ser serializadas.</span><span class="sxs-lookup"><span data-stu-id="908ce-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-161">2</span><span class="sxs-lookup"><span data-stu-id="908ce-161">2</span></span>
</dt> <dd>

<span data-ttu-id="908ce-162">Nenhuma serialização de inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="908ce-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="908ce-163">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="908ce-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-164">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="908ce-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-166">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-167">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="908ce-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-170">TBD</span><span class="sxs-lookup"><span data-stu-id="908ce-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="908ce-171">**Nome**</span><span class="sxs-lookup"><span data-stu-id="908ce-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="908ce-174">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="908ce-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="908ce-175">O nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="908ce-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-176">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="908ce-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-177">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="908ce-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-179">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-180">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="908ce-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-181">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-183">Se for **true**, o provedor será inicializado para cada localidade quando um usuário se conectar ao mesmo namespace mais de uma vez usando localidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="908ce-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="908ce-184">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="908ce-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-185">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="908ce-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-186">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-188">Se for **true**, o provedor será inicializado uma vez para cada usuário do NT LAN Manager (NTLM) que faz solicitações ao provedor.</span><span class="sxs-lookup"><span data-stu-id="908ce-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="908ce-189">Se **for false** (padrão), o provedor será inicializado uma vez para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="908ce-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-190">**Mero**</span><span class="sxs-lookup"><span data-stu-id="908ce-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-191">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-193">Se **for true**, o provedor concorda em se preparar para descarregar chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método **Release** de sua interface primária.</span><span class="sxs-lookup"><span data-stu-id="908ce-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="908ce-194">Provedores que devem permanecer clientes do WMI depois que não funcionam como provedores devem definir **Pure** como **false**.</span><span class="sxs-lookup"><span data-stu-id="908ce-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="908ce-195">A configuração padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="908ce-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="908ce-196">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="908ce-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="908ce-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="908ce-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-200">Descritor de segurança (SD) na linguagem de definição do descritor de segurança (SDDL) que determina o conjunto de usuários que podem chamar [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para o provedor dissociado com êxito.</span><span class="sxs-lookup"><span data-stu-id="908ce-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="908ce-201">Para obter mais informações, consulte o tópico [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) na seção security da SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="908ce-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="908ce-202">Esse descritor de segurança é usado apenas para provedores dissociados e não afeta outros provedores.</span><span class="sxs-lookup"><span data-stu-id="908ce-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="908ce-203">Para obter mais informações, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="908ce-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="908ce-204">O WMI executa verificações de acesso para provedores dissociados que usam as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="908ce-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="908ce-205">Se o descritor de segurança for **nulo**, somente aplicativos ou serviços executados nas contas LocalSystem, NetworkService e LocalService poderão executar um provedor dissociado.</span><span class="sxs-lookup"><span data-stu-id="908ce-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="908ce-206">A cadeia de caracteres a seguir mostra um provedor dissociado a ser executado somente por administradores internos. " O:BAG: INADEQUADO: (A;; 0 X1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="908ce-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="908ce-207">Para obter mais informações sobre como definir a propriedade **SecurityDescriptor** , consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="908ce-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="908ce-208">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="908ce-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-209">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-211">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-212">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="908ce-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-213">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-215">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-216">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="908ce-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-217">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-218">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-219">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-220">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="908ce-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-221">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-222">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-223">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-224">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="908ce-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-225">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-227">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-228">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="908ce-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-229">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="908ce-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-230">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-231">Não usado.</span><span class="sxs-lookup"><span data-stu-id="908ce-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-232">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="908ce-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-233">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="908ce-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-234">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-235">[Formato de data e hora](date-and-time-format.md) que especifica por quanto tempo o WMI permite que o provedor permaneça ocioso antes de ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="908ce-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="908ce-236">Normalmente, os provedores solicitam que o WMI não aguarde mais do que cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="908ce-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="908ce-237">Para a versão atual do WMI, o valor dessa propriedade é ignorado.</span><span class="sxs-lookup"><span data-stu-id="908ce-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="908ce-238">O WMI descarrega o provedor com base no valor de tempo limite em uma classe interna no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="908ce-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="908ce-239">É recomendável que os provedores definam **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="908ce-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="908ce-240">Para obter mais informações, consulte [descarregando um provedor](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="908ce-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="908ce-241">**Versão**</span><span class="sxs-lookup"><span data-stu-id="908ce-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908ce-242">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="908ce-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="908ce-243">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="908ce-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="908ce-244">Versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="908ce-244">Version of the provider.</span></span> <span data-ttu-id="908ce-245">As versões com suporte são 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="908ce-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="908ce-246">A versão 2 reforça as verificações de validade para todos os registros de propriedade associados, especificamente a propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="908ce-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="908ce-247">Comentários</span><span class="sxs-lookup"><span data-stu-id="908ce-247">Remarks</span></span>

<span data-ttu-id="908ce-248">A classe **\_ \_ Win32Provider** é derivada do [**\_ \_ provedor**](--provider.md).</span><span class="sxs-lookup"><span data-stu-id="908ce-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="908ce-249">A maioria dos provedores pode aceitar os valores padrão para a propriedade **InitializationReentrancy** .</span><span class="sxs-lookup"><span data-stu-id="908ce-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="908ce-250">No entanto, se um provedor puder oferecer suporte à inicialização simultânea para usuários separados, essa propriedade poderá ser definida como 1 (um).</span><span class="sxs-lookup"><span data-stu-id="908ce-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="908ce-251">Se a inicialização serializada for necessária, **InitializationReentrancy** permanecerá 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="908ce-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="908ce-252">Em ambas as instâncias, **PerUserInitialization** é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="908ce-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="908ce-253">Um provedor puro ou um provedor que define a propriedade **pura** como **true**, existe apenas para atender a solicitações de aplicativos e WMI.</span><span class="sxs-lookup"><span data-stu-id="908ce-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="908ce-254">A maioria dos provedores são provedores puros.</span><span class="sxs-lookup"><span data-stu-id="908ce-254">Most providers are pure providers.</span></span> <span data-ttu-id="908ce-255">Um provedor não puro é a exceção.</span><span class="sxs-lookup"><span data-stu-id="908ce-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="908ce-256">Os provedores não puros fazem a transição para a função do cliente depois de concluírem as solicitações de manutenção.</span><span class="sxs-lookup"><span data-stu-id="908ce-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="908ce-257">Um exemplo de um provedor não puro é um provedor de envio por push que começa a emitir consultas e faz solicitações do WMI após a conclusão da inicialização.</span><span class="sxs-lookup"><span data-stu-id="908ce-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="908ce-258">Um provedor de push não tem responsabilidades, exceto atualizar o repositório CIM com dados no momento da inicialização.</span><span class="sxs-lookup"><span data-stu-id="908ce-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="908ce-259">Depois de atualizar o repositório, um provedor de push pode aguardar para ser descarregado ou fazer a transição para a função do cliente.</span><span class="sxs-lookup"><span data-stu-id="908ce-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="908ce-260">O provedor de envio por push que espera para ser descarregado é um provedor puro.</span><span class="sxs-lookup"><span data-stu-id="908ce-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="908ce-261">O provedor de envio por push que participa de atividades do cliente é não puro.</span><span class="sxs-lookup"><span data-stu-id="908ce-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="908ce-262">O WMI deve ser capaz de distinguir provedores puros de provedores não puros para que ele possa determinar quando é seguro desligá-lo.</span><span class="sxs-lookup"><span data-stu-id="908ce-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="908ce-263">O WMI deve esperar que todas as operações que envolvem provedores não puros sejam concluídas antes de serem desligadas com segurança.</span><span class="sxs-lookup"><span data-stu-id="908ce-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="908ce-264">Requisitos</span><span class="sxs-lookup"><span data-stu-id="908ce-264">Requirements</span></span>



| <span data-ttu-id="908ce-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="908ce-265">Requirement</span></span> | <span data-ttu-id="908ce-266">Valor</span><span class="sxs-lookup"><span data-stu-id="908ce-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="908ce-267">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="908ce-267">Minimum supported client</span></span><br/> | <span data-ttu-id="908ce-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="908ce-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="908ce-269">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="908ce-269">Minimum supported server</span></span><br/> | <span data-ttu-id="908ce-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="908ce-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="908ce-271">Namespace</span><span class="sxs-lookup"><span data-stu-id="908ce-271">Namespace</span></span><br/>                | <span data-ttu-id="908ce-272">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="908ce-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="908ce-273">Confira também</span><span class="sxs-lookup"><span data-stu-id="908ce-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908ce-274">**\_\_Provedor**</span><span class="sxs-lookup"><span data-stu-id="908ce-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="908ce-275">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="908ce-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="908ce-276">Registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="908ce-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

