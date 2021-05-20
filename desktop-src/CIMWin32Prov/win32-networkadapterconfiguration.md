---
description: Representa os atributos e comportamentos de um adaptador de rede. Essa classe inclui propriedades e métodos adicionais que suportam o gerenciamento do protocolo TCP/IP que são independentes do adaptador de rede.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153569"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="0f353-104">Classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f353-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0f353-105">A classe [WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterConfiguration do Win32** representa os atributos e comportamentos de um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="0f353-106">Essa classe inclui propriedades e métodos adicionais que suportam o gerenciamento do protocolo TCP/IP que são independentes do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="0f353-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0f353-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0f353-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0f353-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f353-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f353-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="0f353-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0f353-110">Members</span></span>

<span data-ttu-id="0f353-111">A **classe \_ NetworkAdapterConfiguration do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0f353-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="0f353-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f353-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f353-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0f353-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f353-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f353-114">Methods</span></span>

<span data-ttu-id="0f353-115">A **classe \_ NetworkAdapterConfiguration do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0f353-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="0f353-116">Método</span><span class="sxs-lookup"><span data-stu-id="0f353-116">Method</span></span>                                                                                                                       | <span data-ttu-id="0f353-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f353-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f353-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="0f353-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="0f353-119">Desabilita o IPsec neste adaptador de rede habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="0f353-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="0f353-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="0f353-121">Habilita o protocolo DHCP para serviço com esse adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="0f353-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="0f353-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="0f353-123">Habilita o DNS (Sistema de Nomes de Domínio) para serviço neste adaptador de rede vinculado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="0f353-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="0f353-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="0f353-125">Habilita o IPsec globalmente em todos os adaptadores de rede vinculados a IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="0f353-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="0f353-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="0f353-127">Habilita o IPsec nesse adaptador de rede habilitado para TCP/IP específico.</span><span class="sxs-lookup"><span data-stu-id="0f353-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="0f353-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="0f353-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="0f353-129">Habilita o endereçamento TCP/IP estático para o adaptador de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="0f353-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="0f353-130">**EnableWINS ativa**</span><span class="sxs-lookup"><span data-stu-id="0f353-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="0f353-131">Habilita configurações do WINS específicas para TCP/IP, mas independente do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="0f353-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="0f353-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="0f353-133">Libera o endereço IP associado a um adaptador de rede habilitado para DHCP específico.</span><span class="sxs-lookup"><span data-stu-id="0f353-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="0f353-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="0f353-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="0f353-135">Libera os endereços IP associados a todos os adaptadores de rede habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="0f353-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="0f353-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="0f353-137">Renova o endereço IP em adaptadores de rede habilitados para DHCP específicos.</span><span class="sxs-lookup"><span data-stu-id="0f353-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="0f353-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="0f353-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="0f353-139">Renova os endereços IP em todos os adaptadores de rede habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="0f353-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="0f353-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="0f353-141">Define a transmissão de consultas ARP pelo TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0f353-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="0f353-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="0f353-143">Permite que os pacotes Ethernet usem a codificação de ajuste 802,3.</span><span class="sxs-lookup"><span data-stu-id="0f353-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="0f353-144">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="0f353-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="0f353-145">Define o caminho para os arquivos de banco de dados da Internet padrão (HOSTs, LMHOSTs, redes e protocolos).</span><span class="sxs-lookup"><span data-stu-id="0f353-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="0f353-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="0f353-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="0f353-147">Habilita a detecção de gateway inativo.</span><span class="sxs-lookup"><span data-stu-id="0f353-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="0f353-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="0f353-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="0f353-149">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0f353-149">Obsolete.</span></span> <span data-ttu-id="0f353-150">Esse método define o valor do tipo de serviço (TOS) padrão no cabeçalho dos pacotes de IP de saída.</span><span class="sxs-lookup"><span data-stu-id="0f353-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="0f353-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="0f353-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="0f353-152">Define o valor TTL (Vida Vida) padrão no header de pacotes IP de saída.</span><span class="sxs-lookup"><span data-stu-id="0f353-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="0f353-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="0f353-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="0f353-154">Define o domínio DNS.</span><span class="sxs-lookup"><span data-stu-id="0f353-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="0f353-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="0f353-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="0f353-156">Define a ordem de pesquisa do servidor como uma matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="0f353-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="0f353-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="0f353-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="0f353-158">Define a ordem de pesquisa de sufixo como uma matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="0f353-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="0f353-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="0f353-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="0f353-160">Indica o registro DNS dinâmico de endereços IP para esse adaptador associado a IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="0f353-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="0f353-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="0f353-162">Especifica quanto IP de memória aloca para armazenar dados de pacote na fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="0f353-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="0f353-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="0f353-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="0f353-164">Especifica uma lista de gateways para pacotes de roteamento destinados a uma sub-rede diferente da que esse adaptador está conectado.</span><span class="sxs-lookup"><span data-stu-id="0f353-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="0f353-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="0f353-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="0f353-166">Define a extensão à qual o sistema dá suporte à multicast de IP e participa do Protocolo de Gerenciamento de Grupo da Internet.</span><span class="sxs-lookup"><span data-stu-id="0f353-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="0f353-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="0f353-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="0f353-168">Define a métrica de roteamento associada a esse adaptador associado a IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="0f353-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="0f353-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="0f353-170">Define o uso de difusão de IP zero.</span><span class="sxs-lookup"><span data-stu-id="0f353-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0f353-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="0f353-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="0f353-172">Define os pares de número/quadro de rede IPX (troca de pacotes Interrede) para esse adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="0f353-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="0f353-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="0f353-174">Define o número de rede virtual de intercâmbio de pacotes entre redes (IPX) no sistema de computador de destino.</span><span class="sxs-lookup"><span data-stu-id="0f353-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="0f353-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="0f353-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="0f353-176">Define o intervalo que separa as retransmissões Keep Alive até que uma resposta seja recebida.</span><span class="sxs-lookup"><span data-stu-id="0f353-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="0f353-177">**Setkeepalivetime**</span><span class="sxs-lookup"><span data-stu-id="0f353-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="0f353-178">Define a frequência com que o TCP tenta verificar se uma conexão ociosa ainda está disponível enviando um pacote keep alive.</span><span class="sxs-lookup"><span data-stu-id="0f353-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="0f353-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="0f353-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="0f353-180">Define a MTU (unidade máxima de transmissão) padrão para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="0f353-181">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0f353-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="0f353-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="0f353-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="0f353-183">Define o número de cabeçalhos de pacotes IP alocados para a fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="0f353-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="0f353-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="0f353-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="0f353-185">Habilita a detecção de roteadores buraco negro.</span><span class="sxs-lookup"><span data-stu-id="0f353-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="0f353-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="0f353-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="0f353-187">Habilita a descoberta de MTU (unidade máxima de transmissão).</span><span class="sxs-lookup"><span data-stu-id="0f353-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0f353-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="0f353-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="0f353-189">Define a operação padrão de NetBIOS sobre TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0f353-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="0f353-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="0f353-191">Define o número de tentativas que o TCP retransmitirá uma solicitação de conexão antes de abortar.</span><span class="sxs-lookup"><span data-stu-id="0f353-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="0f353-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="0f353-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="0f353-193">Define o número de vezes que o TCP retransmite um segmento de dados individual antes de anular a conexão.</span><span class="sxs-lookup"><span data-stu-id="0f353-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="0f353-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="0f353-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="0f353-195">Define o número máximo de conexões que o TCP pode ter aberto simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0f353-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="0f353-196">**SetTcpUseRFC1122EntPointer**</span><span class="sxs-lookup"><span data-stu-id="0f353-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="0f353-197">Especifica se o TCP usa a especificação RFC 1122 para dados urgentes ou o modo usado pelos sistemas derivados do BSD (Berkeley Software Design).</span><span class="sxs-lookup"><span data-stu-id="0f353-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="0f353-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="0f353-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="0f353-199">Define o tamanho máximo da Janela de Recebimento TCP oferecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0f353-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="0f353-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="0f353-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="0f353-201">Define os servidores WINS (Windows Internet Serviço de Nomenclatura) primários e secundários neste adaptador de rede vinculado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="0f353-202">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0f353-202">Properties</span></span>

<span data-ttu-id="0f353-203">A **classe \_ NetworkAdapterConfiguration do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0f353-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f353-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="0f353-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-205">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-207">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="0f353-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-208">Se **TRUE**, TCP/IP transmitirá consultas ARP (Protocolo de Resolução de Endereço) com o roteamento de origem habilitado em redes de Anel de Token.</span><span class="sxs-lookup"><span data-stu-id="0f353-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="0f353-209">Por padrão (FALSE), o ARP primeiro consulta sem roteamento de origem e, em seguida, faz uma nova busca com o roteamento de origem habilitado se nenhuma resposta for recebida.</span><span class="sxs-lookup"><span data-stu-id="0f353-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="0f353-210">O roteamento de origem permite o roteamento de pacotes de rede em diferentes tipos de redes.</span><span class="sxs-lookup"><span data-stu-id="0f353-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="0f353-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-212">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-214">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="0f353-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-215">Se **for verdadeiro**, os pacotes de Ethernet seguem a codificação de snap (protocolo de acesso Sub-Network) do IEEE 802,3.</span><span class="sxs-lookup"><span data-stu-id="0f353-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="0f353-216">Definir esse parâmetro como 1 força o TCP/IP a transmitir pacotes Ethernet usando a codificação de encaixe 802,3.</span><span class="sxs-lookup"><span data-stu-id="0f353-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="0f353-217">Por padrão (FALSE), a pilha transmite pacotes no formato de Ethernet DIX.</span><span class="sxs-lookup"><span data-stu-id="0f353-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-218">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0f353-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-221">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0f353-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0f353-222">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="0f353-222">Short textual description of the current object.</span></span>

<span data-ttu-id="0f353-223">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f353-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f353-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="0f353-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-227">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet os \\ \\ \\ \\ \\ \\ parâmetros tcpip \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="0f353-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-228">Caminho de arquivo do Windows válido para arquivos de banco de dados da Internet padrão (HOSTs, LMHOSTs, redes e protocolos).</span><span class="sxs-lookup"><span data-stu-id="0f353-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="0f353-229">O caminho do arquivo é usado pela interface do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="0f353-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0f353-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-233">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="0f353-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-234">Se **for true**, ocorrerá a detecção de gateway inativo.</span><span class="sxs-lookup"><span data-stu-id="0f353-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="0f353-235">Com esse recurso habilitado, o protocolo TCP solicita que o protocolo Internet (IP) mude para um gateway de backup se retransmitir um segmento várias vezes sem receber uma resposta.</span><span class="sxs-lookup"><span data-stu-id="0f353-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="0f353-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-237">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-239">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ parâmetros de serviços \| \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="0f353-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-240">Matriz de endereços IP de gateways padrão que o sistema de computador usa.</span><span class="sxs-lookup"><span data-stu-id="0f353-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="0f353-241">Exemplo: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="0f353-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="0f353-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-243">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0f353-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-245">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="0f353-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-246">Valor padrão tipo de serviço (TOS) definido no header de pacotes IP de saída.</span><span class="sxs-lookup"><span data-stu-id="0f353-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="0f353-247">A RFC (Solicitação de Comentários) 791 define os valores.</span><span class="sxs-lookup"><span data-stu-id="0f353-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="0f353-248">Padrão: 0 (zero), Intervalo válido: 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="0f353-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="0f353-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-250">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0f353-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-252">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="0f353-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-253">Valor TTL (Vida Vida Padrão) definido no header de pacotes IP de saída.</span><span class="sxs-lookup"><span data-stu-id="0f353-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="0f353-254">A TTL especifica o número de roteadores que um pacote IP pode passar para alcançar seu destino antes de ser descartado.</span><span class="sxs-lookup"><span data-stu-id="0f353-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="0f353-255">Cada roteador diminui por um a contagem de TTL de um pacote conforme ele passa e descarta os pacotes — se o TTL for 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="0f353-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="0f353-256">Padrão: 32, Intervalo válido: 1 a 255.</span><span class="sxs-lookup"><span data-stu-id="0f353-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-257">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0f353-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-260">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="0f353-260">Textual description of the current object.</span></span>

<span data-ttu-id="0f353-261">Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f353-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f353-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-263">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-265">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="0f353-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-266">Se **TRUE**, o servidor DHCP (dynamic host configuration protocol) atribuirá automaticamente um endereço IP ao sistema de computador ao estabelecer uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="0f353-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-268">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f353-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-270">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")</span><span class="sxs-lookup"><span data-stu-id="0f353-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-271">Data e hora de expiração de um endereço IP concedido que foi atribuído ao computador pelo servidor de protocolo DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="0f353-272">Exemplo: 20521201000230, 0</span><span class="sxs-lookup"><span data-stu-id="0f353-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="0f353-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="0f353-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-274">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f353-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-276">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")</span><span class="sxs-lookup"><span data-stu-id="0f353-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-277">Data e hora em que a concessão foi obtida para o endereço IP atribuído ao computador pelo servidor DHCP (protocolo de configuração dinâmica de hosts).</span><span class="sxs-lookup"><span data-stu-id="0f353-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="0f353-278">Exemplo: 19521201000230, 0</span><span class="sxs-lookup"><span data-stu-id="0f353-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="0f353-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="0f353-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-282">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")</span><span class="sxs-lookup"><span data-stu-id="0f353-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-283">Endereço IP do servidor de protocolo DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="0f353-284">Exemplo: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="0f353-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="0f353-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-288">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Domain")</span><span class="sxs-lookup"><span data-stu-id="0f353-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-289">Nome da organização seguido por um ponto e uma extensão que indica o tipo de organização, como "microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="0f353-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="0f353-290">O nome pode ser qualquer combinação das letras de a a Z, os numerais de 0 a 9 e o hífen (-), além do caractere de ponto (.) usado como separador.</span><span class="sxs-lookup"><span data-stu-id="0f353-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="0f353-291">Exemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="0f353-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="0f353-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-293">Tipo de dados: matriz **de cadeia de** caracteres</span><span class="sxs-lookup"><span data-stu-id="0f353-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-295">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| SearchList")</span><span class="sxs-lookup"><span data-stu-id="0f353-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-296">Matriz de sufixos de domínio DNS a serem anexados ao final dos nomes de host durante a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="0f353-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="0f353-297">Ao tentar resolver um FQDN (nome de domínio totalmente qualificado) de um nome somente host, o sistema primeiro anexará o nome de domínio local.</span><span class="sxs-lookup"><span data-stu-id="0f353-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="0f353-298">Se isso não for bem-sucedido, o sistema usará a lista de sufixos de domínio para criar FQDNs adicionais na ordem listada e consultar servidores DNS para cada um.</span><span class="sxs-lookup"><span data-stu-id="0f353-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="0f353-299">Exemplo: "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="0f353-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="0f353-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-301">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-303">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="0f353-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-304">Se **TRUE**, o DNS (Sistema de Nomes de Domínio) será habilitado para resolução de nomes pela resolução de Serviço de Nomenclatura Windows Internet (WINS).</span><span class="sxs-lookup"><span data-stu-id="0f353-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="0f353-305">Se o nome não puder ser resolvido usando DNS, a solicitação de nome será encaminhada para WINS para resolução.</span><span class="sxs-lookup"><span data-stu-id="0f353-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-306">**Dnshostname**</span><span class="sxs-lookup"><span data-stu-id="0f353-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-309">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname")</span><span class="sxs-lookup"><span data-stu-id="0f353-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-310">Nome do host usado para identificar o computador local para autenticação por alguns utilitários.</span><span class="sxs-lookup"><span data-stu-id="0f353-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="0f353-311">Outros utilitários baseados em TCP/IP podem usar esse valor para adquirir o nome do computador local.</span><span class="sxs-lookup"><span data-stu-id="0f353-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="0f353-312">Os nomes de host são armazenados em servidores DNS em uma tabela que mapeia nomes para endereços IP para uso pelo DNS.</span><span class="sxs-lookup"><span data-stu-id="0f353-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="0f353-313">O nome pode ser qualquer combinação das letras A a Z, dos numerais de 0 a 9 e do hífen (-), além do caractere de ponto (.) usado como separador.</span><span class="sxs-lookup"><span data-stu-id="0f353-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="0f353-314">Por padrão, esse valor é o nome do computador de rede da Microsoft, mas o administrador de rede pode atribuir outro nome de host sem afetar o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="0f353-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="0f353-315">Exemplo: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="0f353-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="0f353-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-317">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-319">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| nameserver")</span><span class="sxs-lookup"><span data-stu-id="0f353-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-320">Matriz de endereços IP do servidor a ser usada na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="0f353-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-322">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0f353-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-324">Se **for true**, os endereços IP para essa conexão serão registrados no DNS sob o nome de domínio dessa conexão, além de serem registrados sob o nome DNS completo do computador.</span><span class="sxs-lookup"><span data-stu-id="0f353-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="0f353-325">O nome de domínio dessa conexão é definido usando o método [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() ou atribuído pelo DSCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="0f353-326">O nome registrado é o nome do host do computador com o nome de domínio anexado.</span><span class="sxs-lookup"><span data-stu-id="0f353-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="0f353-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-328">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-330">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0f353-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-331">Memória alocada por IP para armazenar dados de pacote na fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="0f353-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="0f353-332">Quando esse espaço de buffer é preenchido, o roteador começa a descartar os pacotes aleatoriamente de sua fila.</span><span class="sxs-lookup"><span data-stu-id="0f353-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="0f353-333">Buffers de dados de fila de pacotes têm 256 bytes de comprimento, portanto, o valor desse parâmetro deve ser um múltiplo de 256.</span><span class="sxs-lookup"><span data-stu-id="0f353-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="0f353-334">Vários buffers são encadeados em pacotes maiores.</span><span class="sxs-lookup"><span data-stu-id="0f353-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="0f353-335">O cabeçalho IP de um pacote é armazenado separadamente.</span><span class="sxs-lookup"><span data-stu-id="0f353-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="0f353-336">Esse parâmetro será ignorado e nenhum buffer será alocado se o roteador IP não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="0f353-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="0f353-337">O tamanho do buffer pode variar da MTU de rede para um valor menor que 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0f353-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="0f353-338">Padrão: 74240 (1480 pacotes de 1480 byte, arredondados para um múltiplo de 256).</span><span class="sxs-lookup"><span data-stu-id="0f353-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="0f353-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-340">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-342">Se **TRUE**, os endereços IP dessa conexão serão registrados no DNS com o nome DNS completo do computador.</span><span class="sxs-lookup"><span data-stu-id="0f353-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="0f353-343">O nome DNS completo do computador é exibido na guia **Identificação de** Rede no aplicativo Sistema no Painel de Controle.</span><span class="sxs-lookup"><span data-stu-id="0f353-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="0f353-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-345">Tipo de dados: **matriz uint16**</span><span class="sxs-lookup"><span data-stu-id="0f353-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-347">Matriz de valores de métrica de custo inteiro (variando de 1 a 9999) a serem usados no cálculo das rotas mais rápidas, mais confiáveis ou menos intensivas em recursos.</span><span class="sxs-lookup"><span data-stu-id="0f353-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="0f353-348">Esse argumento tem uma correspondência um-para-um com a **propriedade DefaultIPGateway.**</span><span class="sxs-lookup"><span data-stu-id="0f353-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="0f353-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-350">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0f353-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-352">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="0f353-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-353">Até que ponto o sistema dá suporte a multicast de IP e participa do protocolo IGMP.</span><span class="sxs-lookup"><span data-stu-id="0f353-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="0f353-354">No nível 0 (zero), o sistema não oferece suporte a multicast.</span><span class="sxs-lookup"><span data-stu-id="0f353-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="0f353-355">No nível 1, o sistema só pode enviar pacotes de multicast IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="0f353-356">No nível 2, o sistema pode enviar pacotes de multicast IP e participar totalmente do IGMP para receber pacotes multicast.</span><span class="sxs-lookup"><span data-stu-id="0f353-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="0f353-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Sem Multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="0f353-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="0f353-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multicast de IP** (1)</span><span class="sxs-lookup"><span data-stu-id="0f353-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="0f353-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Multicast IGMP & IP** (2)</span><span class="sxs-lookup"><span data-stu-id="0f353-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f353-360">IP e IGMP multicast (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f353-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f353-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="0f353-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-362">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-364">Qualifiers: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ classe de controle \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="0f353-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-365">Número de índice da configuração do adaptador de rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="0f353-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="0f353-366">O número de índice é usado quando há mais de uma configuração disponível.</span><span class="sxs-lookup"><span data-stu-id="0f353-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="0f353-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-368">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-370">Valor de índice que identifica exclusivamente uma interface de rede local.</span><span class="sxs-lookup"><span data-stu-id="0f353-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="0f353-371">O valor nessa propriedade é o mesmo que o valor na propriedade **InterfaceIndex** na instância do [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa a interface de rede na tabela de rotas.</span><span class="sxs-lookup"><span data-stu-id="0f353-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-372">**EndereçoIP**</span><span class="sxs-lookup"><span data-stu-id="0f353-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-373">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-375">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ parâmetros de serviços \| \\ \\ \| " tcpip IPAddress ")</span><span class="sxs-lookup"><span data-stu-id="0f353-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-376">Matriz de todos os endereços IP associados ao adaptador de rede atual.</span><span class="sxs-lookup"><span data-stu-id="0f353-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="0f353-377">Essa propriedade pode conter endereços IPv6 ou endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="0f353-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="0f353-378">Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0f353-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="0f353-379">Endereço IPv6 de exemplo: "2010:836B: 4179:: 836B: 4179"</span><span class="sxs-lookup"><span data-stu-id="0f353-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="0f353-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-381">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-383">O custo de usar as rotas configuradas para o adaptador de IP ligado e é o valor ponderado para essas rotas na tabela de roteamento de IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="0f353-384">Se houver várias rotas para um destino na tabela de roteamento de IP, a rota com a métrica mais baixa será usada.</span><span class="sxs-lookup"><span data-stu-id="0f353-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="0f353-385">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="0f353-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-387">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0f353-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-389">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip")</span><span class="sxs-lookup"><span data-stu-id="0f353-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-390">Se **TRUE**, o TCP/IP será vinculado e habilitado neste adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-392">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-394">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="0f353-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-395">Se **TRUE**, a segurança da porta IP será habilitada globalmente em todos os adaptadores de rede associados ao IP e os valores de segurança associados a adaptadores de rede individuais entrarão em vigor.</span><span class="sxs-lookup"><span data-stu-id="0f353-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="0f353-396">Essa propriedade é usada em conjunto com **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**.</span><span class="sxs-lookup"><span data-stu-id="0f353-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="0f353-397">Se **FALSE**, a segurança do filtro IP será desabilitada em todos os adaptadores de rede e permitirá que todo o tráfego de porta e protocolo flua sem filtro.</span><span class="sxs-lookup"><span data-stu-id="0f353-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-399">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-401">Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="0f353-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-402">Se **TRUE,** a segurança da porta IP será habilitada globalmente em todos os adaptadores de rede vinculados a IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="0f353-403">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="0f353-403">This property is obsolete.</span></span> <span data-ttu-id="0f353-404">No lugar dessa propriedade, você deve usar **IPFilterSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="0f353-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="0f353-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-406">Tipo de dados: matriz **de cadeia de** caracteres</span><span class="sxs-lookup"><span data-stu-id="0f353-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-408">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Parâmetros Tcpip \\ \\ \| RawIPAllowedProtocols")</span><span class="sxs-lookup"><span data-stu-id="0f353-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-409">Matriz dos protocolos permitidos para executar o IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="0f353-410">A lista de protocolos é definida usando o [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f353-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="0f353-411">A lista estará vazia ou conterá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0f353-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="0f353-412">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todos os protocolos.</span><span class="sxs-lookup"><span data-stu-id="0f353-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="0f353-413">Uma cadeia de caracteres vazia indica que nenhum protocolo tem permissão para ser executado quando **IPFilterSecurityEnabled** é **true**.</span><span class="sxs-lookup"><span data-stu-id="0f353-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="0f353-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-415">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-417">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TCPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="0f353-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-418">Matriz das portas às quais será concedida permissão de acesso para TCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="0f353-419">A lista de protocolos é definida usando o método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0f353-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="0f353-420">A lista estará vazia ou conterá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0f353-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="0f353-421">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas.</span><span class="sxs-lookup"><span data-stu-id="0f353-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="0f353-422">Uma cadeia de caracteres vazia indica que nenhuma porta recebe permissão de acesso quando **IPFilterSecurityEnabled** é **true**.</span><span class="sxs-lookup"><span data-stu-id="0f353-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="0f353-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-424">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-426">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| UDPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="0f353-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-427">Matriz das portas às quais a permissão de acesso UDP (User Datagram Protocol) será concedida.</span><span class="sxs-lookup"><span data-stu-id="0f353-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="0f353-428">A lista de protocolos é definida usando o método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0f353-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="0f353-429">A lista estará vazia ou conterá valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="0f353-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="0f353-430">Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas.</span><span class="sxs-lookup"><span data-stu-id="0f353-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="0f353-431">Uma cadeia de caracteres vazia indica que nenhuma porta recebe permissão de acesso quando **IPFilterSecurityEnabled** é **true**.</span><span class="sxs-lookup"><span data-stu-id="0f353-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="0f353-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-433">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-435">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ \| Parameters de parâmetros de serviços \| ")</span><span class="sxs-lookup"><span data-stu-id="0f353-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-436">Matriz de todas as máscaras de sub-rede associadas ao adaptador de rede atual.</span><span class="sxs-lookup"><span data-stu-id="0f353-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="0f353-437">Exemplo: "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="0f353-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="0f353-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-439">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-441">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="0f353-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-442">Se **TRUE**, serão usados zeros-difusões de IP (0.0.0.0) e o sistema usará difusões de ones (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="0f353-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="0f353-443">Os sistemas de computador geralmente usam difusões de um, mas aqueles derivados de implementações BSD usam zeros-broadcasts.</span><span class="sxs-lookup"><span data-stu-id="0f353-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="0f353-444">Sistemas que não usam as mesmas difusões não interoperarão na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="0f353-445">O padrão é **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="0f353-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="0f353-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-447">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-449">Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Versão 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")</span><span class="sxs-lookup"><span data-stu-id="0f353-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-450">Não há mais suporte para a tecnologia IPX (Internetwork Packet Exchange) e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-452">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-454">Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0f353-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-455">Não há mais suporte para a tecnologia IPX (Internetwork Packet Exchange) e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="0f353-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-457">Tipo de dados: **matriz uint32**</span><span class="sxs-lookup"><span data-stu-id="0f353-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-459">Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType")</span><span class="sxs-lookup"><span data-stu-id="0f353-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-460">Não há mais suporte para a tecnologia IPX (Internetwork Packet Exchange) e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="0f353-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="0f353-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="0f353-462">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="0f353-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="0f353-463">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="0f353-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="0f353-464">**Ajuste de Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="0f353-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="0f353-465">**Automático** (255)</span><span class="sxs-lookup"><span data-stu-id="0f353-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f353-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="0f353-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-467">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-469">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NwlnkIpx \\ \\ Parameters \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="0f353-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-470">A tecnologia de intercâmbio de pacotes de rede (IPX) não é mais suportada e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="0f353-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="0f353-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="0f353-472">**Token ring** (2)</span><span class="sxs-lookup"><span data-stu-id="0f353-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="0f353-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="0f353-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="0f353-474">**ARCnet** (8)</span><span class="sxs-lookup"><span data-stu-id="0f353-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f353-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="0f353-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-476">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f353-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-478">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NwlnkIpx \\ \\ Parameters \| NetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="0f353-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-479">A tecnologia de intercâmbio de pacotes de rede (IPX) não é mais suportada e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="0f353-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-483">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NwlnkIpx \\ \\ Parameters \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="0f353-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-484">Não há mais suporte para a tecnologia IPX (Internetwork Packet Exchange) e essa propriedade não contém dados úteis.</span><span class="sxs-lookup"><span data-stu-id="0f353-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="0f353-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-486">Tipo de dados: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0f353-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-488">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="0f353-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-489">Intervalo que separa as Retransmissões Keep Alive até que uma resposta seja recebida.</span><span class="sxs-lookup"><span data-stu-id="0f353-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="0f353-490">Depois que uma resposta é recebida, o atraso até a próxima Transmissão Keep Alive é controlado novamente pelo **valor de KeepAliveTime**.</span><span class="sxs-lookup"><span data-stu-id="0f353-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="0f353-491">A conexão será anulada depois que o número de retransmissões especificado por **TcpMaxDataRetransmissions** ficar sem resposta.</span><span class="sxs-lookup"><span data-stu-id="0f353-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="0f353-492">Padrão: 1000, Intervalo válido: 1 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0f353-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="0f353-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-494">Tipo de dados: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0f353-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-496">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="0f353-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-497">A **propriedade KeepAliveTime** indica com que frequência o TCP tenta verificar se uma conexão ociosa ainda está intacta enviando um pacote Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="0f353-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="0f353-498">Um sistema remoto acessível reconhecerá a keep alive transmissão.</span><span class="sxs-lookup"><span data-stu-id="0f353-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="0f353-499">Os pacotes Keep Alive não são enviados por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f353-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="0f353-500">Esse recurso pode ser habilitado em uma conexão por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f353-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="0f353-501">Padrão: 7.200.000 (duas horas).</span><span class="sxs-lookup"><span data-stu-id="0f353-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="0f353-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="0f353-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-503">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-505">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de entrada e saída do dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="0f353-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-506">Endereço MAC (Controle de Acesso à Mídia) do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="0f353-507">Um endereço MAC é atribuído pelo fabricante para identificar exclusivamente o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="0f353-508">Exemplo: "00:80: C7:8F: 6C: 96"</span><span class="sxs-lookup"><span data-stu-id="0f353-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="0f353-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-510">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-511">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-512">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0f353-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-513">Substitui a unidade máxima de transmissão (MTU) padrão para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="0f353-514">A MTU é o tamanho máximo do pacote (incluindo o cabeçalho de transporte) que o transporte transmitirá pela rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="0f353-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="0f353-515">O datagrama IP pode abranger vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="0f353-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="0f353-516">O intervalo desse valor abrange o tamanho mínimo do pacote (68) para a MTU com suporte da rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="0f353-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="0f353-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-518">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-520">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| NumForwardPackets")</span><span class="sxs-lookup"><span data-stu-id="0f353-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-521">Número de cabeçalhos de pacote IP alocados para a fila de pacotes do roteador.</span><span class="sxs-lookup"><span data-stu-id="0f353-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="0f353-522">Quando todos os cabeçalhos estiverem em uso, o roteador começará a descartar os pacotes da fila aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="0f353-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="0f353-523">Esse valor deve ser pelo menos tão grande quanto o valor de **ForwardBufferMemory** dividido pelo tamanho máximo de dados IP das redes conectadas ao roteador.</span><span class="sxs-lookup"><span data-stu-id="0f353-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="0f353-524">Não deve ser maior do que o valor de **ForwardBufferMemory** dividido por 256, pois pelo menos 256 bytes de memória de buffer de encaminhamento são usados para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="0f353-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="0f353-525">O número ideal de pacotes de encaminhamento para um determinado tamanho de **ForwardBufferMemory** depende do tipo de tráfego na rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="0f353-526">Ele estará em algum lugar entre esses dois valores.</span><span class="sxs-lookup"><span data-stu-id="0f353-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="0f353-527">Se o roteador não estiver habilitado, esse parâmetro será ignorado e nenhum cabeçalho será alocado.</span><span class="sxs-lookup"><span data-stu-id="0f353-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="0f353-528">Padrão: 50, intervalo válido: 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="0f353-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-530">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-531">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-532">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="0f353-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-533">Se **TRUE**, a detecção de roteadores de orifício preto ocorrerá enquanto o TCP descobre o caminho da Unidade de Transmissão Máxima.</span><span class="sxs-lookup"><span data-stu-id="0f353-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="0f353-534">Um roteador de orifício preto não retorna mensagens inacessível de destino ICMP quando precisa fragmentar um datagrama IP com o conjunto de bits Não Fragmentar.</span><span class="sxs-lookup"><span data-stu-id="0f353-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="0f353-535">O TCP depende do recebimento dessas mensagens para executar a Descoberta de MTU de Caminho.</span><span class="sxs-lookup"><span data-stu-id="0f353-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="0f353-536">Com esse recurso habilitado, o TCP tentará enviar segmentos sem o conjunto de bits Não Fragmentar se várias retransmissões de um segmento não são conhecidas.</span><span class="sxs-lookup"><span data-stu-id="0f353-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="0f353-537">Se o segmento for confirmado como resultado, o MSS será reduzido e o bit Não Fragmentar será definido em pacotes futuros na conexão.</span><span class="sxs-lookup"><span data-stu-id="0f353-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="0f353-538">A habilitação da detecção de orifícios pretos aumenta o número máximo de retransmissões executadas para um determinado segmento.</span><span class="sxs-lookup"><span data-stu-id="0f353-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="0f353-539">O valor padrão dessa propriedade é **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="0f353-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-540">**PMTUDiscoveryEnabled**</span><span class="sxs-lookup"><span data-stu-id="0f353-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-541">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-543">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="0f353-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-544">Se **TRUE**, o caminho MTU (Unidade máxima de transmissão) será descoberto no caminho para um host remoto.</span><span class="sxs-lookup"><span data-stu-id="0f353-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="0f353-545">Ao descobrir o caminho da MTU e limitar segmentos TCP a esse tamanho, o TCP pode eliminar a fragmentação em roteadores ao longo do caminho que conectam redes com diferentes MTUs.</span><span class="sxs-lookup"><span data-stu-id="0f353-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="0f353-546">A fragmentação afeta negativamente a taxa de transferência TCP e o congestionamento de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="0f353-547">Definir esse parâmetro como **FALSE** faz com que uma MTU de 576 bytes seja usada para todas as conexões que não são para máquinas na sub-rede local.</span><span class="sxs-lookup"><span data-stu-id="0f353-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="0f353-548">O padrão é **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="0f353-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-549">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="0f353-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-550">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-551">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-552">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="0f353-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-553">Nome do serviço do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-553">Service name of the network adapter.</span></span> <span data-ttu-id="0f353-554">Esse nome é geralmente mais curto do que o nome completo do produto.</span><span class="sxs-lookup"><span data-stu-id="0f353-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="0f353-555">Exemplo: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="0f353-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="0f353-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0f353-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-557">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-558">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-559">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0f353-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0f353-560">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0f353-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="0f353-561">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f353-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f353-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="0f353-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-563">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-564">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f353-565">Bitmap das configurações possíveis relacionadas ao NetBIOS sobre TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f353-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="0f353-566">Os valores são identificados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f353-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="0f353-567">**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="0f353-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="0f353-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="0f353-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="0f353-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="0f353-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f353-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="0f353-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-571">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f353-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-573">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="0f353-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-574">Número de vezes que o TCP tenta retransmitir uma solicitação de conexão antes de encerrar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0f353-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="0f353-575">O tempo de retransmissão inicial é de 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="0f353-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="0f353-576">O tempo de retransmissão dobra para cada tentativa.</span><span class="sxs-lookup"><span data-stu-id="0f353-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="0f353-577">Padrão: 3, Intervalo Válido: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0f353-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="0f353-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-579">Tipo de dados: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0f353-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-580">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-581">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Tcpip Parameters TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="0f353-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-582">Número de vezes que o TCP retransmite um segmento de dados individual (segmento não conectado) antes de encerrar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0f353-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="0f353-583">O tempo de retransmissão dobra com cada retransmissão sucessiva em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="0f353-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="0f353-584">Padrão: 5, Intervalo válido: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0f353-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-585">**Tcpnumconnections**</span><span class="sxs-lookup"><span data-stu-id="0f353-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-586">Tipo de dados: **uint32**</span><span class="sxs-lookup"><span data-stu-id="0f353-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-587">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-588">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Tcpip Parameters TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="0f353-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-589">Número máximo de conexões que o TCP pode ter abertas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0f353-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="0f353-590">Padrão: 0xFFFFFE, Intervalo Válido: 0 – 0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="0f353-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-591">**TcpUseRFC1122EntPointer**</span><span class="sxs-lookup"><span data-stu-id="0f353-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-592">Tipo de dados: **booliana**</span><span class="sxs-lookup"><span data-stu-id="0f353-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-593">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-594">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ Tcpip Parameters Tcpip Parameters \| TcpUseRFC1122EntPointer")</span><span class="sxs-lookup"><span data-stu-id="0f353-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-595">Se **TRUE**, o TCP usará a especificação RFC 1122 para dados urgentes.</span><span class="sxs-lookup"><span data-stu-id="0f353-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="0f353-596">Se **FALSE** (padrão), o TCP usará o modo usado pelos sistemas derivados do BSD (Design de Software Berkeley).</span><span class="sxs-lookup"><span data-stu-id="0f353-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="0f353-597">Os dois mecanismos interpretam o ponteiro urgente de forma diferente e não são interoperáveis.</span><span class="sxs-lookup"><span data-stu-id="0f353-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="0f353-598">O valor padrão é **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0f353-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="0f353-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-600">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f353-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-601">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-602">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="0f353-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-603">Tamanho máximo da janela de recepção TCP oferecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0f353-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="0f353-604">A janela de recepção especifica o número de bytes que um remetente pode transmitir sem receber uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="0f353-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="0f353-605">Em geral, as janelas de recebimento maiores melhorarão o desempenho em redes de alto atraso e alta largura de banda.</span><span class="sxs-lookup"><span data-stu-id="0f353-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="0f353-606">Para a eficiência, a janela de recebimento deve ser um múltiplo par do MSS (tamanho máximo de segmento) do TCP.</span><span class="sxs-lookup"><span data-stu-id="0f353-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="0f353-607">Padrão: quatro vezes o tamanho máximo dos dados TCP ou um múltiplo par de tamanho de dados TCP arredondado para o múltiplo mais próximo de 8192.</span><span class="sxs-lookup"><span data-stu-id="0f353-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="0f353-608">As redes Ethernet padrão são 8760.</span><span class="sxs-lookup"><span data-stu-id="0f353-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="0f353-609">Intervalo válido: 0-65535.</span><span class="sxs-lookup"><span data-stu-id="0f353-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="0f353-610">Windows Vista: essa propriedade acessa a `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrada do registro, que não é usada na implementação atual do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0f353-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="0f353-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="0f353-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-612">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0f353-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-613">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-614">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableLMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="0f353-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-615">Se **for true**, os arquivos de pesquisa local serão usados.</span><span class="sxs-lookup"><span data-stu-id="0f353-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="0f353-616">Arquivos de pesquisa conterão um mapa de endereços IP para nomes de host.</span><span class="sxs-lookup"><span data-stu-id="0f353-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="0f353-617">Se existirem no sistema local, eles serão encontrados em% SystemRoot% \\ System32 \\ drivers \\ etc.</span><span class="sxs-lookup"><span data-stu-id="0f353-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="0f353-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-619">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-620">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-621">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| funções de informações do sistema \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers, \\ \\ etc. \\ \\ Lmhosts")</span><span class="sxs-lookup"><span data-stu-id="0f353-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-622">Caminho para um arquivo de pesquisa WINS no sistema local.</span><span class="sxs-lookup"><span data-stu-id="0f353-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="0f353-623">Esse arquivo conterá um mapa de endereços IP para nomes de host.</span><span class="sxs-lookup"><span data-stu-id="0f353-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="0f353-624">Se o arquivo especificado nessa propriedade for encontrado, ele será copiado para a pasta %SystemRoot% \\ system32 \\ drivers \\ etc. do sistema local.</span><span class="sxs-lookup"><span data-stu-id="0f353-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="0f353-625">Válido somente se a **propriedade WINSEnableLMHostsLookup** for **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="0f353-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="0f353-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-627">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-628">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-629">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de entrada e saída do dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="0f353-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-630">Endereço IP do servidor WINS primário.</span><span class="sxs-lookup"><span data-stu-id="0f353-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="0f353-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-632">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-633">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-634">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ScopeID")</span><span class="sxs-lookup"><span data-stu-id="0f353-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-635">Valor anexado ao final do nome NetBIOS que isola um grupo de sistemas de computador que se comunicam entre si.</span><span class="sxs-lookup"><span data-stu-id="0f353-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="0f353-636">Ele é usado para todas as transações NetBIOS em comunicações TCP/IP desse sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="0f353-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="0f353-637">Computadores configurados com identificadores de escopo idênticos podem se comunicar com este computador.</span><span class="sxs-lookup"><span data-stu-id="0f353-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="0f353-638">Clientes TCP/IP com identificadores de escopo diferentes desconsideram pacotes de computadores com esse identificador de escopo.</span><span class="sxs-lookup"><span data-stu-id="0f353-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="0f353-639">Válido somente quando o [**método EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) é executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f353-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="0f353-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="0f353-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f353-641">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0f353-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f353-642">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f353-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f353-643">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de entrada e saída do dispositivo Win32API \| \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="0f353-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="0f353-644">Endereço IP do servidor WINS secundário.</span><span class="sxs-lookup"><span data-stu-id="0f353-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f353-645">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f353-645">Remarks</span></span>

<span data-ttu-id="0f353-646">A **classe \_ NetworkAdapterConfiguration do Win32** é derivada da [**configuração cim \_**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0f353-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0f353-647">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f353-647">Examples</span></span>

<span data-ttu-id="0f353-648">O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ NetworkAdapterConfiguration** para recuperar informações de configuração de rede de vários computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="0f353-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="0f353-649">As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo **Win32 \_ NetworkAdapterConfiguration**, para exibir informações sobre um sistema local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0f353-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="0f353-650">O código do PowerShell a seguir recupera as definições de configuração para o adaptador Microsoft ISTAP.</span><span class="sxs-lookup"><span data-stu-id="0f353-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="0f353-651">O exemplo C a seguir \# recupera a descrição e o número de índice de todas as instâncias de configuração do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="0f353-652">Observe que esse \# exemplo de C usa o namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , que geralmente é dimensionado de forma mais eficiente do que as classes WMI de namespace [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="0f353-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="0f353-653">O exemplo C a seguir \# recupera a descrição e o número de índice de todas as instâncias de configuração do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="0f353-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="0f353-654">Observe que este \# exemplo de C usa o namespace [System. Management](/dotnet/api/system.management) original, que foi substituído por [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f353-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="0f353-655">O exemplo a seguir recupera informações da classe **Win32 \_ NetworkAdapterConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="0f353-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="0f353-656">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f353-656">Requirements</span></span>



| <span data-ttu-id="0f353-657">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f353-657">Requirement</span></span> | <span data-ttu-id="0f353-658">Valor</span><span class="sxs-lookup"><span data-stu-id="0f353-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f353-659">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f353-659">Minimum supported client</span></span><br/> | <span data-ttu-id="0f353-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f353-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f353-661">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f353-661">Minimum supported server</span></span><br/> | <span data-ttu-id="0f353-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f353-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f353-663">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f353-663">Namespace</span></span><br/>                | <span data-ttu-id="0f353-664">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0f353-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f353-665">MOF</span><span class="sxs-lookup"><span data-stu-id="0f353-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f353-666"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f353-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f353-667">DLL</span><span class="sxs-lookup"><span data-stu-id="0f353-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f353-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f353-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f353-669">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f353-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f353-670">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0f353-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0f353-671">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="0f353-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0f353-672">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="0f353-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="0f353-673">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="0f353-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="0f353-674">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="0f353-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
