---
description: Representa o status do recurso de largura de banda do comutador.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Classe Msvm_EthernetSwitchBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787107"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="c71f1-103">\_Classe Msvm EthernetSwitchBandwidthData</span><span class="sxs-lookup"><span data-stu-id="c71f1-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="c71f1-104">Representa o status do recurso de largura de banda do comutador.</span><span class="sxs-lookup"><span data-stu-id="c71f1-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="c71f1-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c71f1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71f1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c71f1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="c71f1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c71f1-107">Members</span></span>

<span data-ttu-id="c71f1-108">A classe **Msvm \_ EthernetSwitchBandwidthData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c71f1-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="c71f1-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c71f1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c71f1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c71f1-110">Properties</span></span>

<span data-ttu-id="c71f1-111">A classe **Msvm \_ EthernetSwitchBandwidthData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c71f1-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c71f1-112">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="c71f1-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c71f1-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-115">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c71f1-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-116">A largura de banda máxima disponível no comutador.</span><span class="sxs-lookup"><span data-stu-id="c71f1-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c71f1-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-120">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c71f1-120">A short description of the object.</span></span> <span data-ttu-id="c71f1-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c71f1-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c71f1-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-125">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c71f1-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-126">O nome da classe ou subclasse usada na criação dessa instância.</span><span class="sxs-lookup"><span data-stu-id="c71f1-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-127">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="c71f1-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c71f1-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-130">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c71f1-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-131">A largura de banda absoluta atual reservada no comutador para o fluxo padrão.</span><span class="sxs-lookup"><span data-stu-id="c71f1-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-132">**DefaultFlowReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="c71f1-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c71f1-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-135">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c71f1-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-136">A porcentagem atual da largura de banda reservada na opção para o fluxo padrão.</span><span class="sxs-lookup"><span data-stu-id="c71f1-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-137">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="c71f1-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-138">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c71f1-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-140">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c71f1-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-141">O peso atual para o fluxo padrão no comutador.</span><span class="sxs-lookup"><span data-stu-id="c71f1-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-142">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c71f1-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-145">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c71f1-145">A description of the object.</span></span> <span data-ttu-id="c71f1-146">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c71f1-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c71f1-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-150">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c71f1-150">A display name for the object.</span></span> <span data-ttu-id="c71f1-151">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c71f1-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c71f1-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-155">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c71f1-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-156">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c71f1-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c71f1-157">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c71f1-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c71f1-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-161">Qualificadores: **chave**, **substituição**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c71f1-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-162">O nome exclusivo do recurso.</span><span class="sxs-lookup"><span data-stu-id="c71f1-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-163">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="c71f1-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-164">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c71f1-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-166">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c71f1-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-167">A largura de banda atual reservada no comutador.</span><span class="sxs-lookup"><span data-stu-id="c71f1-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-168">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c71f1-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-171">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c71f1-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-172">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="c71f1-172">The hosting system's creation class name.</span></span> <span data-ttu-id="c71f1-173">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c71f1-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c71f1-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c71f1-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c71f1-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c71f1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c71f1-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c71f1-177">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c71f1-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c71f1-178">O nome do comutador virtual ao qual a instância de recurso associada está associada.</span><span class="sxs-lookup"><span data-stu-id="c71f1-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c71f1-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c71f1-179">Requirements</span></span>



| <span data-ttu-id="c71f1-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="c71f1-180">Requirement</span></span> | <span data-ttu-id="c71f1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="c71f1-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c71f1-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c71f1-182">Minimum supported client</span></span><br/> | <span data-ttu-id="c71f1-183">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c71f1-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c71f1-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c71f1-184">Minimum supported server</span></span><br/> | <span data-ttu-id="c71f1-185">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c71f1-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c71f1-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="c71f1-186">Namespace</span></span><br/>                | <span data-ttu-id="c71f1-187">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c71f1-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c71f1-188">MOF</span><span class="sxs-lookup"><span data-stu-id="c71f1-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c71f1-189"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c71f1-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c71f1-190">DLL</span><span class="sxs-lookup"><span data-stu-id="c71f1-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71f1-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c71f1-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

