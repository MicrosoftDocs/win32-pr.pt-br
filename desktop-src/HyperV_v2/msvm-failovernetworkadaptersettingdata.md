---
description: Representa as configurações de um adaptador de rede dentro do sistema operacional convidado, que será aplicado no momento de um failover.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Classe Msvm_FailoverNetworkAdapterSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764686"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="1f95e-103">\_Classe Msvm FailoverNetworkAdapterSettingData</span><span class="sxs-lookup"><span data-stu-id="1f95e-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="1f95e-104">Representa as configurações de um adaptador de rede dentro do sistema operacional convidado, que será aplicado no momento de um failover.</span><span class="sxs-lookup"><span data-stu-id="1f95e-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="1f95e-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f95e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f95e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f95e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="1f95e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1f95e-107">Members</span></span>

<span data-ttu-id="1f95e-108">A classe **Msvm \_ FailoverNetworkAdapterSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f95e-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1f95e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f95e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f95e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f95e-110">Properties</span></span>

<span data-ttu-id="1f95e-111">A classe **Msvm \_ FailoverNetworkAdapterSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f95e-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f95e-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1f95e-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1f95e-115">A short description of the object.</span></span> <span data-ttu-id="1f95e-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f95e-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-117">**Defaultgateways**</span><span class="sxs-lookup"><span data-stu-id="1f95e-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-120">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="1f95e-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-121">Uma matriz de cadeias de caracteres que especificam os gateways IP padrão configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1f95e-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="1f95e-122">O número máximo de gateways IP padrão que podem ser configurados em um único adaptador de rede é cinco.</span><span class="sxs-lookup"><span data-stu-id="1f95e-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f95e-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-126">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1f95e-126">A description of the object.</span></span> <span data-ttu-id="1f95e-127">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f95e-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="1f95e-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f95e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-131">Especifica se o DHCP está habilitado na interface IPv4 do adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1f95e-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="1f95e-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-135">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="1f95e-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-136">Uma matriz de cadeias de caracteres que especificam os servidores DNS configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1f95e-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1f95e-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-140">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1f95e-140">A display name for the object.</span></span> <span data-ttu-id="1f95e-141">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f95e-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f95e-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-145">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1f95e-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-146">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1f95e-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1f95e-147">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f95e-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="1f95e-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-149">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-151">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="1f95e-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-152">Uma matriz de cadeias de caracteres que especificam os endereços IP configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1f95e-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1f95e-153">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="1f95e-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f95e-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-156">Identifica os protocolos de Internet aos quais as configurações especificadas por essa instância se aplicam.</span><span class="sxs-lookup"><span data-stu-id="1f95e-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="1f95e-157">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f95e-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f95e-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f95e-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1f95e-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1f95e-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="1f95e-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="1f95e-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="1f95e-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="1f95e-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="1f95e-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="1f95e-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="1f95e-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="1f95e-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f95e-164">**Sub-redes**</span><span class="sxs-lookup"><span data-stu-id="1f95e-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f95e-165">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f95e-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f95e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f95e-167">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="1f95e-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="1f95e-168">Uma matriz de cadeias de caracteres que especificam as sub-redes configuradas no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="1f95e-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="1f95e-169">Cada elemento nessa matriz se aplica ao elemento correspondente na matriz **ipaddresss** .</span><span class="sxs-lookup"><span data-stu-id="1f95e-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f95e-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f95e-170">Requirements</span></span>



| <span data-ttu-id="1f95e-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f95e-171">Requirement</span></span> | <span data-ttu-id="1f95e-172">Valor</span><span class="sxs-lookup"><span data-stu-id="1f95e-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f95e-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f95e-173">Minimum supported client</span></span><br/> | <span data-ttu-id="1f95e-174">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f95e-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f95e-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f95e-175">Minimum supported server</span></span><br/> | <span data-ttu-id="1f95e-176">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f95e-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f95e-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f95e-177">Namespace</span></span><br/>                | <span data-ttu-id="1f95e-178">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1f95e-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f95e-179">MOF</span><span class="sxs-lookup"><span data-stu-id="1f95e-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f95e-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f95e-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f95e-181">DLL</span><span class="sxs-lookup"><span data-stu-id="1f95e-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f95e-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f95e-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

