---
description: Representa uma instância de um componente de extensão instalado em um sistema de host.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Classe Msvm_InstalledEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754667"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="71374-103">\_Classe Msvm InstalledEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="71374-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="71374-104">Representa uma instância de um componente de extensão instalado em um sistema de host.</span><span class="sxs-lookup"><span data-stu-id="71374-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="71374-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="71374-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71374-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71374-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="71374-107">Membros</span><span class="sxs-lookup"><span data-stu-id="71374-107">Members</span></span>

<span data-ttu-id="71374-108">A classe **Msvm \_ InstalledEthernetSwitchExtension** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71374-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="71374-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71374-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71374-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71374-110">Properties</span></span>

<span data-ttu-id="71374-111">A classe **Msvm \_ InstalledEthernetSwitchExtension** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="71374-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71374-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="71374-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71374-115">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="71374-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="71374-116">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="71374-116">A short description of the object.</span></span> <span data-ttu-id="71374-117">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="71374-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-118">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="71374-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71374-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-121">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="71374-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="71374-122">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="71374-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="71374-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="71374-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-127">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="71374-127">A description of the object.</span></span> <span data-ttu-id="71374-128">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="71374-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="71374-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71374-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-132">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="71374-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="71374-133">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="71374-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="71374-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="71374-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-138">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="71374-138">A display name for the object.</span></span> <span data-ttu-id="71374-139">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="71374-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="71374-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-141">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="71374-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71374-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-143">Indica o tipo do componente de extensão.</span><span class="sxs-lookup"><span data-stu-id="71374-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71374-144">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="71374-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="71374-145">**Captura** (1)</span><span class="sxs-lookup"><span data-stu-id="71374-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="71374-146">**Filtro** (2)</span><span class="sxs-lookup"><span data-stu-id="71374-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="71374-147">**Encaminhamento** (3)</span><span class="sxs-lookup"><span data-stu-id="71374-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="71374-148">**Monitoramento** (4)</span><span class="sxs-lookup"><span data-stu-id="71374-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="71374-149">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="71374-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71374-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="71374-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71374-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-153">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="71374-153">The current health of the element.</span></span> <span data-ttu-id="71374-154">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="71374-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="71374-155">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="71374-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="71374-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="71374-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="71374-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71374-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-158">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71374-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71374-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-160">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="71374-160">The date and time when the object was installed.</span></span> <span data-ttu-id="71374-161">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="71374-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="71374-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="71374-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71374-166">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="71374-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="71374-167">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="71374-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="71374-168">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="71374-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="71374-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71374-172">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="71374-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71374-173">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="71374-173">The label by which the object is known.</span></span> <span data-ttu-id="71374-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-175">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="71374-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-176">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71374-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-178">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="71374-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="71374-179">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="71374-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="71374-180">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="71374-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-182">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="71374-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-184">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="71374-184">The current statuses of the object.</span></span> <span data-ttu-id="71374-185">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="71374-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="71374-186">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="71374-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71374-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71374-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-189">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="71374-189">Provides high level status information.</span></span> <span data-ttu-id="71374-190">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="71374-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="71374-191">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="71374-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="71374-192">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="71374-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="71374-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-196">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="71374-196">The current status of the object.</span></span> <span data-ttu-id="71374-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="71374-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="71374-198">PROBLEMAS</span><span class="sxs-lookup"><span data-stu-id="71374-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="71374-199"><span id="OK"></span><span id="ok"></span>**Okey**</span><span class="sxs-lookup"><span data-stu-id="71374-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="71374-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ao**</span><span class="sxs-lookup"><span data-stu-id="71374-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="71374-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado**</span><span class="sxs-lookup"><span data-stu-id="71374-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="71374-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="71374-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="71374-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Falha de Pred**</span><span class="sxs-lookup"><span data-stu-id="71374-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="71374-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Comece**</span><span class="sxs-lookup"><span data-stu-id="71374-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="71374-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Impedir**</span><span class="sxs-lookup"><span data-stu-id="71374-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="71374-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço**</span><span class="sxs-lookup"><span data-stu-id="71374-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="71374-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Analisa**</span><span class="sxs-lookup"><span data-stu-id="71374-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="71374-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Não recuperar**</span><span class="sxs-lookup"><span data-stu-id="71374-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="71374-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato**</span><span class="sxs-lookup"><span data-stu-id="71374-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="71374-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Com perda de comunicação**</span><span class="sxs-lookup"><span data-stu-id="71374-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71374-211">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="71374-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-212">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="71374-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-214">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="71374-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="71374-215">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="71374-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="71374-216">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="71374-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-219">Indica o fornecedor que fornece a extensão.</span><span class="sxs-lookup"><span data-stu-id="71374-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="71374-220">**Versão**</span><span class="sxs-lookup"><span data-stu-id="71374-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71374-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71374-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71374-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71374-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71374-223">A versão da extensão em um formato de "Major. Minor", por exemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="71374-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71374-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71374-224">Requirements</span></span>



| <span data-ttu-id="71374-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="71374-225">Requirement</span></span> | <span data-ttu-id="71374-226">Valor</span><span class="sxs-lookup"><span data-stu-id="71374-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71374-227">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71374-227">Minimum supported client</span></span><br/> | <span data-ttu-id="71374-228">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="71374-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="71374-229">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71374-229">Minimum supported server</span></span><br/> | <span data-ttu-id="71374-230">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="71374-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71374-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="71374-231">Namespace</span></span><br/>                | <span data-ttu-id="71374-232">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="71374-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="71374-233">MOF</span><span class="sxs-lookup"><span data-stu-id="71374-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71374-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71374-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71374-235">DLL</span><span class="sxs-lookup"><span data-stu-id="71374-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71374-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71374-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

