---
title: MSAD_ReplNeighbor classe
description: Representa a estrutura DS REPL NEIGHBOR, que contém as informações de estado de replicação de entrada para um determinado nc (contexto de nomenu) e \_ par de servidores de \_ origem.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor classe active directory
- MSAD_ReplNeighbor classe Active Directory , descrita
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
ms.openlocfilehash: 0598116413d34334e0610895a9c3b0629399fed8bb482e0d08cdae9cafb17fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025754"
---
# <a name="msad_replneighbor-class"></a>Classe MSAD \_ ReplNeighbor

Representa a [**estrutura DS \_ REPL \_ NEIGHBOR,**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) que contém as informações de estado de replicação de entrada para um determinado nc (contexto de nomenplicação) e par de servidores de origem, conforme retornado pela [**função DsReplicaGetInfo.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe MSAD \_ ReplNeighbor** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe MSAD \_ ReplNeighbor** tem esses métodos.



| Método                                                           | Descrição                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Sincroniza um contexto de nomeação de destino com uma de suas fontes.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe MSAD \_ ReplNeighbor** tem essas propriedades.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o caminho X.500 do objeto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) que corresponde ao transporte pelo qual a replicação é executada. Definido como **NULL para** replicação de RPC/IP.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o GUID do objeto de transporte entresite que corresponde à **propriedade AsyncIntersiteTransportDN.**

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ COMPRESS \_ CHANGES** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ DISABLE SCHEDULED \_ \_ SYNC** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**Domínio**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome canônico do domínio do NC replicado.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ DO SCHEDULED \_ \_ SYNCS** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **\_ DS REPL \_ NBR \_ FULL SYNC \_ IN \_ \_ PROGRESS** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ FULL SYNC \_ NEXT \_ \_ PACKET** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ IGNORE CHANGE \_ \_ NOTIFICATIONS** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se essa conexão representa um DC de origem que foi excluído. **TRUE** se essa conexão representar um DC de origem que foi excluído; caso contrário, **FALSE.** Por design, o DS continuará replicando essas conexões por algum tempo após a exclusão do DC de origem.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o **código de erro HRESULT** para a última tentativa de replicação.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o número de tentativas de replicação com falha consecutivas, não incluindo as conexões que devem falhar. Por exemplo, se a **propriedade IsDeletedSourceDsa** estiver definida como **TRUE,** ela deverá falhar.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o caminho X.500 para o NC que é replicado por essa conexão.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o GUID para o NC replicado.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ NEVER \_ SYNCED** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **\_ \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS do DS REPL** foi definido na propriedade **ReplicaFlags.**

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o número de tentativas de replicação com falha consecutivas.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o conjunto de sinalizadores que especificam atributos e opções para os dados de replicação. Essa propriedade pode ser zero ou uma combinação de um ou mais dos sinalizadores a seguir.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ NBR \_ WRITEABLE** (16 (0x10))


</dt> <dd>

A cópia local do contexto de nomenclatura é gravável.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ SINCRONIZAÇÃO \_ NBR \_ REPL \_ NA \_ INICIALIZAÇÃO** (32 (0x20))


</dt> <dd>

A replicação desse contexto de nomeação dessa origem é tentada quando o servidor de destino é inicializado. Esse sinalizador geralmente se aplica somente a vizinhos intra-site.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ SINCRONIZAÇÕES \_ AGENDADAS REPL NBR \_ DO \_ \_** (64 (0x40))


</dt> <dd>

Execute a replicação de acordo com um agendamento. Esse sinalizador geralmente é definido, a menos que o agendamento para esse contexto de nomentura ou origem seja "nunca", ou seja, o agendamento vazio.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ USE TRANSPORTE \_ INTERSITE ASSÍNCRONO \_ \_** (128 (0x80))


</dt> <dd>

Execute a replicação indiretamente por meio do Serviço de Mensagens Entre Sites. Este sinalizador é definido somente durante a replicação por SMTP. Este sinalizador não é definido durante a replicação por RPC/IP entre sites.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ REPL \_ NBR \_ TWO WAY \_ \_ SYNC** (512 (0x200))


</dt> <dd>

Se definido, indica que, quando a replicação de entrada for concluída, o servidor de destino deverá dizer ao servidor de origem para sincronizar na direção inversa. Este recurso é usado em cenários de conexão discada em que apenas um dos dois servidores pode iniciar uma conexão discada. Por exemplo, essa opção pode ser usada em uma sede corporativa e filial, em que a filial se conecta à sede corporativa pela Internet por meio de uma conexão isp discada.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ RETURN OBJECT \_ \_ PARENTS** (2048 (0x800))


</dt> <dd>

Este vizinho está em um estado em que ele retorna objetos pai antes de objetos filho. Ele entra neste estado depois de receber um objeto filho antes de seu pai.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ REPL \_ NBR \_ FULL SYNC \_ IN \_ \_ PROGRESS** (65536 (0x10000))


</dt> <dd>

O servidor de destino está executando uma sincronização completa do servidor de origem. As sincronizações completas não usam vetores que criam atualizações (como [**\_ \_ CURSORES DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) para filtrar atualizações. As sincronizações completas não são usadas como parte do protocolo de replicação padrão.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ REPL \_ NBR \_ FULL SYNC \_ NEXT \_ \_ PACKET** (131072 (0x20000))


</dt> <dd>

O último pacote da origem indicou uma modificação de um objeto que o servidor de destino ainda não criou. O próximo pacote a ser solicitado instrui o servidor de origem a colocar todos os atributos do objeto modificado no pacote.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ NEVER \_ SYNCED** (2097152 (0x200000))


</dt> <dd>

Uma sincronização nunca foi concluída com êxito por meio desta fonte.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ PREEMPTED** (16777216 (0x1000000))


</dt> <dd>

O mecanismo de replicação interrompeu temporariamente o processamento desse vizinho para atender a outro vizinho de prioridade mais alta, para essa partição ou para outra partição. O mecanismo de replicação retomará o processamento deste vizinho após a conclusão do trabalho de maior prioridade.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ IGNORE CHANGE \_ \_ NOTIFICATIONS** (67108864 (0x4000000))


</dt> <dd>

Esse vizinho está definido para desabilitar sincronizações baseadas em notificação. Em um site, os controladores de domínio sincronizam-se entre si com base nas notificações quando ocorrem alterações. Essa configuração impede que esse vizinho executa sincronizações disparadas por notificações. O vizinho ainda fará sincronizações com base em seu agendamento ou em resposta a sincronizações solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ DISABLE SCHEDULED \_ \_ SYNC** (134217728 (0x8000000))


</dt> <dd>

Esse vizinho está definido para não executar sincronizações com base em sua agenda. A única maneira que esse vizinho executará sincronizações é em resposta a notificações de alteração ou a sincronizações solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ REPL \_ NBR \_ COMPACTA \_ ALTERAÇÕES** (268435456 (0x10000000))


</dt> <dd>

As alterações recebidas dessa fonte devem ser compactadas. A compactação geralmente ocorre somente se o servidor de origem estiver em um site diferente.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS** (536870912 (0x20000000))


</dt> <dd>

Nenhuma notificação de alteração deve ser recebida desta fonte. Normalmente, de definido somente se o servidor de origem estiver em um site diferente.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ REPL \_ NBR \_ PARTIAL ATTRIBUTE \_ \_ SET** (1073741824 (0x40000000))


</dt> <dd>

Este vizinho está em um estado em que ele está recriando o conteúdo desta réplica devido a uma alteração no conjunto de atributos parciais.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o endereço DNS do DC de origem.

> [!Note]  
> Essa cadeia de caracteres contém um GUID modificado, não o nome DNS canônico comumente usado.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o componente de caminho do objeto para a DSA que representa o DC de origem. Essa cadeia de caracteres geralmente é semelhante ao nome do computador, mas nem sempre é idêntica.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o caminho X.500 para a DSA que representa o DC de origem.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a ID de invocação que foi usada pelo servidor de origem desde a última replicação.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o GUID do DSA (agente de serviço de diretório) que representa o controlador de domínio de origem (DC).

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o site que contém o DC de origem.

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **\_ DS REPL \_ NBR \_ SYNC ON \_ \_ STARTUP** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o timestamp para a última tentativa de replicação.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o data/hora da última tentativa de replicação bem-sucedida.

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **\_ DS REPL \_ NBR \_ TWO WAY \_ \_ SYNC** foi definido na **propriedade ReplicaFlags.**

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o sinalizador **DS \_ REPL \_ NBR \_ USE \_ ASYNC \_ INTERSITE \_ TRANSPORT** foi definido na propriedade **ReplicaFlags.**

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém **o valor da propriedade USNLastObjChangeSynced** no final do último ciclo de replicação concluído com êxito. Zero se não houver ciclos de replicação concluídos com êxito.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém [**o valor do**](/windows/desktop/ADSchema/a-usnchanged) atributo inalterado da última atualização de objeto recebida.

</dd> <dt>

**Gravável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o **sinalizador \_ gravável do DS repl \_ n \_** foi definido na propriedade **ReplicaFlags** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

