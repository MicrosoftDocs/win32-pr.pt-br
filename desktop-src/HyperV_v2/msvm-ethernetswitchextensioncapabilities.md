---
description: Representa a associação entre as extensões Ethernet e seus recursos.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Classe Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663607"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="7d8a5-103">\_Classe Msvm EthernetSwitchExtensionCapabilities</span><span class="sxs-lookup"><span data-stu-id="7d8a5-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="7d8a5-104">Representa a associação entre as extensões Ethernet e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="7d8a5-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8a5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d8a5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="7d8a5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7d8a5-107">Members</span></span>

<span data-ttu-id="7d8a5-108">A classe **Msvm \_ EthernetSwitchExtensionCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7d8a5-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="7d8a5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d8a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d8a5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d8a5-110">Properties</span></span>

<span data-ttu-id="7d8a5-111">A classe **Msvm \_ EthernetSwitchExtensionCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d8a5-112">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d8a5-113">Tipo de dados: **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7d8a5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d8a5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d8a5-115">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("recursos")</span><span class="sxs-lookup"><span data-stu-id="7d8a5-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="7d8a5-116">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa o objeto Capabilities associado à opção.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="7d8a5-117">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="7d8a5-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="7d8a5-118">**Características**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d8a5-119">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d8a5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d8a5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d8a5-121">Fornece informações descritivas sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="7d8a5-122">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="7d8a5-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="7d8a5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7d8a5-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="7d8a5-124">Significado</span><span class="sxs-lookup"><span data-stu-id="7d8a5-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="7d8a5-125"><dt>**Padrão**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a5-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7d8a5-126">Os recursos associados representam os recursos padrão do elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="7d8a5-127"><dt>**Atual**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a5-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="7d8a5-128">Os recursos associados representam os recursos atuais do elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d8a5-129">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d8a5-130">Tipo de dados: **[ **Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="7d8a5-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7d8a5-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d8a5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d8a5-132">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("managedelement")</span><span class="sxs-lookup"><span data-stu-id="7d8a5-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="7d8a5-133">Uma referência a uma instância da classe [**Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) que representa a extensão instalada.</span><span class="sxs-lookup"><span data-stu-id="7d8a5-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="7d8a5-134">Essa propriedade é herdada do [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="7d8a5-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d8a5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d8a5-135">Requirements</span></span>



| <span data-ttu-id="7d8a5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8a5-136">Requirement</span></span> | <span data-ttu-id="7d8a5-137">Valor</span><span class="sxs-lookup"><span data-stu-id="7d8a5-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8a5-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d8a5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8a5-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7d8a5-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d8a5-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d8a5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8a5-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7d8a5-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d8a5-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d8a5-142">Namespace</span></span><br/>                | <span data-ttu-id="7d8a5-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7d8a5-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d8a5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7d8a5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d8a5-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a5-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d8a5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7d8a5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d8a5-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a5-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

