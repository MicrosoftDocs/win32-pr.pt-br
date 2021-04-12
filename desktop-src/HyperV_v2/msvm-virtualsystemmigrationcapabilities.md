---
description: Define o meio pelo qual um cliente pode descobrir os métodos fornecidos pelo serviço de migração e o intervalo válido de dados de configuração de migração do sistema virtual.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Classe Msvm_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501369"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="f653b-103">\_Classe Msvm VirtualSystemMigrationCapabilities</span><span class="sxs-lookup"><span data-stu-id="f653b-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="f653b-104">Define o meio pelo qual um cliente pode descobrir os métodos fornecidos pelo serviço de migração e o intervalo válido de dados de configuração de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f653b-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="f653b-105">O objeto **Msvm \_ VirtualSystemMigrationCapabilities** é associado a objetos [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f653b-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="f653b-106">Essas associações definem o intervalo válido de serviços de migração disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f653b-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="f653b-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f653b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f653b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f653b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="f653b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f653b-109">Members</span></span>

<span data-ttu-id="f653b-110">A classe **Msvm \_ VirtualSystemMigrationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f653b-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f653b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f653b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f653b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f653b-112">Properties</span></span>

<span data-ttu-id="f653b-113">A classe **Msvm \_ VirtualSystemMigrationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f653b-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f653b-114">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="f653b-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-115">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f653b-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f653b-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f653b-117">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="f653b-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="f653b-118">Identifica os métodos cuja implementação pode ser assíncrona; ou seja, a operação não será concluída imediatamente e retornará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f653b-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="f653b-119">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="f653b-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="f653b-120">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="f653b-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="f653b-121">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="f653b-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="f653b-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span><span class="sxs-lookup"><span data-stu-id="f653b-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f653b-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f653b-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f653b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f653b-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f653b-126">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="f653b-126">A short description of the object.</span></span> <span data-ttu-id="f653b-127">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos de migração".</span><span class="sxs-lookup"><span data-stu-id="f653b-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="f653b-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f653b-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f653b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f653b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f653b-131">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="f653b-131">A description of the object.</span></span> <span data-ttu-id="f653b-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos de migração de sistema virtual".</span><span class="sxs-lookup"><span data-stu-id="f653b-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="f653b-133">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="f653b-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f653b-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f653b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f653b-136">Uma matriz de formatos de nome com suporte para o parâmetro *DestinationHost* dos métodos [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) e [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f653b-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="f653b-137">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="f653b-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="f653b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f653b-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="f653b-139">Significado</span><span class="sxs-lookup"><span data-stu-id="f653b-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="f653b-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f653b-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="f653b-141">Suporte do formato de nome de domínio de acordo com a RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="f653b-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="f653b-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f653b-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f653b-143">Suporte do formato decimal pontilhado IPv4 de acordo com a RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="f653b-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="f653b-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f653b-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="f653b-145">Suporte do formato de texto IPv6 de acordo com a RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="f653b-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="f653b-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f653b-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f653b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f653b-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f653b-149">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="f653b-149">A display name for the object.</span></span> <span data-ttu-id="f653b-150">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f653b-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f653b-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f653b-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f653b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f653b-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f653b-154">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="f653b-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f653b-155">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="f653b-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f653b-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f653b-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f653b-157">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="f653b-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f653b-158">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f653b-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f653b-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f653b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f653b-160">Identifica os métodos cuja implementação pode ser síncrona; ou seja, a operação será concluída imediatamente e não retornará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f653b-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="f653b-161">Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="f653b-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="f653b-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="f653b-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f653b-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="f653b-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f653b-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="f653b-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f653b-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="f653b-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f653b-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="f653b-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="f653b-167">)</span><span class="sxs-lookup"><span data-stu-id="f653b-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f653b-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f653b-168">Requirements</span></span>



| <span data-ttu-id="f653b-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="f653b-169">Requirement</span></span> | <span data-ttu-id="f653b-170">Valor</span><span class="sxs-lookup"><span data-stu-id="f653b-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f653b-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f653b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f653b-172">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f653b-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f653b-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f653b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f653b-174">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f653b-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f653b-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="f653b-175">Namespace</span></span><br/>                | <span data-ttu-id="f653b-176">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f653b-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f653b-177">MOF</span><span class="sxs-lookup"><span data-stu-id="f653b-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f653b-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f653b-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f653b-179">DLL</span><span class="sxs-lookup"><span data-stu-id="f653b-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f653b-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f653b-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

