---
title: Classe ReplicationProvider1
description: A classe base para a instância do provedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory classe ReplicationProvider1
- Active Directory classe ReplicationProvider1, descrita
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009274"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="94faa-105">Classe ReplicationProvider1</span><span class="sxs-lookup"><span data-stu-id="94faa-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="94faa-106">A classe base para a instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-106">The base class for the provider instance.</span></span>

<span data-ttu-id="94faa-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="94faa-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94faa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94faa-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="94faa-109">Membros</span><span class="sxs-lookup"><span data-stu-id="94faa-109">Members</span></span>

<span data-ttu-id="94faa-110">A classe **ReplicationProvider1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94faa-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="94faa-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94faa-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94faa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94faa-112">Properties</span></span>

<span data-ttu-id="94faa-113">A classe **ReplicationProvider1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94faa-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94faa-114">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="94faa-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-117">Identificador de classe que o WMI usa para determinar se um provedor de alto desempenho deve ou não ser carregado no processo do cliente ou no processo WMI.</span><span class="sxs-lookup"><span data-stu-id="94faa-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="94faa-118">Se o provedor e o cliente estiverem localizados no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="94faa-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="94faa-119">Quando o provedor e o cliente estão localizados em computadores diferentes, o WMI carrega o provedor em processo para o WMI.</span><span class="sxs-lookup"><span data-stu-id="94faa-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="94faa-120">O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.</span><span class="sxs-lookup"><span data-stu-id="94faa-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="94faa-121">Para obter mais informações, consulte [registrando um provedor de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="94faa-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="94faa-122">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="94faa-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-126">O **GUID** que representa o identificador de classe (**CLSID**) do objeto com do provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="94faa-127">Esse objeto COM deve conter uma implementação da interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="94faa-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="94faa-128">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-129">**Simultaneidade**</span><span class="sxs-lookup"><span data-stu-id="94faa-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94faa-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-132">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-132">Not used.</span></span>

<span data-ttu-id="94faa-133">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-134">**Defaultmachinename**</span><span class="sxs-lookup"><span data-stu-id="94faa-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-137">Identifica o computador no qual o provedor deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="94faa-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="94faa-138">Se o provedor for executado no computador local, ele será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="94faa-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="94faa-139">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="94faa-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-141">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-143">Se for **true**, essa instância será habilitada e poderá ser usada para concluir as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="94faa-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="94faa-144">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-145">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="94faa-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94faa-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94faa-148">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span><span class="sxs-lookup"><span data-stu-id="94faa-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="94faa-149">Contém o modelo de hospedagem do provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="94faa-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="94faa-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-151">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94faa-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-153">Reservado.</span><span class="sxs-lookup"><span data-stu-id="94faa-153">Reserved.</span></span> <span data-ttu-id="94faa-154">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="94faa-154">The default value is zero (0).</span></span>

<span data-ttu-id="94faa-155">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-156">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="94faa-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94faa-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-159">Conjunto de sinalizadores que fornecem informações sobre a serialização.</span><span class="sxs-lookup"><span data-stu-id="94faa-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="94faa-160">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="94faa-160">The default value is zero (0).</span></span>

<span data-ttu-id="94faa-161">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="94faa-162"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="94faa-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="94faa-163">Todas as inicializações desse provedor devem ser serializadas.</span><span class="sxs-lookup"><span data-stu-id="94faa-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="94faa-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="94faa-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="94faa-165">Todas as inicializações deste provedor no mesmo namespace devem ser serializadas.</span><span class="sxs-lookup"><span data-stu-id="94faa-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="94faa-166"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="94faa-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="94faa-167">Nenhuma serialização de inicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="94faa-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="94faa-168">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="94faa-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-169">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94faa-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-171">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-171">Not used.</span></span>

<span data-ttu-id="94faa-172">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-173">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="94faa-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-176">**Windows Server 2003:** Esta propriedade está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="94faa-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="94faa-177">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="94faa-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94faa-181">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="94faa-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="94faa-182">O nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-182">The provider name.</span></span>

<span data-ttu-id="94faa-183">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-184">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="94faa-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-185">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94faa-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-186">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-187">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-187">Not used.</span></span>

<span data-ttu-id="94faa-188">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-189">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="94faa-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-190">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-192">Se for **true**, o provedor será inicializado para cada localidade quando um usuário se conectar ao mesmo namespace mais de uma vez usando localidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="94faa-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="94faa-193">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="94faa-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="94faa-194">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-195">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="94faa-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-198">Se for **true**, o provedor será inicializado uma vez para cada usuário do NT LAN Manager (NTLM) que faz solicitações ao provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="94faa-199">Se **for false** (padrão), o provedor será inicializado uma vez para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="94faa-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="94faa-200">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-201">**Mero**</span><span class="sxs-lookup"><span data-stu-id="94faa-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-202">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-203">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-204">Se **for true**, o provedor concorda em se preparar para descarregar chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método **Release** de sua interface primária.</span><span class="sxs-lookup"><span data-stu-id="94faa-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="94faa-205">Provedores que devem permanecer clientes do WMI depois que não funcionam como provedores devem definir **Pure** como **false**.</span><span class="sxs-lookup"><span data-stu-id="94faa-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="94faa-206">A configuração padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="94faa-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="94faa-207">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="94faa-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="94faa-208">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="94faa-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94faa-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-212">Descritor de segurança (SD) na linguagem de definição do descritor de segurança (SDDL) que determina o conjunto de usuários que podem chamar [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para o provedor dissociado com êxito.</span><span class="sxs-lookup"><span data-stu-id="94faa-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="94faa-213">Para obter mais informações, consulte o tópico [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) na seção security da SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="94faa-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="94faa-214">Esse descritor de segurança é usado apenas para provedores dissociados e não afeta outros provedores.</span><span class="sxs-lookup"><span data-stu-id="94faa-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="94faa-215">Para obter mais informações, consulte [incorporando um provedor em um aplicativo](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="94faa-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="94faa-216">O WMI executa verificações de acesso para provedores dissociados que usam as interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="94faa-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="94faa-217">Se o descritor de segurança for **nulo**, somente aplicativos ou serviços executados nas contas LocalSystem, NetworkService e LocalService poderão executar um provedor dissociado.</span><span class="sxs-lookup"><span data-stu-id="94faa-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="94faa-218">A cadeia de caracteres a seguir mostra um provedor dissociado a ser executado somente por administradores internos. " O:BAG: INADEQUADO: (A;; 0 X1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="94faa-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="94faa-219">Para obter mais informações sobre como definir a propriedade **SecurityDescriptor** , consulte [mantendo a segurança do WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="94faa-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="94faa-220">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-221">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="94faa-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-222">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-224">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-224">Not used.</span></span>

<span data-ttu-id="94faa-225">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-226">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="94faa-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-228">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-229">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-229">Not used.</span></span>

<span data-ttu-id="94faa-230">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-231">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="94faa-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-232">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-233">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-234">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-234">Not used.</span></span>

<span data-ttu-id="94faa-235">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-236">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="94faa-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-237">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-239">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-239">Not used.</span></span>

<span data-ttu-id="94faa-240">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-241">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="94faa-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-242">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-243">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-244">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-244">Not used.</span></span>

<span data-ttu-id="94faa-245">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-246">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="94faa-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-247">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94faa-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-248">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-249">Não usado.</span><span class="sxs-lookup"><span data-stu-id="94faa-249">Not used.</span></span>

<span data-ttu-id="94faa-250">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-251">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="94faa-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-252">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94faa-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-254">[Formato de data e hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica por quanto tempo o WMI permite que o provedor permaneça ocioso antes de ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="94faa-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="94faa-255">Normalmente, os provedores solicitam que o WMI não aguarde mais do que cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="94faa-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="94faa-256">Para a versão atual do WMI, o valor dessa propriedade é ignorado.</span><span class="sxs-lookup"><span data-stu-id="94faa-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="94faa-257">O WMI descarrega o provedor com base no valor de tempo limite em uma classe interna no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="94faa-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="94faa-258">É recomendável que os provedores definam **UnloadTimeout**.</span><span class="sxs-lookup"><span data-stu-id="94faa-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="94faa-259">Para obter mais informações, consulte [descarregando um provedor](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="94faa-260">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="94faa-261">**Versão**</span><span class="sxs-lookup"><span data-stu-id="94faa-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94faa-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94faa-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94faa-263">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94faa-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94faa-264">Versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="94faa-264">Version of the provider.</span></span> <span data-ttu-id="94faa-265">As versões com suporte são 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="94faa-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="94faa-266">A versão 2 reforça as verificações de validade para todos os registros de propriedade associados, especificamente a propriedade [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .</span><span class="sxs-lookup"><span data-stu-id="94faa-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="94faa-267">Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="94faa-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94faa-268">Comentários</span><span class="sxs-lookup"><span data-stu-id="94faa-268">Remarks</span></span>

<span data-ttu-id="94faa-269">Uma instância dessa classe representa o provedor WMI para serviços de Domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94faa-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="94faa-270">Os padrões são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="94faa-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="94faa-271">Nome = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="94faa-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="94faa-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="94faa-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="94faa-273">HostingModel = "NetworkServiceHost"</span><span class="sxs-lookup"><span data-stu-id="94faa-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="94faa-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94faa-274">Requirements</span></span>



| <span data-ttu-id="94faa-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="94faa-275">Requirement</span></span> | <span data-ttu-id="94faa-276">Valor</span><span class="sxs-lookup"><span data-stu-id="94faa-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94faa-277">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94faa-277">Minimum supported client</span></span><br/> | <span data-ttu-id="94faa-278">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="94faa-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="94faa-279">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94faa-279">Minimum supported server</span></span><br/> | <span data-ttu-id="94faa-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94faa-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94faa-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="94faa-281">Namespace</span></span><br/>                | <span data-ttu-id="94faa-282">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="94faa-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="94faa-283">MOF</span><span class="sxs-lookup"><span data-stu-id="94faa-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94faa-284"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94faa-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="94faa-285">DLL</span><span class="sxs-lookup"><span data-stu-id="94faa-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94faa-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94faa-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94faa-287">Confira também</span><span class="sxs-lookup"><span data-stu-id="94faa-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94faa-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="94faa-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

