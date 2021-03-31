---
title: Classe MicrosoftDNS_Server
description: A \_ classe de servidor MicrosoftDNS descreve um servidor DNS. Cada instância dessa classe pode ser associada a uma instância do cache MicrosoftDNS \_ , uma instância de MicrosoftDNS \_ RootHints e várias instâncias da \_ zona MicrosoftDNS.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- MicrosoftDNS_Server de classe de DNS
- MicrosoftDNS_Server de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918058"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="0dc9d-106">\_Classe de servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="0dc9d-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="0dc9d-107">A classe de **\_ servidor MicrosoftDNS** descreve um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="0dc9d-108">Cada instância dessa classe pode ser associada a uma instância do [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), uma instância de [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)e várias instâncias da [**\_ zona MicrosoftDNS**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="0dc9d-109">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc9d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dc9d-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="0dc9d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0dc9d-111">Members</span></span>

<span data-ttu-id="0dc9d-112">A classe de **\_ servidor MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0dc9d-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="0dc9d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dc9d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dc9d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0dc9d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dc9d-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dc9d-115">Methods</span></span>

<span data-ttu-id="0dc9d-116">A classe de **\_ servidor MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="0dc9d-117">Método</span><span class="sxs-lookup"><span data-stu-id="0dc9d-117">Method</span></span>                   | <span data-ttu-id="0dc9d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dc9d-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="0dc9d-119">**Getdistinguiname**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="0dc9d-120">Recupera o nome distinto do DNS para a zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="0dc9d-121">**StartScavenging**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-121">**StartScavenging**</span></span>      | <span data-ttu-id="0dc9d-122">Inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="0dc9d-123">**StartService**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-123">**StartService**</span></span>         | <span data-ttu-id="0dc9d-124">Inicia o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="0dc9d-125">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-125">**StopService**</span></span>          | <span data-ttu-id="0dc9d-126">Interrompe o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="0dc9d-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0dc9d-127">Properties</span></span>

<span data-ttu-id="0dc9d-128">A classe de **\_ servidor MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0dc9d-129">**AddressAnswerLimit**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-132">Número máximo de registros de host retornados em resposta a uma solicitação de endereço.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="0dc9d-133">Os valores entre 5 e 28 são válidos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-134">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-137">Especifica se o servidor DNS aceita solicitações de atualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="0dc9d-138">Os valores válidos são como mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="0dc9d-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-139">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-140">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-142">Sem restrições.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-144">Não permite atualizações dinâmicas de registros SOA.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-146">Não permite atualizações dinâmicas de registros NS na raiz da zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="0dc9d-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-148">Não permite atualizações dinâmicas de registros NS que não estejam na raiz da zona (registros NS de delegação).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="0dc9d-149">Some esses valores para determinar o valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-150">**AutoCacheUpdate**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-151">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-153">Indica se o servidor DNS tenta atualizar suas entradas de cache usando dados de servidores raiz.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="0dc9d-154">Quando um servidor DNS é inicializado, ele precisa de uma lista de NS ' dicas ' do servidor raiz e registros a para os servidores, historicamente chamados de arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="0dc9d-155">Os servidores DNS da Microsoft têm um recurso que permite que eles tentem gravar um novo arquivo de cache com base nas respostas dos servidores raiz.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-156">**AutoConfigFileZones**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-159">Indica quais zonas primárias padrão que são autoritativas para o nome do servidor DNS devem ser atualizadas quando o servidor de nomes for alterado.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="0dc9d-160">Estes são os valores válidos:</span><span class="sxs-lookup"><span data-stu-id="0dc9d-160">Valid values are as follows:</span></span>



| <span data-ttu-id="0dc9d-161">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-161">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-162">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-164">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-166">Somente servidores que permitem atualizações dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-168">Somente servidores que não permitem atualizações dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="0dc9d-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-170">Todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="0dc9d-171">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-171">The default value is 1.</span></span>

<span data-ttu-id="0dc9d-172">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="0dc9d-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="0dc9d-173">O número 3 representa todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-174">**BindSecondaries**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-175">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-177">Determina o formato de mensagem AXFR ao enviar para secundários de servidor DNS não Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="0dc9d-178">Quando definido como TRUE, o servidor DNS envia transferências para secundários do servidor DNS não Microsoft no formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="0dc9d-179">Quando for falso, todas as transferências serão enviadas no formato rápido.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-180">**BootMethod**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-183">Método de inicialização para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="0dc9d-184">Os valores válidos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="0dc9d-185">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-185">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-186">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-188">Não inicializado.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-190">Inicialize do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-192">Inicializar do registro.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="0dc9d-193"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-194">Inicialize do diretório e do registro.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0dc9d-195">**Defaultenvelhecimentostate**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-198">Valor de **ScavengingInterval** padrão definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="0dc9d-199">O valor padrão é zero, indicando que a limpeza está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-203">Intervalo sem atualização, em horas, definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="0dc9d-204">O valor padrão é 168 horas (sete dias).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-206">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-207">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-208">Intervalo de atualização, em horas, definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="0dc9d-209">O valor padrão é 168 horas (sete dias).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-210">**DisableAutoReverseZones**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-211">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-212">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-213">Indica se o servidor DNS cria automaticamente zonas de pesquisa inversa padrão.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-214">**DisjointNets**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-215">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-217">Indica se a associação de porta padrão para um soquete usado para enviar consultas para servidores DNS remotos pode ser substituída.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-218">**DsAvailable**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-221">Indica se há um DS disponível no servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-222">**DsPollingInterval**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-223">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-224">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-225">Intervalo, em segundos, para sondar as zonas integradas ao DS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-226">**DsTombstoneInterval**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-227">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-228">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-229">Tempo de vida dos registros marcados para exclusão nas zonas integradas do serviço de diretório, expresso em segundos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-230">**EDnsCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-231">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-233">Tempo de vida, em segundos, das informações armazenadas em cache que descrevem a versão do EDNS com suporte de outros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-234">**EnableDirectoryPartitions**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-235">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-236">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-237">Especifica se o suporte para partições de diretório de aplicativo está habilitado no servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="0dc9d-238">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="0dc9d-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="0dc9d-239">Esse método é denominado EnableDirectoryPartitionSupport.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-241">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-242">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-243">Especifica se o servidor DNS inclui RRs específicos do DNSSEC, chave, SIG e NXT em uma resposta, de acordo com a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="0dc9d-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="0dc9d-244">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-244">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-245">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-247">Nenhum registro DNSSEC é incluído na resposta, a menos que a consulta solicitou um conjunto de registros de recursos do tipo de registro DNSSEC.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-249">Os registros DNSSEC são incluídos na resposta de acordo com a RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-251">Os registros DNSSEC são incluídos em uma resposta somente se a consulta do cliente original contivesse o registro de recurso OPT de acordo com a RFC 2671</span><span class="sxs-lookup"><span data-stu-id="0dc9d-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="0dc9d-252">Se uma consulta solicitar um conjunto de registros de recursos do tipo DNSSEC, o servidor DNS sempre responderá com esses registros, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-254">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-255">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-256">Especifica o comportamento do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="0dc9d-257">Quando TRUE, o servidor DNS sempre responde com registros de recursos OPCIONais de acordo com a RFC 2671, a menos que o servidor remoto tenha indicado que ele não oferece suporte ao EDNS em um Exchange anterior.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="0dc9d-258">Se for FALSE, o servidor DNS responderá a consultas com optas somente se as optas forem enviadas na consulta original.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-260">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-261">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-262">Indica quais eventos o servidor DNS registra no log do sistema Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="0dc9d-263">Os valores a seguir são usados.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-263">The following values are used.</span></span>



| <span data-ttu-id="0dc9d-264">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-264">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-265">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-267">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-269">Registrar apenas erros.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-271">Registrar somente avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="0dc9d-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-273">Registrar todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="0dc9d-274">**ForwardDelegations**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-275">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-276">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-277">Especifica se as consultas a subzonas delegadas são encaminhadas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-278">**Encaminhadores**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-279">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-280">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-281">Enumera a lista de endereços IP de encaminhadores para os quais o servidor DNS encaminha consultas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-282">**ForwardingTimeout**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-284">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-285">Tempo, em segundos, um servidor DNS que encaminha uma consulta aguardará a resolução do [*encaminhador*](f-gly.md) antes de tentar resolver a consulta em si.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="0dc9d-286">Esse valor será inútil se o servidor de encaminhamento não estiver definido para usar recursão.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="0dc9d-287">Para determinar isso, verifique a propriedade booliana do isslave.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-288">**Isslave**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-291">**True** se o servidor DNS não usar recursão quando a resolução de nomes por meio de encaminhadores falhar.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-292">**ListenAddresses**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-293">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-294">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-295">Enumera a lista de endereços IP nos quais o servidor DNS pode receber consultas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-296">**LocalNetPriority**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-298">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-299">Indica se o servidor DNS fornece prioridade para o endereço de rede local ao retornar registros A.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-301">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-302">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-303">Tamanho do log de depuração do servidor DNS, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-306">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-307">Nome do arquivo e caminho para o log de depuração do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="0dc9d-308">O padrão é% system32% \\ DNS \\ DNS. log.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="0dc9d-309">Os caminhos relativos são relativos a% SystemRoot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="0dc9d-310">Caminhos absolutos podem ser usados, mas não há suporte para caminhos UNC.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-311">**LogIPFilterList**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-312">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-313">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-314">Lista de endereços IP usados para filtrar eventos DNS gravados no log de depuração.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-316">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-317">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-318">Indica quais políticas são ativadas no log do sistema Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="0dc9d-319">Deve ser definido como valores específicos com base no seguinte algoritmo: cada política (a ser ativada no log do sistema Visualizador de Eventos) recebe um valor específico.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="0dc9d-320">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-320">Value</span></span>                                                                                                                  | <span data-ttu-id="0dc9d-321">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="0dc9d-323">Consultá.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="0dc9d-324"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="0dc9d-325">Sobre.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="0dc9d-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="0dc9d-327">Update.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="0dc9d-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="0dc9d-329">Transações não consulta.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="0dc9d-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="0dc9d-331">Perguntas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="0dc9d-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="0dc9d-333">Respectivas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="0dc9d-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="0dc9d-335">Enviar.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="0dc9d-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="0dc9d-337">Recebe.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="0dc9d-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="0dc9d-339">UDP.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="0dc9d-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="0dc9d-341">TCP.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="0dc9d-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="0dc9d-343">Todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="0dc9d-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="0dc9d-345">Transação de gravação do serviço de diretório do NT.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="0dc9d-346"><dt>**131072**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="0dc9d-347">Transação de atualização do serviço de diretório do NT.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="0dc9d-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="0dc9d-349">Pacotes completos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="0dc9d-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-351">Gravação.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="0dc9d-352">A soma dos valores correspondentes a todas as políticas a serem ativadas é indicada nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-353">**LooseWildcarding**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-354">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-355">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-356">Indica se o servidor DNS executa curingas flexíveis.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="0dc9d-357">Se for indefinido ou zero, o servidor seguirá o comportamento curinga especificado na RFC do DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="0dc9d-358">Nesse caso, é aconselhável que um administrador inclua registros MX para todos os hosts que não têm capacidade de receber emails.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="0dc9d-359">Se for diferente de zero, o servidor buscará o nó curinga mais próximo; Nesse caso, um administrador deve colocar os registros MX na raiz da zona e em um nó curinga (' \* ') diretamente abaixo da raiz da zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="0dc9d-360">Além disso, os administradores devem colocar os registros MX de referência automática em hosts que recebem seus próprios emails.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-361">**MaxCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-362">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-363">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-364">Tempo máximo, em segundos, o registro de uma consulta de nome recursivo pode permanecer no cache do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="0dc9d-365">O servidor DNS exclui registros do cache quando o valor dessa entrada expira, mesmo que o valor do campo TTL no registro seja maior.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="0dc9d-366">O valor padrão dessa propriedade é 86.400 segundos (1 dia).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-367">**MaxNegativeCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-368">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-369">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-370">Tempo máximo, em segundos, um resultado de erro de nome de uma consulta recursiva pode permanecer no cache do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="0dc9d-371">O DNS exclui registros do cache quando esse temporizador expira, mesmo que o campo TTL seja maior.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="0dc9d-372">O valor padrão é 86.400 (um dia).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dc9d-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-376">FQDN (nome de domínio totalmente qualificado) ou endereço IP do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-377">**NameCheckFlag**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-378">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-379">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-380">Indica o conjunto de caracteres qualificados a ser usado em nomes DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="0dc9d-381">Os valores a seguir são usados.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-381">The following values are used.</span></span>



| <span data-ttu-id="0dc9d-382">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-382">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-383">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-385">RFC estrito (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0dc9d-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-387">Não RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0dc9d-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="0dc9d-388"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-389">Multibyte (UTF8)</span><span class="sxs-lookup"><span data-stu-id="0dc9d-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="0dc9d-390">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="0dc9d-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="0dc9d-391">Um valor de "2" indica "any".</span><span class="sxs-lookup"><span data-stu-id="0dc9d-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-392">**Recursão**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-393">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-394">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-395">Indica se o servidor DNS executa Pesquisas recursivas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="0dc9d-396">VERDADEIRO indica que as pesquisas recursivas não são executadas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-397">**RecursionRetry**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-398">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-399">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-400">Segundos decorridos antes de tentar novamente uma pesquisa recursiva.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="0dc9d-401">Se a propriedade for indefinida ou zero, as novas tentativas serão feitas após três segundos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="0dc9d-402">Os usuários não são incentivados de alterar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="0dc9d-403">Há certas situações em que a propriedade deve ser alterada; um exemplo é quando o servidor DNS entra em contato com servidores remotos por um link lento e o servidor DNS está tentando novamente antes de receber a resposta do DNS remoto.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="0dc9d-404">Nesse caso, aumentar o tempo para ser um pouco mais longo do que o tempo de resposta observado do DNS remoto seria razoável.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-405">**RecursionTimeout**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-406">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-407">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-408">Segundos decorridos antes que o servidor DNS forneça uma consulta recursiva.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="0dc9d-409">Se a propriedade for indefinida ou zero, o servidor DNS será disponibilizado após 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="0dc9d-410">Em geral, o tempo limite de 15 segundos é suficiente para permitir que qualquer resposta pendente volte ao servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="0dc9d-411">Os usuários não são incentivados de alterar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="0dc9d-412">Um cenário em que a propriedade deve ser alterada é quando o servidor DNS entra em contato com servidores remotos por um link lento, e o servidor DNS observa a rejeição de consultas (com falha do servidor \_ ) antes que as respostas sejam recebidas.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="0dc9d-413">Os resolvedores de cliente também tentam consultas novamente, portanto, uma investigação cuidadosa é necessária para determinar se as respostas remotas estão realmente associadas à consulta que atingiu o tempo limite. Nesse caso, elevar o valor de tempo limite para ser um pouco mais longo do que o tempo de resposta observado do DNS remoto seria razoável.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-414">**RoundRobin**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-415">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-416">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-417">Indica se o servidor DNS arredondado Robin vários registros A.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-418">**RpcProtocol**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-419">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-420">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-421">Protocolo RPC ou protocolos sobre os quais o RPC administrativo é executado.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="0dc9d-422">O algoritmo a seguir é usado para atribuir um valor específico:</span><span class="sxs-lookup"><span data-stu-id="0dc9d-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="0dc9d-423">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-423">Value</span></span>                                                                                                | <span data-ttu-id="0dc9d-424">Significado</span><span class="sxs-lookup"><span data-stu-id="0dc9d-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0dc9d-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-426">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0dc9d-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="0dc9d-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-428">TCP</span><span class="sxs-lookup"><span data-stu-id="0dc9d-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="0dc9d-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-430">Pipes nomeados</span><span class="sxs-lookup"><span data-stu-id="0dc9d-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="0dc9d-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0dc9d-432">LPC</span><span class="sxs-lookup"><span data-stu-id="0dc9d-432">LPC</span></span><br/>         |



 

<span data-ttu-id="0dc9d-433">A soma dos valores indica os protocolos usados.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-435">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-436">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-437">Intervalo, em horas, entre duas operações de eliminação consecutivas executadas pelo servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="0dc9d-438">Zero indica que a limpeza está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="0dc9d-439">O valor padrão é 168 horas (sete dias).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-440">**SecureResponses**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-441">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-442">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-443">Indica se o servidor DNS salva exclusivamente os registros de nomes na mesma subárvore que o servidor que os forneceu.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-445">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-446">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-447">Porta na qual o servidor DNS envia consultas UDP para outros servidores.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="0dc9d-448">Por padrão, o servidor DNS envia consultas em um soquete associado à porta DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="0dc9d-449">Em determinadas situações, essa não é a melhor configuração.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="0dc9d-450">Um caso óbvio é quando um administrador bloqueia a porta DNS com um firewall para impedir o acesso externo ao servidor DNS, mas ainda quer que o servidor seja capaz de contatar os servidores DNS da Internet para fornecer resolução de nomes para clientes internos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="0dc9d-451">Outro caso é quando o servidor DNS oferece suporte a redes não atendidas (a propriedade **DisjointNets** definida como true identifica esse cenário).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="0dc9d-452">Nesses casos, definir a propriedade **SendOnNonDnsPort** como um valor diferente de zero direciona o servidor DNS para se associar a uma porta arbitrária para enviar para servidores DNS remotos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="0dc9d-453">Se o valor de **SendOnNonDnsPort** for maior que 1024, o servidor DNS será associado explicitamente ao valor de porta fornecido.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="0dc9d-454">Essa opção de configuração é útil quando um administrador precisa corrigir a porta de consulta DNS para fins de firewall.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="0dc9d-455">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="0dc9d-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="0dc9d-456">Definir a propriedade SendPort como um valor diferente de zero faz com que o servidor DNS se vincule a uma porta arbitrária para enviar para servidores DNS remotos.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-457">**ServerAddresses**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-458">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dc9d-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-460">Enumera a lista de endereços IP para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-461">**StrictFileParsing**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-462">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-463">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-464">Indica se o servidor DNS analisa os [*arquivos de zona*](z-gly.md) estritamente.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="0dc9d-465">Se for indefinido ou igual a zero, o servidor registrará e ignorará dados inválidos no arquivo de zona e continuará a carregar.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="0dc9d-466">Se for diferente de zero, o servidor fará o log e falhará em erros de arquivo de zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-467">**UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-468">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dc9d-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-470">Restringe o tipo de registro que pode ser atualizado dinamicamente no servidor, usado além das configurações de **AllowUpdate** em objetos de servidor e de zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="0dc9d-471">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="0dc9d-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="0dc9d-472">0: sem restrições.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-472">0: No restrictions.</span></span>

<span data-ttu-id="0dc9d-473">1: não permitir atualizações dinâmicas de registros SOA.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="0dc9d-474">2: não permitir atualizações dinâmicas de registros NS na raiz da zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="0dc9d-475">4: não permitir atualizações dinâmicas de registros NS não na raiz da zona (registros NS de delegação).</span><span class="sxs-lookup"><span data-stu-id="0dc9d-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="0dc9d-476">Some esses valores para determinar o valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-477">**Versão**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-478">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dc9d-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-480">Versão do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-481">**WriteAuthorityNS**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-482">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-483">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-484">Especifica se o servidor DNS grava os registros NS e SOA na seção autoridade sobre uma resposta bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9d-485">**XfrConnectTimeout**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dc9d-486">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dc9d-487">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0dc9d-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0dc9d-488">Tempo, em segundos, o servidor DNS aguarda uma conexão TCP bem-sucedida para um servidor remoto ao tentar uma transferência de zona.</span><span class="sxs-lookup"><span data-stu-id="0dc9d-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dc9d-489">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc9d-489">Requirements</span></span>



| <span data-ttu-id="0dc9d-490">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc9d-490">Requirement</span></span> | <span data-ttu-id="0dc9d-491">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc9d-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc9d-492">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dc9d-492">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc9d-493">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0dc9d-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0dc9d-494">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dc9d-494">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc9d-495">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0dc9d-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0dc9d-496">Namespace</span><span class="sxs-lookup"><span data-stu-id="0dc9d-496">Namespace</span></span><br/>                | <span data-ttu-id="0dc9d-497">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="0dc9d-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0dc9d-498">MOF</span><span class="sxs-lookup"><span data-stu-id="0dc9d-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0dc9d-499"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9d-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc9d-500">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0dc9d-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc9d-501">**Método StartService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="0dc9d-502">**Método StopService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="0dc9d-503">**Método StartScavenging da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="0dc9d-504">**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="0dc9d-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





