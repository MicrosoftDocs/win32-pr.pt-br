---
description: Representa a configuração de um adaptador de rede dentro do sistema operacional convidado.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Classe Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090671"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="c14b2-103">\_Classe Msvm GuestNetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="c14b2-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c14b2-104">Representa a configuração de um adaptador de rede dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="c14b2-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c14b2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14b2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c14b2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="c14b2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c14b2-107">Members</span></span>

<span data-ttu-id="c14b2-108">A classe **Msvm \_ GuestNetworkAdapterConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c14b2-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="c14b2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c14b2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c14b2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c14b2-110">Properties</span></span>

<span data-ttu-id="c14b2-111">A classe **Msvm \_ GuestNetworkAdapterConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c14b2-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c14b2-112">**Defaultgateways**</span><span class="sxs-lookup"><span data-stu-id="c14b2-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c14b2-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-115">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c14b2-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-116">Uma matriz de cadeias de caracteres que contém os gateways IP padrão configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="c14b2-117">O número máximo de gateways IP padrão que podem ser configurados em um único adaptador de rede é cinco.</span><span class="sxs-lookup"><span data-stu-id="c14b2-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="c14b2-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="c14b2-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c14b2-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-121">Especifica se o DHCP está habilitado no adaptador de rede dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c14b2-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="c14b2-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-123">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c14b2-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-125">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c14b2-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-126">Uma matriz de cadeias de caracteres que contêm os servidores DNS configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c14b2-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c14b2-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c14b2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c14b2-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-131">O identificador exclusivo deste objeto.</span><span class="sxs-lookup"><span data-stu-id="c14b2-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="c14b2-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="c14b2-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c14b2-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-135">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c14b2-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-136">Uma matriz de cadeias de caracteres que contêm os endereços IP configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c14b2-137">**IPAddressOrigins**</span><span class="sxs-lookup"><span data-stu-id="c14b2-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-138">Tipo de dados: a matriz **UINT16**</span><span class="sxs-lookup"><span data-stu-id="c14b2-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-140">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c14b2-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-141">A origem dos endereços IP configurados no adaptador de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c14b2-142">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c14b2-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c14b2-143">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c14b2-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="c14b2-144">**Estático** (2)</span><span class="sxs-lookup"><span data-stu-id="c14b2-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c14b2-145">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="c14b2-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c14b2-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-148">Identifica os protocolos IP aos quais as configurações especificadas por essa instância se aplicam.</span><span class="sxs-lookup"><span data-stu-id="c14b2-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c14b2-149">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c14b2-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c14b2-150">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c14b2-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="c14b2-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="c14b2-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="c14b2-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="c14b2-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="c14b2-153">**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="c14b2-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c14b2-154">**Sub-redes**</span><span class="sxs-lookup"><span data-stu-id="c14b2-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c14b2-155">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c14b2-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c14b2-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c14b2-157">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c14b2-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c14b2-158">Uma matriz de cadeias de caracteres que contêm as sub-redes configuradas no adaptador de rede dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="c14b2-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="c14b2-159">Cada elemento nessa matriz se aplica ao elemento correspondente na matriz **ipaddresss** .</span><span class="sxs-lookup"><span data-stu-id="c14b2-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c14b2-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c14b2-160">Requirements</span></span>



| <span data-ttu-id="c14b2-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c14b2-161">Requirement</span></span> | <span data-ttu-id="c14b2-162">Valor</span><span class="sxs-lookup"><span data-stu-id="c14b2-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14b2-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c14b2-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c14b2-164">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c14b2-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c14b2-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c14b2-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c14b2-166">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c14b2-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c14b2-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="c14b2-167">Namespace</span></span><br/>                | <span data-ttu-id="c14b2-168">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c14b2-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c14b2-169">MOF</span><span class="sxs-lookup"><span data-stu-id="c14b2-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c14b2-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c14b2-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c14b2-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c14b2-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c14b2-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c14b2-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

