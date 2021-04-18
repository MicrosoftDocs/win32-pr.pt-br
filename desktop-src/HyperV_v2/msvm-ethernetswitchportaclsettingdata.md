---
description: Representa a lista de controle de acesso (ACL) para as configurações de porta do comutador.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Classe Msvm_EthernetSwitchPortAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792522"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="d20d0-103">\_Classe Msvm EthernetSwitchPortAclSettingData</span><span class="sxs-lookup"><span data-stu-id="d20d0-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="d20d0-104">Representa a lista de controle de acesso (ACL) para as configurações de porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="d20d0-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="d20d0-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d20d0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d20d0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d20d0-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="d20d0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d20d0-107">Members</span></span>

<span data-ttu-id="d20d0-108">A classe **Msvm \_ EthernetSwitchPortAclSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d20d0-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d20d0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d20d0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d20d0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d20d0-110">Properties</span></span>

<span data-ttu-id="d20d0-111">A classe **Msvm \_ EthernetSwitchPortAclSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d20d0-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d20d0-112">**AclType**</span><span class="sxs-lookup"><span data-stu-id="d20d0-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-115">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-116">Isso indica o tipo de ponto de extremidade ACL.</span><span class="sxs-lookup"><span data-stu-id="d20d0-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d20d0-117">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="d20d0-118">**ACL do Mac** (1)</span><span class="sxs-lookup"><span data-stu-id="d20d0-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="d20d0-119">**ACL IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="d20d0-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="d20d0-120">**ACL IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="d20d0-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d20d0-121">**Ação**</span><span class="sxs-lookup"><span data-stu-id="d20d0-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-122">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-124">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-125">Isso indica a ação da ACL.</span><span class="sxs-lookup"><span data-stu-id="d20d0-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d20d0-126">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="d20d0-127">**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="d20d0-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="d20d0-128">**Negar** (2)</span><span class="sxs-lookup"><span data-stu-id="d20d0-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="d20d0-129">**Medidor** (3)</span><span class="sxs-lookup"><span data-stu-id="d20d0-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d20d0-130">**Aplicabilidade**</span><span class="sxs-lookup"><span data-stu-id="d20d0-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-131">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-133">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-134">Isso indica se a ACL se aplica ao ponto de extremidade local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d20d0-135">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="d20d0-136">**Local** (1)</span><span class="sxs-lookup"><span data-stu-id="d20d0-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="d20d0-137">**Remoto** (2)</span><span class="sxs-lookup"><span data-stu-id="d20d0-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d20d0-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d20d0-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d20d0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-141">A short description of the object.</span></span> <span data-ttu-id="d20d0-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de ACL de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d20d0-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-143">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d20d0-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d20d0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-146">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d20d0-146">A description of the object.</span></span> <span data-ttu-id="d20d0-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa a classe base para as configurações de porta do comutador.".</span><span class="sxs-lookup"><span data-stu-id="d20d0-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-148">**Direção**</span><span class="sxs-lookup"><span data-stu-id="d20d0-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-149">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-151">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-152">Isso indica se a ACL se aplica à direção de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="d20d0-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d20d0-153">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="d20d0-154">**Entrada** (1)</span><span class="sxs-lookup"><span data-stu-id="d20d0-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="d20d0-155">**Saída** (2)</span><span class="sxs-lookup"><span data-stu-id="d20d0-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d20d0-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d20d0-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d20d0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-159">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-159">A display name for the object.</span></span> <span data-ttu-id="d20d0-160">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de ACL de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="d20d0-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d20d0-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d20d0-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-164">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d20d0-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-165">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d20d0-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d20d0-166">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d20d0-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="d20d0-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-170">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-171">O endereço local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d20d0-171">The local address of the virtual machine.</span></span> <span data-ttu-id="d20d0-172">Pode ser um endereço IPv4, IPv6 ou MAC.</span><span class="sxs-lookup"><span data-stu-id="d20d0-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-173">**LocalAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="d20d0-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-174">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-176">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-177">O comprimento do prefixo do endereço local.</span><span class="sxs-lookup"><span data-stu-id="d20d0-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d20d0-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-182">O nome de exibição da ACL.</span><span class="sxs-lookup"><span data-stu-id="d20d0-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="d20d0-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d20d0-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-186">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-187">O endereço remoto da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d20d0-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="d20d0-188">Pode ser IPv4, IPv6 ou um endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="d20d0-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d20d0-189">**RemoteAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="d20d0-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d20d0-190">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d20d0-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d20d0-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d20d0-192">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="d20d0-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="d20d0-193">O comprimento do prefixo do endereço remoto.</span><span class="sxs-lookup"><span data-stu-id="d20d0-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d20d0-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d20d0-194">Requirements</span></span>



| <span data-ttu-id="d20d0-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="d20d0-195">Requirement</span></span> | <span data-ttu-id="d20d0-196">Valor</span><span class="sxs-lookup"><span data-stu-id="d20d0-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d20d0-197">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d20d0-197">Minimum supported client</span></span><br/> | <span data-ttu-id="d20d0-198">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d20d0-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d20d0-199">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d20d0-199">Minimum supported server</span></span><br/> | <span data-ttu-id="d20d0-200">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d20d0-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d20d0-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="d20d0-201">Namespace</span></span><br/>                | <span data-ttu-id="d20d0-202">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d20d0-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d20d0-203">MOF</span><span class="sxs-lookup"><span data-stu-id="d20d0-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d20d0-204"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d20d0-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d20d0-205">DLL</span><span class="sxs-lookup"><span data-stu-id="d20d0-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d20d0-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d20d0-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

