---
description: Registra provedores de instância no WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Classe __InstanceProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798384"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="95d64-103">\_\_Classe InstanceProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="95d64-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="95d64-104">A classe de sistema **\_ \_ InstanceProviderRegistration** registra provedores de instância no WMI.</span><span class="sxs-lookup"><span data-stu-id="95d64-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="95d64-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="95d64-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="95d64-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="95d64-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d64-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95d64-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="95d64-108">Membros</span><span class="sxs-lookup"><span data-stu-id="95d64-108">Members</span></span>

<span data-ttu-id="95d64-109">A classe **\_ \_ InstanceProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95d64-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="95d64-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95d64-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95d64-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95d64-111">Properties</span></span>

<span data-ttu-id="95d64-112">A classe **\_ \_ InstanceProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="95d64-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95d64-113">**Entre ações**</span><span class="sxs-lookup"><span data-stu-id="95d64-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-114">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95d64-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-116">Indica que um provedor de classe ou instância fornece dados ou recupera dados do WMI e do repositório de modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="95d64-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="95d64-117">Os provedores de pull dão suporte ao acesso dinâmico aos seus dados; e os provedores de push armazenam seus dados no repositório CIM e usam o WMI para fornecer acesso a ele.</span><span class="sxs-lookup"><span data-stu-id="95d64-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="95d64-118">Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="95d64-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="95d64-119">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="95d64-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="95d64-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="95d64-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-121">O provedor é um provedor de pull.</span><span class="sxs-lookup"><span data-stu-id="95d64-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="95d64-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="95d64-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-123">O provedor é um provedor de push.</span><span class="sxs-lookup"><span data-stu-id="95d64-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="95d64-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="95d64-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-125">O provedor é um provedor de verificação por push.</span><span class="sxs-lookup"><span data-stu-id="95d64-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="95d64-126">Observe que os provedores de verificação por push não têm suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="95d64-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-127">**operador**</span><span class="sxs-lookup"><span data-stu-id="95d64-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-128">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="95d64-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95d64-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95d64-130">Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa o caminho do objeto para o provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="95d64-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="95d64-131">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="95d64-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d64-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="95d64-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95d64-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95d64-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-135">Matriz dos tipos de suporte incluído no provedor para processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="95d64-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="95d64-136">Os provedores de classe não dão suporte a todos os tipos de consultas.</span><span class="sxs-lookup"><span data-stu-id="95d64-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="95d64-137">Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="95d64-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="95d64-138">Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="95d64-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="95d64-139">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="95d64-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95d64-140">("WQL: referências")</span><span class="sxs-lookup"><span data-stu-id="95d64-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95d64-141">("WQL: ASSOCIATORS")</span><span class="sxs-lookup"><span data-stu-id="95d64-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95d64-142">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="95d64-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="95d64-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-146">Não usado.</span><span class="sxs-lookup"><span data-stu-id="95d64-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="95d64-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="95d64-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-150">Se **for true**, o provedor dará suporte à exclusão de dados.</span><span class="sxs-lookup"><span data-stu-id="95d64-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="95d64-151">True</span><span class="sxs-lookup"><span data-stu-id="95d64-151">True</span></span>
</dt> <dd>

<span data-ttu-id="95d64-152">O provedor dá suporte à exclusão de classe ou instância implementando o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="95d64-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="95d64-153">Falso</span><span class="sxs-lookup"><span data-stu-id="95d64-153">False</span></span>
</dt> <dd>

<span data-ttu-id="95d64-154">O provedor não dá suporte à exclusão de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="95d64-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="95d64-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-156">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-158">Se **for true**, o provedor dará suporte à enumeração de dados.</span><span class="sxs-lookup"><span data-stu-id="95d64-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="95d64-159">True</span><span class="sxs-lookup"><span data-stu-id="95d64-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-160">O provedor dá suporte à enumeração de dados implementando um dos [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provedores de classe) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="95d64-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="95d64-161">For</span><span class="sxs-lookup"><span data-stu-id="95d64-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-162">O provedor não oferece suporte à enumeração de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="95d64-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="95d64-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-164">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-166">Se **for true**, o provedor de classe ou instância dará suporte à recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="95d64-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="95d64-167">True</span><span class="sxs-lookup"><span data-stu-id="95d64-167">True</span></span>
</dt> <dd>

<span data-ttu-id="95d64-168">O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="95d64-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="95d64-169">Falso</span><span class="sxs-lookup"><span data-stu-id="95d64-169">False</span></span>
</dt> <dd>

<span data-ttu-id="95d64-170">O provedor não dá suporte à recuperação de dados e retorna **o \_ provedor WBEM e \_ não é \_ \_ capaz** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="95d64-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="95d64-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-174">Se **for true**, o provedor de classe ou instância dará suporte à modificação de dados.</span><span class="sxs-lookup"><span data-stu-id="95d64-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="95d64-175">True</span><span class="sxs-lookup"><span data-stu-id="95d64-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-176">O provedor dá suporte à modificação de classe ou instância implementando um dos seguintes métodos: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).</span><span class="sxs-lookup"><span data-stu-id="95d64-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="95d64-177">For</span><span class="sxs-lookup"><span data-stu-id="95d64-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="95d64-178">O provedor não dá suporte à modificação de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ compatível** com [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="95d64-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95d64-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="95d64-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d64-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95d64-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d64-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="95d64-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="95d64-182">Não usado.</span><span class="sxs-lookup"><span data-stu-id="95d64-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d64-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="95d64-183">Remarks</span></span>

<span data-ttu-id="95d64-184">A classe **\_ \_ InstanceProviderRegistration** é derivada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="95d64-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="95d64-185">Somente os administradores podem registrar um provedor de instância criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ InstanceProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="95d64-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="95d64-186">Somente os administradores podem excluir um provedor.</span><span class="sxs-lookup"><span data-stu-id="95d64-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d64-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d64-187">Requirements</span></span>



| <span data-ttu-id="95d64-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d64-188">Requirement</span></span> | <span data-ttu-id="95d64-189">Valor</span><span class="sxs-lookup"><span data-stu-id="95d64-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="95d64-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95d64-190">Minimum supported client</span></span><br/> | <span data-ttu-id="95d64-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d64-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="95d64-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95d64-192">Minimum supported server</span></span><br/> | <span data-ttu-id="95d64-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d64-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="95d64-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="95d64-194">Namespace</span></span><br/>                | <span data-ttu-id="95d64-195">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="95d64-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="95d64-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="95d64-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d64-197">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="95d64-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="95d64-198">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="95d64-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="95d64-199">Registrando um provedor de classe</span><span class="sxs-lookup"><span data-stu-id="95d64-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="95d64-200">Registrando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="95d64-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

