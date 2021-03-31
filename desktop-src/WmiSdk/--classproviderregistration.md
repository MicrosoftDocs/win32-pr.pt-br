---
description: Registra provedores de classe no WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Classe __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663475"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="29db0-103">\_\_Classe ClassProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="29db0-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="29db0-104">A classe de sistema **\_ \_ ClassProviderRegistration** registra provedores de classe no WMI.</span><span class="sxs-lookup"><span data-stu-id="29db0-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="29db0-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="29db0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29db0-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="29db0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29db0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29db0-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="29db0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="29db0-108">Members</span></span>

<span data-ttu-id="29db0-109">A classe **\_ \_ ClassProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="29db0-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="29db0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29db0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29db0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29db0-111">Properties</span></span>

<span data-ttu-id="29db0-112">A classe **\_ \_ ClassProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29db0-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29db0-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="29db0-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-114">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="29db0-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-117">**Entre ações**</span><span class="sxs-lookup"><span data-stu-id="29db0-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="29db0-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-120">Indica se o provedor de classe ou instância fornece dados ou se baseia no WMI e no repositório de modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="29db0-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="29db0-121">Os provedores de pull dão suporte ao acesso dinâmico aos dados, e os provedores de envio por push armazenam dados no repositório CIM e contam com o WMI para fornecer acesso a ele.</span><span class="sxs-lookup"><span data-stu-id="29db0-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="29db0-122">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="29db0-122">The default value is 0 (zero).</span></span> <span data-ttu-id="29db0-123">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="29db0-124">Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="29db0-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="29db0-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-126">O provedor é um provedor de pull.</span><span class="sxs-lookup"><span data-stu-id="29db0-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="29db0-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="29db0-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-128">O provedor é um provedor de push.</span><span class="sxs-lookup"><span data-stu-id="29db0-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="29db0-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="29db0-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-130">O provedor é um provedor de verificação por push.</span><span class="sxs-lookup"><span data-stu-id="29db0-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="29db0-131">Observe que os provedores de **PushVerify** não têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="29db0-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-132">**PerUserSchema**</span><span class="sxs-lookup"><span data-stu-id="29db0-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-135">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-136">**operador**</span><span class="sxs-lookup"><span data-stu-id="29db0-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-137">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="29db0-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29db0-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29db0-139">Caminho do objeto para um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="29db0-139">Object path to a class provider.</span></span> <span data-ttu-id="29db0-140">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="29db0-141">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="29db0-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-142">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29db0-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29db0-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-144">Matriz dos tipos de suporte incluído no provedor para processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="29db0-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="29db0-145">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="29db0-146">Provedores de classe são necessários para dar suporte a pelo menos um tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="29db0-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="29db0-147">Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="29db0-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="29db0-148">Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="29db0-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="29db0-149">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="29db0-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="29db0-150">("WQL: referências")</span><span class="sxs-lookup"><span data-stu-id="29db0-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="29db0-151">("WQL: ASSOCIATORS")</span><span class="sxs-lookup"><span data-stu-id="29db0-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="29db0-152">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="29db0-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-153">**ReferencedSetQueries**</span><span class="sxs-lookup"><span data-stu-id="29db0-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-154">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29db0-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29db0-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-156">Uma ou mais consultas que descrevem o conjunto de classes referenciadas com suporte de um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="29db0-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="29db0-157">Provedores que podem fornecer classes de associação devem incluir pelo menos uma consulta nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="29db0-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-158">**ResultSetQueries**</span><span class="sxs-lookup"><span data-stu-id="29db0-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-159">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29db0-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29db0-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-161">Uma ou mais consultas que descrevem o conjunto de todas as classes que podem ser fornecidas pelo provedor de classe ou um superconjunto dessas classes.</span><span class="sxs-lookup"><span data-stu-id="29db0-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="29db0-162">Essa propriedade nunca especifica um subconjunto de classes com suporte.</span><span class="sxs-lookup"><span data-stu-id="29db0-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-163">**ReSynchroniseOnNamespaceOpen**</span><span class="sxs-lookup"><span data-stu-id="29db0-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-164">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-166">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-167">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="29db0-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-170">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-170">Not used.</span></span>

<span data-ttu-id="29db0-171">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="29db0-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="29db0-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-173">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-175">Se **for true**, o provedor dará suporte à exclusão de dados.</span><span class="sxs-lookup"><span data-stu-id="29db0-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="29db0-176">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="29db0-177">True</span><span class="sxs-lookup"><span data-stu-id="29db0-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-178">O provedor dá suporte à exclusão de classe ou instância implementando um dos [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="29db0-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="29db0-179">For</span><span class="sxs-lookup"><span data-stu-id="29db0-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-180">O provedor não dá suporte à exclusão de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="29db0-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-181">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="29db0-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-182">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-184">Se **for true**, o provedor dará suporte à enumeração de dados.</span><span class="sxs-lookup"><span data-stu-id="29db0-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="29db0-185">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="29db0-186">True</span><span class="sxs-lookup"><span data-stu-id="29db0-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-187">O provedor dá suporte à enumeração de dados implementando um dos [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provedores de classe) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="29db0-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="29db0-188">For</span><span class="sxs-lookup"><span data-stu-id="29db0-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-189">O provedor não oferece suporte à enumeração de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="29db0-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-190">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="29db0-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-191">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-193">Se **for true**, o provedor de classe ou instância dará suporte à recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="29db0-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="29db0-194">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="29db0-195">True</span><span class="sxs-lookup"><span data-stu-id="29db0-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-196">O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="29db0-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="29db0-197">For</span><span class="sxs-lookup"><span data-stu-id="29db0-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-198">O provedor não dá suporte à recuperação de dados e retorna **o \_ provedor WBEM e \_ não é \_ \_ capaz** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="29db0-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-199">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="29db0-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-200">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-202">Se **for true**, o provedor de classe ou instância dará suporte à modificação de dados.</span><span class="sxs-lookup"><span data-stu-id="29db0-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="29db0-203">Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="29db0-204">True</span><span class="sxs-lookup"><span data-stu-id="29db0-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-205">O provedor dá suporte à modificação de classe ou instância implementando um dos [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).</span><span class="sxs-lookup"><span data-stu-id="29db0-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="29db0-206">For</span><span class="sxs-lookup"><span data-stu-id="29db0-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="29db0-207">O provedor não dá suporte à modificação de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ compatível** com [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="29db0-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="29db0-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="29db0-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-209">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-211">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-212">**SuppportsBatching**</span><span class="sxs-lookup"><span data-stu-id="29db0-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-213">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29db0-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-215">Não usado.</span><span class="sxs-lookup"><span data-stu-id="29db0-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-216">**UnsupportedQueries**</span><span class="sxs-lookup"><span data-stu-id="29db0-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-217">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29db0-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29db0-218">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-219">Uma ou mais consultas que descrevem o conjunto de classes para as quais o provedor de classes não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="29db0-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="29db0-220">Use essa propriedade para subtrair do conjunto de classes implícitas por **ResultSetQueries**.</span><span class="sxs-lookup"><span data-stu-id="29db0-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="29db0-221">**Versão**</span><span class="sxs-lookup"><span data-stu-id="29db0-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29db0-222">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29db0-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29db0-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="29db0-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29db0-224">Versão deste provedor de classes.</span><span class="sxs-lookup"><span data-stu-id="29db0-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29db0-225">Comentários</span><span class="sxs-lookup"><span data-stu-id="29db0-225">Remarks</span></span>

<span data-ttu-id="29db0-226">A classe **\_ \_ ClassProviderRegistration** é derivada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="29db0-227">As propriedades herdadas de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indicam se o provedor de classe dá suporte à recuperação de dados, modificação, exclusão, enumeração e processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="29db0-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="29db0-228">A propriedade **interactiontype** especifica se o provedor de classe foi projetado ou não como um provedor de pull ou push.</span><span class="sxs-lookup"><span data-stu-id="29db0-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="29db0-229">Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="29db0-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="29db0-230">A classe [**\_ \_ ProviderRegistration**](--providerregistration.md) define a propriedade do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="29db0-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="29db0-231">Somente os administradores podem registrar um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ ClassProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="29db0-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="29db0-232">Somente os administradores podem excluir um provedor.</span><span class="sxs-lookup"><span data-stu-id="29db0-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="29db0-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29db0-233">Requirements</span></span>



| <span data-ttu-id="29db0-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="29db0-234">Requirement</span></span> | <span data-ttu-id="29db0-235">Valor</span><span class="sxs-lookup"><span data-stu-id="29db0-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="29db0-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29db0-236">Minimum supported client</span></span><br/> | <span data-ttu-id="29db0-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29db0-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="29db0-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29db0-238">Minimum supported server</span></span><br/> | <span data-ttu-id="29db0-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29db0-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="29db0-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="29db0-240">Namespace</span></span><br/>                | <span data-ttu-id="29db0-241">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="29db0-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="29db0-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="29db0-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29db0-243">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="29db0-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="29db0-244">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="29db0-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="29db0-245">Registrando um provedor de classe</span><span class="sxs-lookup"><span data-stu-id="29db0-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="29db0-246">Registrando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="29db0-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="29db0-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="29db0-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

