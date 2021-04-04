---
description: Representa os dados de configuração do recurso de segurança.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Classe Msvm_EthernetSwitchPortSecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837514"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="901e1-103">\_Classe Msvm EthernetSwitchPortSecuritySettingData</span><span class="sxs-lookup"><span data-stu-id="901e1-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="901e1-104">Representa os dados de configuração do recurso de segurança.</span><span class="sxs-lookup"><span data-stu-id="901e1-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="901e1-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="901e1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="901e1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="901e1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="901e1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="901e1-107">Members</span></span>

<span data-ttu-id="901e1-108">A classe **Msvm \_ EthernetSwitchPortSecuritySettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="901e1-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="901e1-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="901e1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="901e1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="901e1-110">Properties</span></span>

<span data-ttu-id="901e1-111">A classe **Msvm \_ EthernetSwitchPortSecuritySettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="901e1-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="901e1-112">**AllowIeeePriorityTag**</span><span class="sxs-lookup"><span data-stu-id="901e1-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-115">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-116">Especifica se o tráfego de/para a porta retém informações de 802.1 P.</span><span class="sxs-lookup"><span data-stu-id="901e1-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="901e1-117">Conterá **true** se o tráfego de/para a porta mantiver informações 802.1 p ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="901e1-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="901e1-118">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="901e1-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-119">**AllowMacSpoofing**</span><span class="sxs-lookup"><span data-stu-id="901e1-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-122">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-123">Indica se a porta permitirá a falsificação de MAC.</span><span class="sxs-lookup"><span data-stu-id="901e1-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="901e1-124">Se essa propriedade for **true**, a porta permitirá que os endereços MAC sejam falsificados.</span><span class="sxs-lookup"><span data-stu-id="901e1-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="901e1-125">Todos os valores válidos de endereço MAC de unicast são permitidos.</span><span class="sxs-lookup"><span data-stu-id="901e1-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="901e1-126">Se essa propriedade for **falsa**, a porta só permitirá que os endereços MAC configurados no gerenciamento do Hyper-V sejam usados.</span><span class="sxs-lookup"><span data-stu-id="901e1-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="901e1-127">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="901e1-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-128">**AllowTeaming**</span><span class="sxs-lookup"><span data-stu-id="901e1-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-131">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-132">Indica se as NICs conectadas à porta podem fazer parte de uma equipe.</span><span class="sxs-lookup"><span data-stu-id="901e1-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="901e1-133">Isso se aplica somente a NICs conectadas a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="901e1-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="901e1-134">Contém **true** se o agrupamento NIC for permitido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="901e1-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="901e1-135">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="901e1-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-136">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="901e1-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="901e1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="901e1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="901e1-139">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="901e1-139">A short description of the object.</span></span> <span data-ttu-id="901e1-140">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de segurança de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="901e1-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="901e1-141">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="901e1-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="901e1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="901e1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="901e1-144">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="901e1-144">A description of the object.</span></span> <span data-ttu-id="901e1-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de configuração do recurso de segurança.".</span><span class="sxs-lookup"><span data-stu-id="901e1-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="901e1-146">**DynamicIPAddressLimit**</span><span class="sxs-lookup"><span data-stu-id="901e1-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="901e1-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-149">Qualificadores: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-150">Define o limite para o número de endereços IP dinâmicos aprendidos.</span><span class="sxs-lookup"><span data-stu-id="901e1-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="901e1-151">O padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="901e1-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="901e1-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="901e1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="901e1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="901e1-155">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="901e1-155">A display name for the object.</span></span> <span data-ttu-id="901e1-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de segurança de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="901e1-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="901e1-157">**EnableDhcpGuard**</span><span class="sxs-lookup"><span data-stu-id="901e1-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-158">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-160">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-161">Especifica se as ofertas DHCP estão bloqueadas da porta.</span><span class="sxs-lookup"><span data-stu-id="901e1-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="901e1-162">Contém **true** se as ofertas DHCP forem bloqueadas da porta ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="901e1-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="901e1-163">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="901e1-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="901e1-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-167">Qualificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-168">Defina como TRUE se a velocidade fixa 10G estiver habilitada, caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="901e1-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="901e1-169">O valor padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="901e1-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="901e1-170">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="901e1-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="901e1-171">**EnableRouterGuard**</span><span class="sxs-lookup"><span data-stu-id="901e1-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-174">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-175">Especifica se anúncios de roteador e redirecionamentos de roteador estão bloqueados da porta.</span><span class="sxs-lookup"><span data-stu-id="901e1-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="901e1-176">Conterá **true** se anúncios de roteador e redirecionamentos de roteador forem bloqueados da porta ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="901e1-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="901e1-177">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="901e1-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="901e1-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="901e1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="901e1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="901e1-181">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="901e1-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="901e1-182">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="901e1-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="901e1-183">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="901e1-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="901e1-184">**Monitormode**</span><span class="sxs-lookup"><span data-stu-id="901e1-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-185">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="901e1-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-186">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-187">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-188">Isso indica o modo de monitor da porta.</span><span class="sxs-lookup"><span data-stu-id="901e1-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="901e1-189">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="901e1-190">**Destino** (1)</span><span class="sxs-lookup"><span data-stu-id="901e1-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="901e1-191">**Origem** (2)</span><span class="sxs-lookup"><span data-stu-id="901e1-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="901e1-192">**MonitorSession**</span><span class="sxs-lookup"><span data-stu-id="901e1-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-193">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="901e1-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-194">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-195">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-196">Especifica o identificador da sessão de monitor à qual esta porta pertence.</span><span class="sxs-lookup"><span data-stu-id="901e1-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="901e1-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-198">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="901e1-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-200">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-201">Reservado</span><span class="sxs-lookup"><span data-stu-id="901e1-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="901e1-202">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="901e1-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="901e1-203">**StormLimit**</span><span class="sxs-lookup"><span data-stu-id="901e1-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-204">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="901e1-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-206">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-207">Define o limite de pacotes por segundo para o tráfego de difusão e multicast.</span><span class="sxs-lookup"><span data-stu-id="901e1-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="901e1-208">O padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="901e1-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-209">**TeamName**</span><span class="sxs-lookup"><span data-stu-id="901e1-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="901e1-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-212">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-213">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="901e1-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="901e1-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-215">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="901e1-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-217">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="901e1-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-218">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="901e1-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="901e1-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="901e1-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="901e1-220">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="901e1-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="901e1-221">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="901e1-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="901e1-222">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="901e1-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="901e1-223">Especifica o identificador da sub-rede virtual da qual a porta é membro.</span><span class="sxs-lookup"><span data-stu-id="901e1-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="901e1-224">O padrão é none.</span><span class="sxs-lookup"><span data-stu-id="901e1-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="901e1-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="901e1-225">Requirements</span></span>



| <span data-ttu-id="901e1-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="901e1-226">Requirement</span></span> | <span data-ttu-id="901e1-227">Valor</span><span class="sxs-lookup"><span data-stu-id="901e1-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="901e1-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="901e1-228">Minimum supported client</span></span><br/> | <span data-ttu-id="901e1-229">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="901e1-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="901e1-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="901e1-230">Minimum supported server</span></span><br/> | <span data-ttu-id="901e1-231">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="901e1-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="901e1-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="901e1-232">Namespace</span></span><br/>                | <span data-ttu-id="901e1-233">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="901e1-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="901e1-234">MOF</span><span class="sxs-lookup"><span data-stu-id="901e1-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="901e1-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="901e1-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="901e1-236">DLL</span><span class="sxs-lookup"><span data-stu-id="901e1-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="901e1-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="901e1-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

