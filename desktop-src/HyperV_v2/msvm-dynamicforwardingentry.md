---
description: Representa uma entrada no banco de dados de encaminhamento (filtragem) associado ao serviço de ponte transparente.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Classe Msvm_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768754"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="a3448-103">\_Classe Msvm DynamicForwardingEntry</span><span class="sxs-lookup"><span data-stu-id="a3448-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="a3448-104">Representa uma entrada no banco de dados de encaminhamento (filtragem) associado ao serviço de ponte transparente.</span><span class="sxs-lookup"><span data-stu-id="a3448-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="a3448-105">A entrada é fraca para o serviço, conforme especificado por [**Msvm \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span><span class="sxs-lookup"><span data-stu-id="a3448-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="a3448-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a3448-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3448-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3448-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="a3448-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a3448-108">Members</span></span>

<span data-ttu-id="a3448-109">A classe **Msvm \_ DynamicForwardingEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a3448-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="a3448-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a3448-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3448-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a3448-111">Properties</span></span>

<span data-ttu-id="a3448-112">A classe **Msvm \_ DynamicForwardingEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a3448-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3448-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a3448-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-116">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a3448-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-117">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a3448-117">A short description of the object.</span></span> <span data-ttu-id="a3448-118">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-119">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-120">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-122">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="a3448-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a3448-123">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a3448-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3448-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a3448-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-128">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a3448-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-129">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a3448-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="a3448-130">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a3448-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="a3448-131">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a3448-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-135">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="a3448-135">A description of the object.</span></span> <span data-ttu-id="a3448-136">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-140">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="a3448-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a3448-141">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a3448-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3448-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-143">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-146">O status da entrada.</span><span class="sxs-lookup"><span data-stu-id="a3448-146">The status of the entry.</span></span> <span data-ttu-id="a3448-147">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a3448-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3448-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a3448-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Inválido** (2)</span><span class="sxs-lookup"><span data-stu-id="a3448-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a3448-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Aprendido** (3)</span><span class="sxs-lookup"><span data-stu-id="a3448-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a3448-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>Por **conta própria** (4)</span><span class="sxs-lookup"><span data-stu-id="a3448-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a3448-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Gerenciamento** (5)</span><span class="sxs-lookup"><span data-stu-id="a3448-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a3448-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a3448-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-156">Um nome de exibição para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a3448-156">A display name for the element.</span></span> <span data-ttu-id="a3448-157">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a3448-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-161">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="a3448-161">The current health of the element.</span></span> <span data-ttu-id="a3448-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 ("OK").</span><span class="sxs-lookup"><span data-stu-id="a3448-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="a3448-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a3448-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-164">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a3448-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-166">Preenchido automaticamente quando a máquina virtual é criada.</span><span class="sxs-lookup"><span data-stu-id="a3448-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="a3448-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a3448-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-171">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a3448-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a3448-172">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a3448-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a3448-173">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="a3448-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-177">Qualificadores: **chave**, **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="a3448-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-178">Endereço MAC unicast para o qual o serviço de ponte transparente tem informações de encaminhamento e filtragem.</span><span class="sxs-lookup"><span data-stu-id="a3448-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="a3448-179">O endereço MAC é formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits "canônica" de acordo com a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="a3448-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="a3448-180">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-181">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a3448-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-184">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a3448-184">The label by which the object is known.</span></span> <span data-ttu-id="a3448-185">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-186">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-189">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="a3448-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a3448-190">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a3448-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3448-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-193">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3448-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="a3448-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3448-196">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a3448-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-197">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-199">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="a3448-199">Provides high level status information.</span></span> <span data-ttu-id="a3448-200">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a3448-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a3448-201">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a3448-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3448-202">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3448-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-203">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a3448-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-206">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a3448-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-207">O **CreationClassName** do serviço de escopo.</span><span class="sxs-lookup"><span data-stu-id="a3448-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="a3448-208">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-209">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="a3448-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-212">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a3448-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-213">O nome do serviço de escopo.</span><span class="sxs-lookup"><span data-stu-id="a3448-213">The scoping service's name.</span></span> <span data-ttu-id="a3448-214">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="a3448-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a3448-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a3448-219">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a3448-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-220">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a3448-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3448-222">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="a3448-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3448-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a3448-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-226">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a3448-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-227">O **CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a3448-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="a3448-228">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a3448-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3448-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3448-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3448-232">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a3448-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3448-233">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a3448-233">The scoping system's name.</span></span> <span data-ttu-id="a3448-234">Essa propriedade é herdada do [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3448-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a3448-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="a3448-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3448-236">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3448-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3448-237">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a3448-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a3448-238">O identificador de LAN virtual associado a esta entrada.</span><span class="sxs-lookup"><span data-stu-id="a3448-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3448-239">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3448-239">Remarks</span></span>

<span data-ttu-id="a3448-240">O acesso à classe **Msvm \_ DynamicForwardingEntry** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a3448-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a3448-241">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a3448-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a3448-242">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3448-242">Examples</span></span>

<span data-ttu-id="a3448-243">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a3448-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3448-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3448-244">Requirements</span></span>



| <span data-ttu-id="a3448-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3448-245">Requirement</span></span> | <span data-ttu-id="a3448-246">Valor</span><span class="sxs-lookup"><span data-stu-id="a3448-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3448-247">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3448-247">Minimum supported client</span></span><br/> | <span data-ttu-id="a3448-248">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a3448-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a3448-249">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3448-249">Minimum supported server</span></span><br/> | <span data-ttu-id="a3448-250">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a3448-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3448-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3448-251">Namespace</span></span><br/>                | <span data-ttu-id="a3448-252">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a3448-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a3448-253">MOF</span><span class="sxs-lookup"><span data-stu-id="a3448-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3448-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3448-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3448-255">DLL</span><span class="sxs-lookup"><span data-stu-id="a3448-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3448-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3448-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3448-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3448-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3448-258">**\_DYNAMICFORWARDINGENTRY CIM**</span><span class="sxs-lookup"><span data-stu-id="a3448-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="a3448-259">[**\_DYNAMICFORWARDINGENTRY CIM**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3448-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

