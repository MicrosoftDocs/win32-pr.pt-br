---
title: Classe MicrosoftDNS_Zone
description: A \_ classe de zona MicrosoftDNS descreve uma zona DNS. Cada instância da classe de \_ zona MicrosoftDNS deve ser atribuída a exatamente um servidor DNS. As zonas podem ser associadas a várias instâncias do \_ domínio MicrosoftDNS ou \_ classes MicrosoftDNS ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone de classe de DNS
- MicrosoftDNS_Zone de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009866"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="ea4c6-107">\_Classe de zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ea4c6-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="ea4c6-108">Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ea4c6-109">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="ea4c6-110">Este artigo contém referências ao termo servidor mestre, um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ea4c6-111">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="ea4c6-112">A classe de **\_ zona MicrosoftDNS** descreve uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="ea4c6-113">Cada instância da classe **de \_ zona MicrosoftDNS** deve ser atribuída a exatamente um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="ea4c6-114">As zonas podem ser associadas a várias instâncias [**do \_ domínio MicrosoftDNS**](microsoftdns-domain.md) ou classes [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4c6-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="ea4c6-115">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4c6-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea4c6-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="ea4c6-117">Membros</span><span class="sxs-lookup"><span data-stu-id="ea4c6-117">Members</span></span>

<span data-ttu-id="ea4c6-118">A classe de **\_ zona MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ea4c6-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="ea4c6-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea4c6-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea4c6-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea4c6-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea4c6-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea4c6-121">Methods</span></span>

<span data-ttu-id="ea4c6-122">A classe de **\_ zona MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="ea4c6-123">Método</span><span class="sxs-lookup"><span data-stu-id="ea4c6-123">Method</span></span>                   | <span data-ttu-id="ea4c6-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea4c6-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4c6-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="ea4c6-126">Habilita a expiração para alguns ou todos os registros não NS e não SOA.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="ea4c6-127">**ChangeZoneType**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="ea4c6-128">Altera os tipos de zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-128">Changes zone types.</span></span> <br/> <span data-ttu-id="ea4c6-129">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="ea4c6-130">**Createzone**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-130">**CreateZone**</span></span>           | <span data-ttu-id="ea4c6-131">Cria uma nova zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="ea4c6-132">Qualificadores: nenhum.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="ea4c6-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-133">**ForceRefresh**</span></span>         | <span data-ttu-id="ea4c6-134">Força uma atualização do secundário do servidor DNS mestre.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="ea4c6-135">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="ea4c6-136">**Getdistinguiname**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="ea4c6-137">Obtém o nome distinto do DS para a zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="ea4c6-138">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="ea4c6-139">**PauseZone**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-139">**PauseZone**</span></span>            | <span data-ttu-id="ea4c6-140">Pausa a zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="ea4c6-141">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="ea4c6-142">**ReloadZone**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-142">**ReloadZone**</span></span>           | <span data-ttu-id="ea4c6-143">Recarrega a zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="ea4c6-144">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ea4c6-145">**ResetSecondaries**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="ea4c6-146">Redefine a matriz de endereço IP secundário.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="ea4c6-147">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="ea4c6-148">**ResumeZone**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-148">**ResumeZone**</span></span>           | <span data-ttu-id="ea4c6-149">Retoma a zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="ea4c6-150">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ea4c6-151">**UpdateFromDS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="ea4c6-152">Força uma atualização da zona do serviço de diretório (DS).</span><span class="sxs-lookup"><span data-stu-id="ea4c6-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="ea4c6-153">Para que esse método seja válido, o Zonetype deve ser 0. na verdade, a zona deve ser armazenada no DS.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="ea4c6-154">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ea4c6-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="ea4c6-155">**WriteBackZone**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-155">**WriteBackZone**</span></span>        | <span data-ttu-id="ea4c6-156">Salva dados de zona em seu arquivo de zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="ea4c6-157">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ea4c6-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="ea4c6-158">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea4c6-158">Properties</span></span>

<span data-ttu-id="ea4c6-159">A classe de **\_ zona MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea4c6-160">**Estágios**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-161">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-163">Especifica o comportamento de expiração e eliminação da zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="ea4c6-164">Zero indica que a limpeza está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="ea4c6-165">Quando a eliminação está desabilitada, os carimbos de data/hora dos registros na zona não são atualizados e os registros não estão sujeitos à eliminação.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="ea4c6-166">Quando definido como um, os registros estão sujeitos à eliminação e seus carimbos de data/hora são atualizados quando o servidor recebe a solicitação de atualização dinâmica para os registros.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="ea4c6-167">Para zonas integradas Active Directory, esse valor é definido como a propriedade *Defaultenvelhecimentostate* do servidor DNS onde a zona é criada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="ea4c6-168">Para zonas primárias padrão, o valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-169">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-172">Indica se a zona aceita solicitações de atualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-173">**Criado automaticamente**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-176">Indica se a zona é criada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-177">**AvailForScavengeTime**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-178">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-180">Especifica a hora em que o servidor pode tentar eliminar a zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="ea4c6-181">Mesmo que a zona esteja configurada para habilitar a eliminação, o servidor DNS não tentará recuperar essa zona até esse momento.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="ea4c6-182">Esse valor é definido como a hora atual mais o intervalo de atualização da zona sempre que a zona é carregada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="ea4c6-183">Esse parâmetro é armazenado localmente e não é replicado para outras cópias da zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-184">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-187">Indica o nome do arquivo de zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-188">**DisableWINSRecordReplication**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-189">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-191">Indica se o registro WINS é replicado.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="ea4c6-192">Se definido como TRUE, a replicação do registro WINS será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-193">**DsIntegrated**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-194">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-196">Especifica se a zona é integrada ao DS.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-197">**ForwarderSlave**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-198">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-200">Indica se o DNS usa recursão ao resolver os nomes para a zona de encaminhamento especificada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="ea4c6-201">Aplicável somente a zonas de encaminhamento condicionais.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-202">**ForwarderTimeout**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-205">Indica o tempo, em segundos, que um servidor DNS que encaminha uma consulta para o nome na zona de encaminhamento aguarda a resolução do encaminhador antes de tentar resolver a consulta em si.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="ea4c6-206">Esse parâmetro é aplicável somente às zonas de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-207">**LastSuccessfulSoaCheck**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-210">Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde a última verificação do número de série SOA da zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-211">**LastSuccessfulXfr**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-212">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-214">Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde que a zona foi transferida pela última vez de um servidor mestre.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-215">**LocalMasterServers**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-216">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-218">Endereços IP locais dos servidores DNS mestre para esta zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="ea4c6-219">Se definido, esses mestres ultrapassarão o MasterServers encontrado em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-220">**MasterServers**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-221">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-223">Endereços IP dos servidores DNS mestre para esta zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-227">Especifica o intervalo de tempo entre a última atualização do carimbo de data/hora de um registro e o primeiro momento em que o carimbo de data/hora pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-228">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-229">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-231">Indica se a zona mestra notifica os secundários de quaisquer alterações em seu banco de dados RRs.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="ea4c6-232">Defina como 1 para notificar secundários.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-233">**NotifyServers**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-234">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-236">Matriz de cadeias de caracteres que enumeram endereços IP de servidores DNS para serem notificados sobre alterações nessa zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-237">**Em pausa**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-238">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-240">Indica se a zona está pausada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-241">**Intervalo de atualização**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-242">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-244">Especifica o intervalo de atualização durante o qual os registros com carimbo de data/hora diferente devem ser atualizados para permanecer na zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="ea4c6-245">Os registros que não foram atualizados pela expiração do intervalo de atualização podem ser removidos pela próxima limpeza executada por um servidor.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="ea4c6-246">Esse valor nunca deve ser menor do que o período de atualização mais longo dos registros registrados na zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="ea4c6-247">Valores muito pequenos podem levar à remoção de registros DNS válidos.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="ea4c6-248">valores muito grandes prolongam o tempo de vida dos registros obsoletos.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="ea4c6-249">Esse valor é definido como a propriedade *DefaultRefreshInterval* do servidor DNS onde a zona é criada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-250">**Ordem**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-253">Indica se a zona é inversa (TRUE) ou Forward (FALSE).</span><span class="sxs-lookup"><span data-stu-id="ea4c6-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-254">**ScavengeServers**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-255">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-257">Matriz de cadeias de caracteres que enumera a lista de endereços IP de servidores DNS que têm permissão para executar a eliminação de registros obsoletos dessa zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="ea4c6-258">Se a lista não for especificada, qualquer servidor DNS primário autoritativo para a zona poderá eliminar a zona quando outros pré-requisitos forem atendidos.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-259">**SecondaryServers**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-260">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-262">Matriz de cadeias de caracteres que enumeram endereços IP de servidores DNS com permissão para receber essa zona por meio da replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-263">**SecureSecondaries**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-266">Indica se a transferência de zona é permitida apenas para secundários designados.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="ea4c6-267">Os secundários designados são servidores DNS cujos endereços IP são listados em SecondariesIPAddressesArray.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-268">**Desligamento**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-269">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-271">Indica se a cópia da zona expirou.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="ea4c6-272">Se for TRUE, a zona expirará ou será desligada.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-273">**UseNBStat**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-274">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-276">Esse booliano indica se a zona usa a pesquisa inversa do NBStat.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-277">**UseWins**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-278">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-280">Indica se a zona usa a pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="ea4c6-281">**ZoneType**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4c6-282">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4c6-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea4c6-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4c6-284">Indica o tipo da zona.</span><span class="sxs-lookup"><span data-stu-id="ea4c6-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="ea4c6-285">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="ea4c6-285">Valid values are:</span></span>

-   <span data-ttu-id="ea4c6-286">Integrado ao DS</span><span class="sxs-lookup"><span data-stu-id="ea4c6-286">DS integrated</span></span>
-   <span data-ttu-id="ea4c6-287">Primária</span><span class="sxs-lookup"><span data-stu-id="ea4c6-287">Primary</span></span>
-   <span data-ttu-id="ea4c6-288">Secundário</span><span class="sxs-lookup"><span data-stu-id="ea4c6-288">Secondary</span></span>

<span data-ttu-id="ea4c6-289">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="ea4c6-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="ea4c6-290">Valores adicionais:</span><span class="sxs-lookup"><span data-stu-id="ea4c6-290">Additional values:</span></span>

-   <span data-ttu-id="ea4c6-291">Cache</span><span class="sxs-lookup"><span data-stu-id="ea4c6-291">Cache</span></span>
-   <span data-ttu-id="ea4c6-292">Gerenciador</span><span class="sxs-lookup"><span data-stu-id="ea4c6-292">Stub</span></span>
-   <span data-ttu-id="ea4c6-293">Encaminhador de</span><span class="sxs-lookup"><span data-stu-id="ea4c6-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea4c6-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4c6-294">Requirements</span></span>



| <span data-ttu-id="ea4c6-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4c6-295">Requirement</span></span> | <span data-ttu-id="ea4c6-296">Valor</span><span class="sxs-lookup"><span data-stu-id="ea4c6-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4c6-297">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea4c6-297">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4c6-298">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ea4c6-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea4c6-299">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea4c6-299">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4c6-300">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea4c6-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea4c6-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea4c6-301">Namespace</span></span><br/>                | <span data-ttu-id="ea4c6-302">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ea4c6-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ea4c6-303">MOF</span><span class="sxs-lookup"><span data-stu-id="ea4c6-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea4c6-304"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea4c6-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4c6-305">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea4c6-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4c6-306">**\_Domínio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-307">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-308">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-309">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-310">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-311">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-312">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-313">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-314">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-315">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-316">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="ea4c6-317">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ea4c6-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





