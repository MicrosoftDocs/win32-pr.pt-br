---
description: Representa parâmetros operacionais de switch.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Classe Msvm_EthernetSwitchOperationalData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297781"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="081dc-103">\_Classe Msvm EthernetSwitchOperationalData</span><span class="sxs-lookup"><span data-stu-id="081dc-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="081dc-104">Representa parâmetros operacionais de switch.</span><span class="sxs-lookup"><span data-stu-id="081dc-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="081dc-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="081dc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="081dc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="081dc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="081dc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="081dc-107">Members</span></span>

<span data-ttu-id="081dc-108">A classe **Msvm \_ EthernetSwitchOperationalData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="081dc-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="081dc-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="081dc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="081dc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="081dc-110">Properties</span></span>

<span data-ttu-id="081dc-111">A classe **Msvm \_ EthernetSwitchOperationalData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="081dc-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="081dc-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="081dc-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="081dc-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="081dc-115">A short description of the object.</span></span> <span data-ttu-id="081dc-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="081dc-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="081dc-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-120">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="081dc-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-121">O nome da classe ou subclasse usada na criação dessa instância.</span><span class="sxs-lookup"><span data-stu-id="081dc-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="081dc-122">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="081dc-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-123">**CurrentSwitchingMode**</span><span class="sxs-lookup"><span data-stu-id="081dc-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="081dc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-126">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="081dc-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-127">O modo de troca atual no comutador.</span><span class="sxs-lookup"><span data-stu-id="081dc-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="081dc-128">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="081dc-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="081dc-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="081dc-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="081dc-130">**802.1 qbg** (2)</span><span class="sxs-lookup"><span data-stu-id="081dc-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="081dc-131">**802.1 qbh** (3)</span><span class="sxs-lookup"><span data-stu-id="081dc-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="081dc-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="081dc-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="081dc-135">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="081dc-135">A description of the object.</span></span> <span data-ttu-id="081dc-136">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="081dc-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="081dc-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="081dc-140">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="081dc-140">A display name for the object.</span></span> <span data-ttu-id="081dc-141">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="081dc-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="081dc-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-145">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="081dc-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="081dc-146">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="081dc-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="081dc-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="081dc-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="081dc-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-151">Qualificadores: **chave**, **substituição**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="081dc-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-152">O nome exclusivo do recurso.</span><span class="sxs-lookup"><span data-stu-id="081dc-152">The unique name of the resource.</span></span> <span data-ttu-id="081dc-153">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="081dc-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-154">**SupportedSwitchingModes**</span><span class="sxs-lookup"><span data-stu-id="081dc-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-155">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="081dc-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="081dc-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-157">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="081dc-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-158">Os modos de comutação com suporte no comutador.</span><span class="sxs-lookup"><span data-stu-id="081dc-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="081dc-159">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="081dc-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-162">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="081dc-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-163">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="081dc-163">The hosting system's creation class name.</span></span> <span data-ttu-id="081dc-164">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="081dc-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="081dc-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="081dc-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="081dc-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="081dc-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="081dc-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="081dc-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="081dc-168">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="081dc-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="081dc-169">O nome do comutador virtual ao qual a instância de recurso associada está associada.</span><span class="sxs-lookup"><span data-stu-id="081dc-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="081dc-170">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="081dc-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="081dc-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="081dc-171">Requirements</span></span>



| <span data-ttu-id="081dc-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="081dc-172">Requirement</span></span> | <span data-ttu-id="081dc-173">Valor</span><span class="sxs-lookup"><span data-stu-id="081dc-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="081dc-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="081dc-174">Minimum supported client</span></span><br/> | <span data-ttu-id="081dc-175">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="081dc-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="081dc-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="081dc-176">Minimum supported server</span></span><br/> | <span data-ttu-id="081dc-177">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="081dc-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="081dc-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="081dc-178">Namespace</span></span><br/>                | <span data-ttu-id="081dc-179">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="081dc-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="081dc-180">MOF</span><span class="sxs-lookup"><span data-stu-id="081dc-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="081dc-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="081dc-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="081dc-182">DLL</span><span class="sxs-lookup"><span data-stu-id="081dc-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="081dc-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="081dc-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

