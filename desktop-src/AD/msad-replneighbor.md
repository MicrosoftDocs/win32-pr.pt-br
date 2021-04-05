---
title: Classe MSAD_ReplNeighbor
description: Representa a \_ estrutura de vizinho de repl DS \_ , que contém as informações de estado de replicação de entrada para um determinado NC (contexto de nomenclatura) e par de servidor de origem.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_ReplNeighbor Active Directory
- Active Directory de MSAD_ReplNeighbor classe, descrita
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918493"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="8b166-105">\_Classe MSAD ReplNeighbor</span><span class="sxs-lookup"><span data-stu-id="8b166-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="8b166-106">Representa a estrutura de [**\_ \_ vizinho de repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , que contém as informações de estado de replicação de entrada para um determinado NC (contexto de nomenclatura) e par de servidor de origem, conforme retornado pela função [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="8b166-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b166-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b166-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="8b166-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8b166-108">Members</span></span>

<span data-ttu-id="8b166-109">A classe **MSAD \_ ReplNeighbor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b166-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="8b166-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b166-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b166-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b166-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b166-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b166-112">Methods</span></span>

<span data-ttu-id="8b166-113">A classe **MSAD \_ ReplNeighbor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8b166-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="8b166-114">Método</span><span class="sxs-lookup"><span data-stu-id="8b166-114">Method</span></span>                                                           | <span data-ttu-id="8b166-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b166-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="8b166-116">**SyncNamingContext**</span><span class="sxs-lookup"><span data-stu-id="8b166-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="8b166-117">Sincroniza um contexto de nomenclatura de destino com uma de suas fontes.</span><span class="sxs-lookup"><span data-stu-id="8b166-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8b166-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b166-118">Properties</span></span>

<span data-ttu-id="8b166-119">A classe **MSAD \_ ReplNeighbor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b166-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b166-120">**AsyncIntersiteTransportDN**</span><span class="sxs-lookup"><span data-stu-id="8b166-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-123">Obtém o caminho X. 500 do objeto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) que corresponde ao transporte sobre o qual a replicação é executada.</span><span class="sxs-lookup"><span data-stu-id="8b166-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="8b166-124">Defina como **nulo** para replicação RPC/IP.</span><span class="sxs-lookup"><span data-stu-id="8b166-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-125">**AsyncIntersiteTransportObjGuid**</span><span class="sxs-lookup"><span data-stu-id="8b166-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-128">Obtém o GUID do objeto de transporte entre sites que corresponde à propriedade **AsyncIntersiteTransportDN** .</span><span class="sxs-lookup"><span data-stu-id="8b166-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-129">**CompressChanges**</span><span class="sxs-lookup"><span data-stu-id="8b166-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-132">Obtém o valor que indica se o sinalizador **DS \_ repl/ \_ \_ compactar \_ alterações** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-133">**DisableScheduledSync**</span><span class="sxs-lookup"><span data-stu-id="8b166-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-136">Obtém o valor que indica se o sinalizador de **\_ \_ \_ \_ \_ sincronização agendada do DS repl/desabilitar** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-137">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="8b166-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-140">Obtém o nome canônico do domínio do NC replicado.</span><span class="sxs-lookup"><span data-stu-id="8b166-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-141">**DoScheduledSyncs**</span><span class="sxs-lookup"><span data-stu-id="8b166-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-144">Obtém o valor que indica se o sinalizador **DS \_ repl de \_ \_ \_ \_ sincronizações agendadas** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-145">**FullSyncInProgress**</span><span class="sxs-lookup"><span data-stu-id="8b166-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-148">Obtém o valor que indica se o **sinalizador \_ DS \_ repl \_ total \_ Sync \_ em \_ andamento** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-149">**FullSyncNextPacket**</span><span class="sxs-lookup"><span data-stu-id="8b166-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-152">Obtém o valor que indica se o sinalizador de **\_ \_ \_ \_ \_ próximo \_ pacote de sincronização completa do DS repl** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-153">**IgnoreChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="8b166-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-154">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-156">Obtém o valor que indica se o sinalizador de **alteração do DS \_ repl \_ n º \_ ignorar \_ \_ notificações de mudança** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-157">**IsDeletedSourceDsa**</span><span class="sxs-lookup"><span data-stu-id="8b166-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-158">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-160">Obtém o valor que indica se essa conexão representa um controlador de domínio de origem que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="8b166-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="8b166-161">**True** se essa conexão representa um DC de origem que foi excluído; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="8b166-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="8b166-162">Por design, o DS continuará replicando essas conexões por algum tempo por algum tempo depois que o DC de origem for excluído.</span><span class="sxs-lookup"><span data-stu-id="8b166-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-163">**LastSyncResult**</span><span class="sxs-lookup"><span data-stu-id="8b166-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b166-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-166">Obtém o código de erro **HRESULT** para a última tentativa de replicação.</span><span class="sxs-lookup"><span data-stu-id="8b166-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="8b166-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b166-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-170">Obtém o número de tentativas de replicação com falha consecutivas, não incluindo as conexões que se espera que falhem.</span><span class="sxs-lookup"><span data-stu-id="8b166-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="8b166-171">Por exemplo, se a propriedade **IsDeletedSourceDsa** for definida como **true**, espera-se que ela falhe.</span><span class="sxs-lookup"><span data-stu-id="8b166-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-172">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="8b166-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b166-175">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b166-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b166-176">Obtém o caminho X. 500 para o NC que é replicado por essa conexão.</span><span class="sxs-lookup"><span data-stu-id="8b166-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-177">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="8b166-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-180">Obtém o GUID para o NC replicado.</span><span class="sxs-lookup"><span data-stu-id="8b166-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-181">**NeverSynced**</span><span class="sxs-lookup"><span data-stu-id="8b166-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-182">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-184">Obtém o valor que indica se o sinalizador **DS \_ repl \_ n \_ Never não \_ sincronizado** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-185">**NoChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="8b166-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-186">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-188">Obtém o valor que indica se o sinalizador **DS \_ repl \_ n \_ nenhum \_ \_ notificações de alteração** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-189">**NumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="8b166-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-190">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b166-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-192">Obtém o número de tentativas consecutivas de replicação com falha.</span><span class="sxs-lookup"><span data-stu-id="8b166-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-193">**ReplicaFlags**</span><span class="sxs-lookup"><span data-stu-id="8b166-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-194">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b166-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-196">Obtém o conjunto de sinalizadores que especificam atributos e opções para os dados de replicação.</span><span class="sxs-lookup"><span data-stu-id="8b166-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="8b166-197">Essa propriedade pode ser zero ou uma combinação de um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b166-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="8b166-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ n \_ Writeable** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="8b166-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-199">A cópia local do contexto de nomenclatura é gravável.</span><span class="sxs-lookup"><span data-stu-id="8b166-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="8b166-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ \_ \_ Sincronização de repl n \_ na \_ inicialização** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="8b166-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-201">A replicação desse contexto de nomenclatura dessa fonte é tentada quando o servidor de destino é inicializado.</span><span class="sxs-lookup"><span data-stu-id="8b166-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="8b166-202">Esse sinalizador geralmente se aplica apenas a vizinhos dentro do site.</span><span class="sxs-lookup"><span data-stu-id="8b166-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="8b166-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ N º de REPL para \_ \_ \_ \_ sincronizações agendadas** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="8b166-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-204">Execute a replicação de acordo com um agendamento.</span><span class="sxs-lookup"><span data-stu-id="8b166-204">Perform replication on a schedule.</span></span> <span data-ttu-id="8b166-205">Esse sinalizador geralmente é definido, a menos que o agendamento para esse contexto de nomenclatura ou origem seja "Never", ou seja, o agendamento vazio.</span><span class="sxs-lookup"><span data-stu-id="8b166-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="8b166-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ O \_ n º de repl \_ usa \_ \_ \_ transporte assíncrono entre sites** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8b166-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-207">Execute a replicação indiretamente por meio do Serviço de Mensagens Entre Sites.</span><span class="sxs-lookup"><span data-stu-id="8b166-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="8b166-208">Este sinalizador é definido somente durante a replicação por SMTP.</span><span class="sxs-lookup"><span data-stu-id="8b166-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="8b166-209">Este sinalizador não é definido durante a replicação por RPC/IP entre sites.</span><span class="sxs-lookup"><span data-stu-id="8b166-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="8b166-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ Sincronização de n º de REPL do \_ \_ \_ tipo \_** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="8b166-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-211">Se definido, indica que quando a replicação de entrada é concluída, o servidor de destino deve informar ao servidor de origem para sincronizar na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="8b166-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="8b166-212">Este recurso é usado em cenários de conexão discada em que apenas um dos dois servidores pode iniciar uma conexão discada.</span><span class="sxs-lookup"><span data-stu-id="8b166-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="8b166-213">Por exemplo, essa opção pode ser usada em uma matriz corporativa e filial, em que a filial se conecta à sede corporativa pela Internet por meio de uma conexão de ISP dial-up.</span><span class="sxs-lookup"><span data-stu-id="8b166-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="8b166-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ Os \_ \_ objetos do \_ objeto \_ de retorno do replm** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="8b166-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-215">Este vizinho está em um estado em que ele retorna objetos pai antes de objetos filho.</span><span class="sxs-lookup"><span data-stu-id="8b166-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="8b166-216">Ele entra neste estado depois de receber um objeto filho antes de seu pai.</span><span class="sxs-lookup"><span data-stu-id="8b166-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="8b166-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ \_ \_ Sincronização completa de repl n \_ \_ em \_ andamento** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="8b166-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-218">O servidor de destino está executando uma sincronização completa do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="8b166-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="8b166-219">As sincronizações completas não usam vetores que criam atualizações (como [**\_ \_ cursores de repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) para filtrar atualizações.</span><span class="sxs-lookup"><span data-stu-id="8b166-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="8b166-220">As sincronizações completas não são usadas como parte do protocolo de replicação padrão.</span><span class="sxs-lookup"><span data-stu-id="8b166-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="8b166-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ \_ \_ \_ \_ Próximo \_ pacote da sincronização completa do repl n** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8b166-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-222">O último pacote da origem indicou uma modificação de um objeto que o servidor de destino ainda não criou.</span><span class="sxs-lookup"><span data-stu-id="8b166-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="8b166-223">O próximo pacote a ser solicitado instrui o servidor de origem a colocar todos os atributos do objeto modificado no pacote.</span><span class="sxs-lookup"><span data-stu-id="8b166-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="8b166-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ O \_ n º de repl \_ nunca foi \_ sincronizado** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="8b166-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-225">Uma sincronização nunca foi concluída com êxito por meio desta fonte.</span><span class="sxs-lookup"><span data-stu-id="8b166-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="8b166-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ O \_ n \_ º de repl foi preempção** (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-227">O mecanismo de replicação interrompeu temporariamente o processamento desse vizinho para atender a outro vizinho de prioridade mais alta, seja para esta partição ou para outra partição.</span><span class="sxs-lookup"><span data-stu-id="8b166-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="8b166-228">O mecanismo de replicação retomará o processamento deste vizinho após a conclusão do trabalho de maior prioridade.</span><span class="sxs-lookup"><span data-stu-id="8b166-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="8b166-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ n \_ ignorar \_ \_ notificações de alteração** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-230">Esse vizinho é definido para desabilitar sincronizações baseadas em notificação.</span><span class="sxs-lookup"><span data-stu-id="8b166-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="8b166-231">Em um site, os controladores de domínio sincronizam-se entre si com base nas notificações quando ocorrem alterações.</span><span class="sxs-lookup"><span data-stu-id="8b166-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="8b166-232">Essa configuração impede que esse vizinho execute sincronizações disparadas por notificações.</span><span class="sxs-lookup"><span data-stu-id="8b166-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="8b166-233">O vizinho ainda fará sincronizações com base em seu agendamento ou em resposta a sincronizações solicitadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="8b166-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="8b166-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ n \_ desabilitar \_ \_ sincronização agendada** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-235">Esse vizinho é definido para não executar sincronizações com base em sua agenda.</span><span class="sxs-lookup"><span data-stu-id="8b166-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="8b166-236">A única maneira que esse vizinho executará sincronizações é em resposta a notificações de alteração ou a sincronizações solicitadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="8b166-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="8b166-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ \_ \_ \_ Alterações de compactação de repl** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-238">As alterações recebidas dessa fonte devem ser compactadas.</span><span class="sxs-lookup"><span data-stu-id="8b166-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="8b166-239">A compactação geralmente ocorrerá somente se o servidor de origem estiver em um site diferente.</span><span class="sxs-lookup"><span data-stu-id="8b166-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="8b166-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ n º de \_ \_ \_ notificações de alteração** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-241">Nenhuma notificação de alteração deve ser recebida desta fonte.</span><span class="sxs-lookup"><span data-stu-id="8b166-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="8b166-242">Em geral, defina somente se o servidor de origem estiver em um site diferente.</span><span class="sxs-lookup"><span data-stu-id="8b166-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="8b166-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ \_Conjunto de \_ \_ atributos \_ parciais repl** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="8b166-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="8b166-244">Este vizinho está em um estado em que ele está recriando o conteúdo desta réplica devido a uma alteração no conjunto de atributos parciais.</span><span class="sxs-lookup"><span data-stu-id="8b166-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b166-245">**SourceDsaAddress**</span><span class="sxs-lookup"><span data-stu-id="8b166-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-248">Obtém o endereço DNS do DC de origem.</span><span class="sxs-lookup"><span data-stu-id="8b166-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="8b166-249">Essa cadeia de caracteres contém um GUID modificado, não o nome DNS canônico comumente usado.</span><span class="sxs-lookup"><span data-stu-id="8b166-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b166-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="8b166-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-253">Obtém o componente de caminho do objeto para o DSA que representa o DC de origem.</span><span class="sxs-lookup"><span data-stu-id="8b166-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="8b166-254">Essa cadeia de caracteres geralmente é semelhante ao nome do computador, mas nem sempre é idêntica.</span><span class="sxs-lookup"><span data-stu-id="8b166-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-255">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="8b166-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-258">Obtém o caminho X. 500 para o DSA que representa o DC de origem.</span><span class="sxs-lookup"><span data-stu-id="8b166-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-259">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="8b166-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-262">Obtém a ID de invocação usada pelo servidor de origem a partir da última replicação.</span><span class="sxs-lookup"><span data-stu-id="8b166-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-263">**SourceDsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="8b166-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b166-266">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b166-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b166-267">Obtém o GUID para o DSA (agente de serviço de diretório) que representa o controlador de domínio de origem (DC).</span><span class="sxs-lookup"><span data-stu-id="8b166-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="8b166-268">**SourceDsaSite**</span><span class="sxs-lookup"><span data-stu-id="8b166-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b166-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-271">Obtém o site que contém o controlador de domínio de origem.</span><span class="sxs-lookup"><span data-stu-id="8b166-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-272">**SyncOnStartup**</span><span class="sxs-lookup"><span data-stu-id="8b166-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-273">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-275">Obtém o valor que indica se o **sinalizador \_ DS \_ repl \_ Sync \_ no \_ início** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-276">**TimeOfLastSyncAttempt**</span><span class="sxs-lookup"><span data-stu-id="8b166-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-277">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b166-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-279">Obtém o carimbo de data/hora da última tentativa de replicação.</span><span class="sxs-lookup"><span data-stu-id="8b166-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="8b166-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-281">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b166-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-283">Obtém o carimbo de data/hora da última tentativa de replicação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8b166-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-284">**TwoWaySync**</span><span class="sxs-lookup"><span data-stu-id="8b166-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-285">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-287">Obtém o valor que indica se o sinalizador de **\_ sincronização do tipo DS repl de \_ \_ duas \_ vias \_** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-288">**UseAsyncIntersiteTransport**</span><span class="sxs-lookup"><span data-stu-id="8b166-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-291">Obtém o valor que indica se o sinalizador de **transporte entre sites do DS \_ repl \_ \_ use \_ \_ \_** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-292">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="8b166-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-293">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b166-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-295">Obtém o valor da propriedade **USNLastObjChangeSynced** no final do último ciclo de replicação concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="8b166-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="8b166-296">Zero se não houvesse nenhum ciclo de replicação concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="8b166-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-297">**USNLastObjChangeSynced**</span><span class="sxs-lookup"><span data-stu-id="8b166-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-298">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b166-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-300">Obtém o valor do atributo [**inalterado**](/windows/desktop/ADSchema/a-usnchanged) da última atualização de objeto recebida.</span><span class="sxs-lookup"><span data-stu-id="8b166-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="8b166-301">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="8b166-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b166-302">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b166-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b166-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b166-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b166-304">Obtém o valor que indica se o **sinalizador \_ gravável do DS repl \_ n \_** foi definido na propriedade **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="8b166-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b166-305">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b166-305">Requirements</span></span>



| <span data-ttu-id="8b166-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b166-306">Requirement</span></span> | <span data-ttu-id="8b166-307">Valor</span><span class="sxs-lookup"><span data-stu-id="8b166-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b166-308">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b166-308">Minimum supported client</span></span><br/> | <span data-ttu-id="8b166-309">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b166-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8b166-310">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b166-310">Minimum supported server</span></span><br/> | <span data-ttu-id="8b166-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b166-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b166-312">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b166-312">Namespace</span></span><br/>                | <span data-ttu-id="8b166-313">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="8b166-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="8b166-314">MOF</span><span class="sxs-lookup"><span data-stu-id="8b166-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b166-315"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b166-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b166-316">DLL</span><span class="sxs-lookup"><span data-stu-id="8b166-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b166-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b166-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

