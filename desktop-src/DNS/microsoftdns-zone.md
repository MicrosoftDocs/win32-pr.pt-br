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
# <a name="microsoftdns_zone-class"></a>\_Classe de zona MicrosoftDNS

> [!NOTE]
> Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais. Quando o termo for removido do software, também o removeremos deste artigo.

> [!NOTE]
> Este artigo contém referências ao termo servidor mestre, um termo que a Microsoft não usa mais. Quando o termo for removido do software, também o removeremos deste artigo.

A classe de **\_ zona MicrosoftDNS** descreve uma zona DNS. Cada instância da classe **de \_ zona MicrosoftDNS** deve ser atribuída a exatamente um servidor DNS. As zonas podem ser associadas a várias instâncias [**do \_ domínio MicrosoftDNS**](microsoftdns-domain.md) ou classes [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe de **\_ zona MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ zona MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Habilita a expiração para alguns ou todos os registros não NS e não SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Altera os tipos de zona. <br/> Qualificadores: implementados<br/>                                                                                                                                         |
| **Createzone**           | Cria uma nova zona. <br/> Qualificadores: nenhum.<br/>                                                                                                                                               |
| **ForceRefresh**         | Força uma atualização do secundário do servidor DNS mestre. <br/> Qualificadores: implementados<br/>                                                                                               |
| **Getdistinguiname** | Obtém o nome distinto do DS para a zona. <br/> Qualificadores: implementados<br/>                                                                                                                 |
| **PauseZone**            | Pausa a zona. <br/> Qualificadores: implementados<br/>                                                                                                                                            |
| **ReloadZone**           | Recarrega a zona. <br/> Qualificadores: implementados<br/>                                                                                                                                           |
| **ResetSecondaries**     | Redefine a matriz de endereço IP secundário. <br/> Qualificadores: implementados<br/>                                                                                                                      |
| **ResumeZone**           | Retoma a zona. <br/> Qualificadores: implementados<br/>                                                                                                                                           |
| **UpdateFromDS**         | Força uma atualização da zona do serviço de diretório (DS). Para que esse método seja válido, o Zonetype deve ser 0. na verdade, a zona deve ser armazenada no DS. <br/> Qualificadores: implementados<br/> |
| **WriteBackZone**        | Salva dados de zona em seu arquivo de zona. <br/> Qualificadores: implementados, estáticos<br/>                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A classe de **\_ zona MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Estágios**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o comportamento de expiração e eliminação da zona. Zero indica que a limpeza está desabilitada. Quando a eliminação está desabilitada, os carimbos de data/hora dos registros na zona não são atualizados e os registros não estão sujeitos à eliminação. Quando definido como um, os registros estão sujeitos à eliminação e seus carimbos de data/hora são atualizados quando o servidor recebe a solicitação de atualização dinâmica para os registros. Para zonas integradas Active Directory, esse valor é definido como a propriedade *Defaultenvelhecimentostate* do servidor DNS onde a zona é criada. Para zonas primárias padrão, o valor padrão é zero.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona aceita solicitações de atualização dinâmica.

</dd> <dt>

**Criado automaticamente**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona é criada.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a hora em que o servidor pode tentar eliminar a zona. Mesmo que a zona esteja configurada para habilitar a eliminação, o servidor DNS não tentará recuperar essa zona até esse momento. Esse valor é definido como a hora atual mais o intervalo de atualização da zona sempre que a zona é carregada. Esse parâmetro é armazenado localmente e não é replicado para outras cópias da zona.

</dd> <dt>

**Arquivo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o nome do arquivo de zona.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o registro WINS é replicado. Se definido como TRUE, a replicação do registro WINS será desabilitada.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se a zona é integrada ao DS.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o DNS usa recursão ao resolver os nomes para a zona de encaminhamento especificada. Aplicável somente a zonas de encaminhamento condicionais.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o tempo, em segundos, que um servidor DNS que encaminha uma consulta para o nome na zona de encaminhamento aguarda a resolução do encaminhador antes de tentar resolver a consulta em si. Esse parâmetro é aplicável somente às zonas de encaminhamento.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde a última verificação do número de série SOA da zona.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde que a zona foi transferida pela última vez de um servidor mestre.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereços IP locais dos servidores DNS mestre para esta zona. Se definido, esses mestres ultrapassarão o MasterServers encontrado em Active Directory.

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereços IP dos servidores DNS mestre para esta zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o intervalo de tempo entre a última atualização do carimbo de data/hora de um registro e o primeiro momento em que o carimbo de data/hora pode ser atualizado.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona mestra notifica os secundários de quaisquer alterações em seu banco de dados RRs. Defina como 1 para notificar secundários.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres que enumeram endereços IP de servidores DNS para serem notificados sobre alterações nessa zona.

</dd> <dt>

**Em pausa**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona está pausada.

</dd> <dt>

**Intervalo de atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o intervalo de atualização durante o qual os registros com carimbo de data/hora diferente devem ser atualizados para permanecer na zona. Os registros que não foram atualizados pela expiração do intervalo de atualização podem ser removidos pela próxima limpeza executada por um servidor. Esse valor nunca deve ser menor do que o período de atualização mais longo dos registros registrados na zona. Valores muito pequenos podem levar à remoção de registros DNS válidos. valores muito grandes prolongam o tempo de vida dos registros obsoletos. Esse valor é definido como a propriedade *DefaultRefreshInterval* do servidor DNS onde a zona é criada.

</dd> <dt>

**Ordem**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona é inversa (TRUE) ou Forward (FALSE).

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres que enumera a lista de endereços IP de servidores DNS que têm permissão para executar a eliminação de registros obsoletos dessa zona. Se a lista não for especificada, qualquer servidor DNS primário autoritativo para a zona poderá eliminar a zona quando outros pré-requisitos forem atendidos.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres que enumeram endereços IP de servidores DNS com permissão para receber essa zona por meio da replicação de zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a transferência de zona é permitida apenas para secundários designados. Os secundários designados são servidores DNS cujos endereços IP são listados em SecondariesIPAddressesArray.

</dd> <dt>

**Desligamento**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a cópia da zona expirou. Se for TRUE, a zona expirará ou será desligada.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Esse booliano indica se a zona usa a pesquisa inversa do NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a zona usa a pesquisa WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o tipo da zona. Os valores válidos são:

-   Integrado ao DS
-   Primária
-   Secundário

* * Windows Server 2003: * *

Valores adicionais:

-   Cache
-   Gerenciador
-   Encaminhador de

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Domínio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método createzone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





