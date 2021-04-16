---
description: Representa os recursos de um \_ objeto CIM VirtualSystemMigrationService.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: Classe CIM_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505808"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="d8935-103">\_Classe CIM VirtualSystemMigrationCapabilities</span><span class="sxs-lookup"><span data-stu-id="d8935-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="d8935-104">Representa os recursos de um objeto [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8935-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8935-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8935-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="d8935-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d8935-106">Members</span></span>

<span data-ttu-id="d8935-107">A classe **CIM \_ VirtualSystemMigrationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8935-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="d8935-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8935-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8935-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8935-109">Properties</span></span>

<span data-ttu-id="d8935-110">A classe **CIM \_ VirtualSystemMigrationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8935-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8935-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="d8935-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8935-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8935-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8935-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8935-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8935-114">Uma matriz que indica os métodos [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) com suporte para operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="d8935-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="d8935-115">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="d8935-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="d8935-116">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="d8935-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8935-117">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8935-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8935-118">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="d8935-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8935-119">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8935-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8935-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8935-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8935-121">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost (DestinationHost)**","**CIM \_ VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost (DestinationHost)**")</span><span class="sxs-lookup"><span data-stu-id="d8935-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="d8935-122">Uma matriz que contém os formatos com suporte para o parâmetro *DestinationHost* dos métodos [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) e [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) para o objeto [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8935-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="d8935-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="d8935-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8935-124">Suporte do formato de texto de nome de domínio de acordo com a RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="d8935-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="d8935-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="d8935-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d8935-126">Suporte do formato decimal pontilhado IPv4 de acordo com a RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="d8935-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="d8935-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="d8935-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d8935-128">Suporte ao formato de texto IPv6 de acordo com a RFC 4291</span><span class="sxs-lookup"><span data-stu-id="d8935-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8935-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8935-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8935-130">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="d8935-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8935-131">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8935-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8935-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8935-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8935-133">Uma matriz que indica os métodos [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) com suporte para operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="d8935-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="d8935-134">Enumeração de identificadores de método cuja implementação pode ser síncrona; ou seja, a operação pode ser concluída imediatamente e, portanto, o método pode não retornar um trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8935-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="d8935-135">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="d8935-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="d8935-136">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="d8935-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="d8935-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="d8935-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="d8935-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="d8935-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8935-139">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8935-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="d8935-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d8935-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d8935-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8935-141">Requirements</span></span>



| <span data-ttu-id="d8935-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8935-142">Requirement</span></span> | <span data-ttu-id="d8935-143">Valor</span><span class="sxs-lookup"><span data-stu-id="d8935-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8935-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8935-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d8935-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8935-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d8935-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8935-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d8935-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8935-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d8935-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8935-148">Namespace</span></span><br/>                | <span data-ttu-id="d8935-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d8935-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8935-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d8935-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8935-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8935-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8935-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d8935-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8935-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8935-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8935-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8935-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8935-155">**Recursos de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d8935-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

