---
description: Representa o status de descarregamento de hardware do comutador.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Classe Msvm_EthernetSwitchHardwareOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750844"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="8ccac-103">\_Classe Msvm EthernetSwitchHardwareOffloadData</span><span class="sxs-lookup"><span data-stu-id="8ccac-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="8ccac-104">Representa o status de descarregamento de hardware do comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="8ccac-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8ccac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ccac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ccac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="8ccac-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8ccac-107">Members</span></span>

<span data-ttu-id="8ccac-108">A classe **Msvm \_ EthernetSwitchHardwareOffloadData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8ccac-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="8ccac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ccac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ccac-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ccac-110">Properties</span></span>

<span data-ttu-id="8ccac-111">A classe **Msvm \_ EthernetSwitchHardwareOffloadData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8ccac-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ccac-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8ccac-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8ccac-115">A short description of the object.</span></span> <span data-ttu-id="8ccac-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ccac-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ccac-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-120">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ccac-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-121">O nome da classe ou subclasse usada na criação dessa instância.</span><span class="sxs-lookup"><span data-stu-id="8ccac-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="8ccac-122">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="8ccac-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-123">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="8ccac-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ccac-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-126">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-127">A configuração de VMMQ atual para a fila padrão</span><span class="sxs-lookup"><span data-stu-id="8ccac-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-128">Propriedade adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="8ccac-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-129">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="8ccac-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-132">Qualificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-133">O número atual de filas alocadas para a fila padrão</span><span class="sxs-lookup"><span data-stu-id="8ccac-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-134">Propriedade adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="8ccac-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-135">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="8ccac-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ccac-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-138">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-139">A configuração de VRss atual para a fila padrão</span><span class="sxs-lookup"><span data-stu-id="8ccac-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-140">Propriedade adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="8ccac-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-141">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="8ccac-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ccac-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-144">Qualificadores: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-145">Indica se a CPU de VMQ primária foi excluída da tabela de indireção VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="8ccac-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-146">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="8ccac-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-147">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="8ccac-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ccac-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-150">Qualificadores: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-151">Indica se a difusão do VRSS deve ser sempre feita para a fila padrão, independentemente do estado de RSS do vPort externo.</span><span class="sxs-lookup"><span data-stu-id="8ccac-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-152">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="8ccac-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-153">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="8ccac-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-156">Qualificadores: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-157">Indica o número mínimo de filas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="8ccac-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-158">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="8ccac-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-159">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="8ccac-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-162">Qualificadores: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-163">Indica como as filas VRSS/VMMQ são direcionadas para processadores de host diferentes.</span><span class="sxs-lookup"><span data-stu-id="8ccac-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-164">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="8ccac-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-165">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ccac-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-168">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8ccac-168">A description of the object.</span></span> <span data-ttu-id="8ccac-169">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ccac-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8ccac-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-173">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8ccac-173">A display name for the object.</span></span> <span data-ttu-id="8ccac-174">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ccac-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ccac-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-178">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8ccac-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-179">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8ccac-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8ccac-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ccac-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-181">**IovQueuePairCapacity**</span><span class="sxs-lookup"><span data-stu-id="8ccac-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-184">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-185">O número máximo de pares de fila com suporte no comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-186">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="8ccac-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-189">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-190">O número atual de pares de fila que estão sendo usados pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-191">**IovVfCapacity**</span><span class="sxs-lookup"><span data-stu-id="8ccac-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-192">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-194">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-195">O número máximo de funções virtuais com suporte no comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-196">**IovVfUsage**</span><span class="sxs-lookup"><span data-stu-id="8ccac-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-199">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-200">O número atual de funções virtuais que estão sendo usadas pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-201">**IPsecSACapacity**</span><span class="sxs-lookup"><span data-stu-id="8ccac-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-202">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-204">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-205">O número máximo de descarregamentos de associação de segurança IPsec com suporte no comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-206">**IPsecSAUsage**</span><span class="sxs-lookup"><span data-stu-id="8ccac-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-209">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-210">O número atual de descarregamentos de associação de segurança IPsec que estão sendo usados pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-211">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8ccac-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-214">Qualificadores: **chave**, **substituição**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ccac-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-215">O nome exclusivo do recurso.</span><span class="sxs-lookup"><span data-stu-id="8ccac-215">The unique name of the resource.</span></span> <span data-ttu-id="8ccac-216">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="8ccac-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-217">**PacketDirectInUse**</span><span class="sxs-lookup"><span data-stu-id="8ccac-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-218">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ccac-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-220">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-221">Indica se o pacote direto está sendo usado pelo comutador</span><span class="sxs-lookup"><span data-stu-id="8ccac-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="8ccac-222">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8ccac-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8ccac-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ccac-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-226">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ccac-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-227">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="8ccac-227">The hosting system's creation class name.</span></span> <span data-ttu-id="8ccac-228">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="8ccac-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8ccac-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ccac-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-232">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ccac-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-233">O nome do comutador virtual ao qual a instância de recurso associada está associada.</span><span class="sxs-lookup"><span data-stu-id="8ccac-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="8ccac-234">Esta propriedade é herdada de [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="8ccac-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-235">**VmqCapacity**</span><span class="sxs-lookup"><span data-stu-id="8ccac-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-236">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-238">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-239">O número máximo de descarregamentos de fila de máquina virtual com suporte no comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="8ccac-240">**VmqUsage**</span><span class="sxs-lookup"><span data-stu-id="8ccac-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ccac-241">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ccac-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ccac-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ccac-243">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8ccac-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8ccac-244">O número atual de descarregamentos de fila de máquina virtual que estão sendo usados pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="8ccac-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ccac-245">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ccac-245">Requirements</span></span>



| <span data-ttu-id="8ccac-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ccac-246">Requirement</span></span> | <span data-ttu-id="8ccac-247">Valor</span><span class="sxs-lookup"><span data-stu-id="8ccac-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ccac-248">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ccac-248">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccac-249">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8ccac-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ccac-250">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ccac-250">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccac-251">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8ccac-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ccac-252">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ccac-252">Namespace</span></span><br/>                | <span data-ttu-id="8ccac-253">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8ccac-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8ccac-254">MOF</span><span class="sxs-lookup"><span data-stu-id="8ccac-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ccac-255"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ccac-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ccac-256">DLL</span><span class="sxs-lookup"><span data-stu-id="8ccac-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ccac-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ccac-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

