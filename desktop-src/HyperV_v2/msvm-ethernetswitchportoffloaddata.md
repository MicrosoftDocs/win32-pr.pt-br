---
description: Representa os dados de status do recurso de descarregamento de porta.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Classe Msvm_EthernetSwitchPortOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764687"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="cd6d7-103">\_Classe Msvm EthernetSwitchPortOffloadData</span><span class="sxs-lookup"><span data-stu-id="cd6d7-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="cd6d7-104">Representa os dados de status do recurso de descarregamento de porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="cd6d7-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6d7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd6d7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="cd6d7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cd6d7-107">Members</span></span>

<span data-ttu-id="cd6d7-108">A classe **Msvm \_ EthernetSwitchPortOffloadData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd6d7-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="cd6d7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd6d7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd6d7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd6d7-110">Properties</span></span>

<span data-ttu-id="cd6d7-111">A classe **Msvm \_ EthernetSwitchPortOffloadData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd6d7-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-115">A short description of the object.</span></span> <span data-ttu-id="cd6d7-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de descarregamento de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-120">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-121">O nome da subclasse usada na criação desta instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="cd6d7-122">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPortOffloadData".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-126">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="cd6d7-126">A description of the object.</span></span> <span data-ttu-id="cd6d7-127">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de status do recurso de descarregamento de porta.".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-131">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-132">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-132">The scoping system's creation class name.</span></span> <span data-ttu-id="cd6d7-133">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-137">Qualificadores: **chave**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-138">A ID do dispositivo da porta que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="cd6d7-139">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="cd6d7-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-143">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-143">A display name for the object.</span></span> <span data-ttu-id="cd6d7-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de descarregamento de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-148">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-149">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cd6d7-150">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd6d7-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-151">**IovOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-154">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-155">O uso de descarregamento de IOV (virtualização de e/s) atual.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-156">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-159">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-160">O número atual de pares de fila que estão sendo usados pela porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-161">**IovVfDataPathActive**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-162">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-164">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-165">Indica se o caminho de dados de IOV VF está ativo.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-166">**IovVfId**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-169">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-170">O identificador FV de IOV atual que é atribuído à porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="cd6d7-171">Isso será válido se **IovOffloadUsage** não for zero.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-172">**IpsecCurrentOffloadSaCount**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-175">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-176">O número atual de Slots de descarga SA (Associação de segurança) em uso na porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-180">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-181">Uma cadeia de caracteres que identifica exclusivamente essa instância de dados de porta dentro do escopo do comutador e da porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="cd6d7-182">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="cd6d7-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-183">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-186">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-187">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-187">The scoping system's creation class name.</span></span> <span data-ttu-id="cd6d7-188">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="cd6d7-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-192">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-193">O nome do comutador virtual que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="cd6d7-194">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="cd6d7-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-195">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-198">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-199">Indica se VMMQ está ativo.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-200">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-201">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-202">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-204">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-205">Indica quantas filas são usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-206">Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-207">**VMQId**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-209">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-210">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-211">O identificador da fila da máquina virtual atual que é atribuído à porta.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="cd6d7-212">Isso será válido se **VMQOffloadUsage** não for zero.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-213">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-215">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd6d7-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-216">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-217">O uso de descarregamento da VMQ (fila de máquina virtual) atual.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="cd6d7-218">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-221">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-222">Indica se o vRSS está ativo.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-223">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-224">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-225">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-227">Qualificadores: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-228">Indica se a CPU de VMQ primária foi excluída da tabela de indireção VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-229">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-230">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-233">Qualificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-234">Indica se a dispersão de VRSS/VMMQ do lado do host ocorre, independentemente das configurações de RSS da NIC virtual.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-235">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-236">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-237">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-239">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-240">Indica o número mínimo de filas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-241">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-242">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-243">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-245">Qualificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-246">Indica como as filas VRSS/VMMQ são direcionadas para processadores de host diferentes.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-247">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd6d7-248">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6d7-249">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd6d7-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd6d7-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6d7-251">Qualificadores: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cd6d7-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cd6d7-252">Indica como os canais VMBus são relacionados para os processadores de host.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="cd6d7-253">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="cd6d7-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd6d7-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd6d7-254">Requirements</span></span>



| <span data-ttu-id="cd6d7-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6d7-255">Requirement</span></span> | <span data-ttu-id="cd6d7-256">Valor</span><span class="sxs-lookup"><span data-stu-id="cd6d7-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6d7-257">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd6d7-257">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6d7-258">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd6d7-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd6d7-259">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd6d7-259">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6d7-260">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd6d7-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd6d7-261">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd6d7-261">Namespace</span></span><br/>                | <span data-ttu-id="cd6d7-262">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cd6d7-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd6d7-263">MOF</span><span class="sxs-lookup"><span data-stu-id="cd6d7-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd6d7-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd6d7-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd6d7-265">DLL</span><span class="sxs-lookup"><span data-stu-id="cd6d7-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd6d7-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd6d7-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

