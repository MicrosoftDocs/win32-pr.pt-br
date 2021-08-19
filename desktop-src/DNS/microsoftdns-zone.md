---
title: MicrosoftDNS_Zone classe
description: A classe Zona MicrosoftDNS \_ descreve uma Zona DNS. Cada instância da classe Zona MicrosoftDNS \_ deve ser atribuída a exatamente um servidor DNS. As zonas podem ser associadas a várias instâncias das classes \_ MicrosoftDNS Domain ou MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- dns MicrosoftDNS_Zone classe
- MicrosoftDNS_Zone classe DNS , descrita
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
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957175"
---
# <a name="microsoftdns_zone-class"></a>Classe Zona \_ MicrosoftDNS

> [!NOTE]
> Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais. Quando o termo for removido do software, também o removeremos deste artigo.

> [!NOTE]
> Este artigo contém referências ao termo servidor mestre, um termo que a Microsoft não usa mais. Quando o termo for removido do software, também o removeremos deste artigo.

A **classe \_ Zona MicrosoftDNS** descreve uma Zona DNS. Cada instância da classe **Zona MicrosoftDNS \_** deve ser atribuída a exatamente um servidor DNS. As zonas podem ser associadas a várias instâncias das classes [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) ou [**MicrosoftDNS \_ ResourceRecord.**](microsoftdns-resourcerecord.md)

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

A **classe \_ Zona MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Zona MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Habilita o tempo de vida para alguns ou todos os registros não NS e não SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Altera os tipos de zona. <br/> Qualificadores: implementados<br/>                                                                                                                                         |
| **CreateZone**           | Cria uma nova zona. <br/> Qualificadores: Nenhum.<br/>                                                                                                                                               |
| **ForceRefresh**         | Força uma atualização do secundário do Servidor DNS Mestre. <br/> Qualificadores: implementados<br/>                                                                                               |
| **GetDistinguishedName** | Obtém o nome diferenciado de DS para a zona. <br/> Qualificadores: implementados<br/>                                                                                                                 |
| **PauseZone**            | Pausa a Zona. <br/> Qualificadores: implementados<br/>                                                                                                                                            |
| **ReloadZone**           | Recarrega a Zona. <br/> Qualificadores: implementados<br/>                                                                                                                                           |
| **ResetSecondaries**     | Redefine a matriz de endereços IP secundários. <br/> Qualificadores: implementados<br/>                                                                                                                      |
| **ResumeZone**           | Retoma a Zona. <br/> Qualificadores: implementados<br/>                                                                                                                                           |
| **UpdateFromDS**         | Força uma atualização da Zona do DS (Serviço de Diretório). Para que esse método seja válido, ZoneType deve ser 0, a zona deve ser realmente armazenada no DS. <br/> Qualificadores: implementados<br/> |
| **WriteBackZone**        | Salva dados de zona em seu arquivo de zona. <br/> Qualificadores: implementados, estáticos<br/>                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A **classe \_ Zona MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Envelhecimento**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o comportamento de idade e limpeza da zona. Zero indica que a limpeza está desabilitada. Quando a limpeza é desabilitada, os tempos de registro na zona não são atualizados e os registros não são sujeitos à limpeza. Quando definido como um, os registros são sujeitos a desaloques e seus tempos de data/hora são atualizados quando o servidor recebe a solicitação de atualização dinâmica para os registros. Para zonas integradas ao Active Directory, esse valor é definido como a *propriedade DefaultAgingState* do Servidor DNS em que a zona é criada. Para zonas primárias padrão, o valor padrão é zero.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona aceita solicitações de atualização dinâmicas.

</dd> <dt>

**AutoCreated**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona é automaticamentecriada.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a hora em que o servidor pode tentar limpar a zona. Mesmo que a zona seja configurada para habilitar a eliminação de problemas, o servidor DNS não tentará limpar essa zona até depois desse momento. Esse valor é definido como a hora atual mais o Intervalo de Atualização da zona sempre que a zona é carregada. Esse parâmetro é armazenado localmente e não é replicado para outras cópias da zona.

</dd> <dt>

**Datafile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o nome do arquivo de zona.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o registro WINS é replicado. Se definido como TRUE, a replicação de registro WINS será desabilitada.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se a zona é integrada a DS.

</dd> <dt>

**Forwarder Ltda**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o DNS usa recursão ao resolver os nomes para a zona de encaminhamento especificada. Aplicável somente a zonas de encaminhamento condicional.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o tempo, em segundos, que um servidor DNS que encaminha uma consulta para o nome na zona de encaminhamento aguarda a resolução do encaminhador antes de tentar resolver a consulta em si. Esse parâmetro é aplicável somente às zonas de encaminhamento.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde que o número de série SOA da zona foi verificado pela última vez.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de segundos desde o início de 1º de janeiro de 1970 GMT, desde que a zona foi transferida pela última vez de um servidor mestre.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereços IP locais dos servidores DNS mestres para essa zona. Se definidos, esses mestres superam os MasterServers encontrados no Active Directory.

</dd> <dt>

**Masterservers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereços IP dos servidores DNS mestres para essa zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o intervalo de tempo entre a última atualização do timestamp de um registro e o momento mais antigo em que o timestamp pode ser atualizado.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona mestra notifica os secundários de quaisquer alterações em seu banco de dados RRs. De definido como 1 para notificar secundários.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres enumerando endereços IP de servidores DNS a serem notificados sobre alterações nessa zona.

</dd> <dt>

**Em pausa**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona está em pausa.

</dd> <dt>

**Intervalo de atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o intervalo de atualização, durante o qual os registros com o timestamp não zero devem ser atualizados para permanecerem na zona. Os registros que não foram atualizados pela expiração do intervalo de atualização podem ser removidos pela próxima eliminação executada por um servidor. Esse valor nunca deve ser menor que o período de atualização mais longo dos registros registrados na zona. Valores muito pequenos podem levar à remoção de registros DNS válidos. valores muito grandes duram o tempo de vida de registros antigos. Esse valor é definido como a *propriedade DefaultRefreshInterval* do servidor DNS em que a zona é criada.

</dd> <dt>

**Reverter**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona é inversa (TRUE) ou avançar (FALSE).

</dd> <dt>

**DesemãoServidores**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres que enumera a lista de endereços IP de servidores DNS que têm permissão para executar a eliminação de registros antigos dessa zona. Se a lista não for especificada, qualquer servidor DNS primário autoritativo para a zona poderá limpar a zona quando outros pré-requisitos são atendidos.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeias de caracteres enumerando endereços IP de servidores DNS com permissão para receber essa zona por meio da replicação de zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a transferência de zona tem permissão apenas para secundárias designadas. Os secundários designados são servidores DNS cujos endereços IP estão listados em SecondariesIPAddressesArray.

</dd> <dt>

**Desligamento**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a cópia da Zona expirou. Se TRUE, a Zona expirou ou será desligado.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Esse booliana indica se a Zona usa a pesquisa inversa NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a Zona usa a pesquisa WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o tipo da Zona. Os valores válidos são:

-   DS integrado
-   Primária
-   Secundário

**Windows Server 2003: **

Valores adicionais:

-   Cache
-   Esboço
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

 

 





