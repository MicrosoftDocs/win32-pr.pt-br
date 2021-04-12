---
description: Serve como a classe pai para classes que são usadas para registrar provedores de classe e de instância no WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Classe __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296829"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="6a46b-103">\_\_Classe ObjectProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="6a46b-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="6a46b-104">A classe de sistema abstrata **\_ \_ ObjectProviderRegistration** serve como a classe pai para classes que são usadas para registrar provedores de classe e de instância no WMI.</span><span class="sxs-lookup"><span data-stu-id="6a46b-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="6a46b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6a46b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6a46b-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6a46b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a46b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a46b-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="6a46b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6a46b-108">Members</span></span>

<span data-ttu-id="6a46b-109">A classe **\_ \_ ObjectProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6a46b-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="6a46b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a46b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a46b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a46b-111">Properties</span></span>

<span data-ttu-id="6a46b-112">A classe **\_ \_ ObjectProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6a46b-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a46b-113">**Entre ações**</span><span class="sxs-lookup"><span data-stu-id="6a46b-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-114">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a46b-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-116">Indica se o provedor de classe ou instância fornece ou não seus próprios dados ou se baseia no WMI e no repositório de modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="6a46b-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="6a46b-117">Os provedores de pull dão suporte ao acesso dinâmico aos seus dados, e os provedores de push armazenam seus dados no repositório CIM e contam com o WMI para fornecer acesso a ele.</span><span class="sxs-lookup"><span data-stu-id="6a46b-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="6a46b-118">Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="6a46b-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="6a46b-119">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6a46b-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="6a46b-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="6a46b-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a46b-121">O provedor é um provedor de pull.</span><span class="sxs-lookup"><span data-stu-id="6a46b-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="6a46b-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="6a46b-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a46b-123">O provedor é um provedor de push.</span><span class="sxs-lookup"><span data-stu-id="6a46b-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="6a46b-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="6a46b-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a46b-125">O provedor é um provedor de verificação por push.</span><span class="sxs-lookup"><span data-stu-id="6a46b-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="6a46b-126">Observe que o push-Verify não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="6a46b-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a46b-127">**operador**</span><span class="sxs-lookup"><span data-stu-id="6a46b-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-128">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="6a46b-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a46b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-130">Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa um caminho de objeto para o provedor de objetos.</span><span class="sxs-lookup"><span data-stu-id="6a46b-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="6a46b-131">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="6a46b-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="6a46b-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a46b-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-135">Matriz dos tipos de suporte incluído no provedor para processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="6a46b-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="6a46b-136">Os provedores de classe não dão suporte a nenhum tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="6a46b-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="6a46b-137">Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta.</span><span class="sxs-lookup"><span data-stu-id="6a46b-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="6a46b-138">Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos valores a seguir (o tipo de propriedade é uma matriz).</span><span class="sxs-lookup"><span data-stu-id="6a46b-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="6a46b-139">"WQL: UnarySelect"</span><span class="sxs-lookup"><span data-stu-id="6a46b-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="6a46b-140">"WQL: referências"</span><span class="sxs-lookup"><span data-stu-id="6a46b-140">"WQL:References"</span></span>

<span data-ttu-id="6a46b-141">"WQL: ASSOCIATORS"</span><span class="sxs-lookup"><span data-stu-id="6a46b-141">"WQL:Associators"</span></span>

<span data-ttu-id="6a46b-142">"WQL: V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="6a46b-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="6a46b-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-146">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6a46b-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="6a46b-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-150">Se **for true**, o provedor dará suporte à exclusão de dados.</span><span class="sxs-lookup"><span data-stu-id="6a46b-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="6a46b-151">True</span><span class="sxs-lookup"><span data-stu-id="6a46b-151">True</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-152">O provedor dá suporte à exclusão de classe ou instância implementando um dos [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="6a46b-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-153">Falso</span><span class="sxs-lookup"><span data-stu-id="6a46b-153">False</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-154">O provedor não dá suporte à exclusão de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="6a46b-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a46b-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="6a46b-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-156">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-158">Se **for true**, o provedor dará suporte à enumeração de dados.</span><span class="sxs-lookup"><span data-stu-id="6a46b-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="6a46b-159">True</span><span class="sxs-lookup"><span data-stu-id="6a46b-159">True</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-160">O provedor dá suporte à enumeração de dados implementando um dos [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provedores de classe) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provedores de instância).</span><span class="sxs-lookup"><span data-stu-id="6a46b-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-161">Falso</span><span class="sxs-lookup"><span data-stu-id="6a46b-161">False</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-162">O provedor não oferece suporte à enumeração de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="6a46b-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a46b-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="6a46b-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-164">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-166">Se **for true**, o provedor de classe ou instância dará suporte à recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="6a46b-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="6a46b-167">True</span><span class="sxs-lookup"><span data-stu-id="6a46b-167">True</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-168">O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="6a46b-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6a46b-169">False</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-170">O provedor não dá suporte à recuperação de dados e retorna **o \_ provedor WBEM e \_ não é \_ \_ capaz** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="6a46b-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a46b-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="6a46b-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-174">Se **for true**, o provedor de classe ou instância dará suporte à modificação de dados.</span><span class="sxs-lookup"><span data-stu-id="6a46b-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="6a46b-175">True</span><span class="sxs-lookup"><span data-stu-id="6a46b-175">True</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-176">O provedor dá suporte à modificação de classe ou instância implementando um dos [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).</span><span class="sxs-lookup"><span data-stu-id="6a46b-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="6a46b-177">Falso</span><span class="sxs-lookup"><span data-stu-id="6a46b-177">False</span></span>
</dt> <dd>

<span data-ttu-id="6a46b-178">O provedor não dá suporte à modificação de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ compatível** com [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="6a46b-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a46b-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="6a46b-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a46b-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6a46b-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a46b-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a46b-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a46b-182">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6a46b-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a46b-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a46b-183">Remarks</span></span>

<span data-ttu-id="6a46b-184">A classe **\_ \_ ObjectProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="6a46b-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="6a46b-185">Os provedores de classe devem definir a propriedade **SupportsEnumeration** como **true** porque os provedores devem ser capazes de fornecer o WMI com uma lista de suas classes.</span><span class="sxs-lookup"><span data-stu-id="6a46b-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="6a46b-186">Se um provedor de classes tentar definir essa propriedade como **false**, o WMI sinalizará o registro como inválido.</span><span class="sxs-lookup"><span data-stu-id="6a46b-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="6a46b-187">Os provedores de instância não são necessários para dar suporte à enumeração e podem optar por definir **SupportsEnumeration** como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="6a46b-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="6a46b-188">Um provedor que define **QuerySupportLevels** como "WQL: UnarySelect" pode aceitar uma consulta que consiste na instrução SELECT básica como com suporte na versão 1,0 do WMI.</span><span class="sxs-lookup"><span data-stu-id="6a46b-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="6a46b-189">Os provedores de classe e de instância devem ser capazes de lidar com a propriedade do sistema de **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="6a46b-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="6a46b-190">Os provedores de classe também devem processar a propriedade do sistema de **\_ \_ superclasse** e o operador ISA.</span><span class="sxs-lookup"><span data-stu-id="6a46b-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="6a46b-191">O operador ISA é usado para expandir um conjunto de resultados para classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="6a46b-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="6a46b-192">Se um provedor receber uma consulta que não pode interpretar, ele solicitará que o WMI o manipule retornando o WBEM E um valor de erro **\_ \_ muito \_ complexo** .</span><span class="sxs-lookup"><span data-stu-id="6a46b-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="6a46b-193">Para obter uma descrição da sintaxe WQL válida, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="6a46b-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="6a46b-194">Um provedor que define **QuerySupportLevels** para **WQL: V1ProviderDefined** pode tentar dar suporte a um conjunto maior de sintaxe do SQL por seu próprio risco, como a `ORDER BY` cláusula.</span><span class="sxs-lookup"><span data-stu-id="6a46b-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="6a46b-195">O WMI não interpreta as cláusulas adicionais ou tenta garantir que o conjunto de resultados esteja correto.</span><span class="sxs-lookup"><span data-stu-id="6a46b-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="6a46b-196">Somente os administradores podem registrar ou excluir um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e registrando-o.</span><span class="sxs-lookup"><span data-stu-id="6a46b-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a46b-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a46b-197">Requirements</span></span>



| <span data-ttu-id="6a46b-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a46b-198">Requirement</span></span> | <span data-ttu-id="6a46b-199">Valor</span><span class="sxs-lookup"><span data-stu-id="6a46b-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6a46b-200">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a46b-200">Minimum supported client</span></span><br/> | <span data-ttu-id="6a46b-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a46b-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6a46b-202">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a46b-202">Minimum supported server</span></span><br/> | <span data-ttu-id="6a46b-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a46b-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6a46b-204">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a46b-204">Namespace</span></span><br/>                | <span data-ttu-id="6a46b-205">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="6a46b-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6a46b-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a46b-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a46b-207">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="6a46b-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="6a46b-208">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6a46b-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6a46b-209">Registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="6a46b-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

