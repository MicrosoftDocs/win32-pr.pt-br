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
# <a name="microsoftdns_server-class"></a>\_Classe de servidor MicrosoftDNS

A classe de **\_ servidor MicrosoftDNS** descreve um servidor DNS. Cada instância dessa classe pode ser associada a uma instância do [**\_ cache MicrosoftDNS**](microsoftdns-cache.md), uma instância de [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)e várias instâncias da [**\_ zona MicrosoftDNS**](microsoftdns-zone.md).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe de **\_ servidor MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ servidor MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **Getdistinguiname** | Recupera o nome distinto do DNS para a zona.<br/>                        |
| **StartScavenging**      | Inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.<br/> |
| **StartService**         | Inicia o servidor DNS.<br/>                                                |
| **StopService**          | Interrompe o servidor DNS.<br/>                                                 |



 

### <a name="properties"></a>Propriedades

A classe de **\_ servidor MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número máximo de registros de host retornados em resposta a uma solicitação de endereço. Os valores entre 5 e 28 são válidos.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o servidor DNS aceita solicitações de atualização dinâmica. Os valores válidos são como mostrado na tabela a seguir.



| Valor                                                                                                | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Sem restrições.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Não permite atualizações dinâmicas de registros SOA.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Não permite atualizações dinâmicas de registros NS na raiz da zona.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Não permite atualizações dinâmicas de registros NS que não estejam na raiz da zona (registros NS de delegação).<br/> |



 

Some esses valores para determinar o valor da configuração.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS tenta atualizar suas entradas de cache usando dados de servidores raiz. Quando um servidor DNS é inicializado, ele precisa de uma lista de NS ' dicas ' do servidor raiz e registros a para os servidores, historicamente chamados de arquivo de cache. Os servidores DNS da Microsoft têm um recurso que permite que eles tentem gravar um novo arquivo de cache com base nas respostas dos servidores raiz.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica quais zonas primárias padrão que são autoritativas para o nome do servidor DNS devem ser atualizadas quando o servidor de nomes for alterado. Estes são os valores válidos:



| Valor                                                                                                | Significado                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Somente servidores que permitem atualizações dinâmicas.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Somente servidores que não permitem atualizações dinâmicas.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Todos os servidores.<br/>                                    |



 

O valor padrão é 1.

* * Windows Server 2003: * *

O número 3 representa todos os servidores.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Determina o formato de mensagem AXFR ao enviar para secundários de servidor DNS não Microsoft. Quando definido como TRUE, o servidor DNS envia transferências para secundários do servidor DNS não Microsoft no formato descompactado. Quando for falso, todas as transferências serão enviadas no formato rápido.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Método de inicialização para o servidor DNS. Os valores válidos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Não inicializado.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Inicialize do arquivo.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Inicializar do registro.<br/>               |
| <span id="3"></span><dl> <dt>**Beta**</dt> </dl> | Inicialize do diretório e do registro.<br/> |



 

</dd> <dt>

**Defaultenvelhecimentostate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Valor de **ScavengingInterval** padrão definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS. O valor padrão é zero, indicando que a limpeza está desabilitada.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo sem atualização, em horas, definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS. O valor padrão é 168 horas (sete dias).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo de atualização, em horas, definido para todas as zonas integradas ao Active Directory criadas neste servidor DNS. O valor padrão é 168 horas (sete dias).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS cria automaticamente zonas de pesquisa inversa padrão.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se a associação de porta padrão para um soquete usado para enviar consultas para servidores DNS remotos pode ser substituída.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se há um DS disponível no servidor DNS.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo, em segundos, para sondar as zonas integradas ao DS.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo de vida dos registros marcados para exclusão nas zonas integradas do serviço de diretório, expresso em segundos.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo de vida, em segundos, das informações armazenadas em cache que descrevem a versão do EDNS com suporte de outros servidores DNS.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o suporte para partições de diretório de aplicativo está habilitado no servidor DNS.

* * Windows Server 2003: * *

Esse método é denominado EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o servidor DNS inclui RRs específicos do DNSSEC, chave, SIG e NXT em uma resposta, de acordo com a tabela a seguir:



| Valor                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum registro DNSSEC é incluído na resposta, a menos que a consulta solicitou um conjunto de registros de recursos do tipo de registro DNSSEC.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Os registros DNSSEC são incluídos na resposta de acordo com a RFC 2535.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Os registros DNSSEC são incluídos em uma resposta somente se a consulta do cliente original contivesse o registro de recurso OPT de acordo com a RFC 2671<br/> |



 

Se uma consulta solicitar um conjunto de registros de recursos do tipo DNSSEC, o servidor DNS sempre responderá com esses registros, se disponível.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o comportamento do servidor DNS. Quando TRUE, o servidor DNS sempre responde com registros de recursos OPCIONais de acordo com a RFC 2671, a menos que o servidor remoto tenha indicado que ele não oferece suporte ao EDNS em um Exchange anterior. Se for FALSE, o servidor DNS responderá a consultas com optas somente se as optas forem enviadas na consulta original.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica quais eventos o servidor DNS registra no log do sistema Visualizador de Eventos. Os valores a seguir são usados.



| Valor                                                                                                | Significado                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Registrar apenas erros.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Registrar somente avisos e erros.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Registrar todos os eventos.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se as consultas a subzonas delegadas são encaminhadas.

</dd> <dt>

**Encaminhadores**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Enumera a lista de endereços IP de encaminhadores para os quais o servidor DNS encaminha consultas.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo, em segundos, um servidor DNS que encaminha uma consulta aguardará a resolução do [*encaminhador*](f-gly.md) antes de tentar resolver a consulta em si.

Esse valor será inútil se o servidor de encaminhamento não estiver definido para usar recursão. Para determinar isso, verifique a propriedade booliana do isslave.

</dd> <dt>

**Isslave**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**True** se o servidor DNS não usar recursão quando a resolução de nomes por meio de encaminhadores falhar.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Enumera a lista de endereços IP nos quais o servidor DNS pode receber consultas.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS fornece prioridade para o endereço de rede local ao retornar registros A.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tamanho do log de depuração do servidor DNS, em bytes.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome do arquivo e caminho para o log de depuração do servidor DNS. O padrão é% system32% \\ DNS \\ DNS. log. Os caminhos relativos são relativos a% SystemRoot% \\ System32. Caminhos absolutos podem ser usados, mas não há suporte para caminhos UNC.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Lista de endereços IP usados para filtrar eventos DNS gravados no log de depuração.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica quais políticas são ativadas no log do sistema Visualizador de Eventos.

Deve ser definido como valores específicos com base no seguinte algoritmo: cada política (a ser ativada no log do sistema Visualizador de Eventos) recebe um valor específico.



| Valor                                                                                                                  | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Consultá.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Sobre.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Update.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Transações não consulta.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Perguntas.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Respectivas.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Enviar.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Recebe.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | UDP.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Todos os pacotes.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | Transação de gravação do serviço de diretório do NT.<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | Transação de atualização do serviço de diretório do NT.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Pacotes completos.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Gravação.<br/>                           |



 

A soma dos valores correspondentes a todas as políticas a serem ativadas é indicada nesta propriedade.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS executa curingas flexíveis. Se for indefinido ou zero, o servidor seguirá o comportamento curinga especificado na RFC do DNS. Nesse caso, é aconselhável que um administrador inclua registros MX para todos os hosts que não têm capacidade de receber emails. Se for diferente de zero, o servidor buscará o nó curinga mais próximo; Nesse caso, um administrador deve colocar os registros MX na raiz da zona e em um nó curinga (' \* ') diretamente abaixo da raiz da zona. Além disso, os administradores devem colocar os registros MX de referência automática em hosts que recebem seus próprios emails.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo máximo, em segundos, o registro de uma consulta de nome recursivo pode permanecer no cache do servidor DNS. O servidor DNS exclui registros do cache quando o valor dessa entrada expira, mesmo que o valor do campo TTL no registro seja maior.

O valor padrão dessa propriedade é 86.400 segundos (1 dia).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo máximo, em segundos, um resultado de erro de nome de uma consulta recursiva pode permanecer no cache do servidor DNS. O DNS exclui registros do cache quando esse temporizador expira, mesmo que o campo TTL seja maior. O valor padrão é 86.400 (um dia).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN (nome de domínio totalmente qualificado) ou endereço IP do servidor DNS.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica o conjunto de caracteres qualificados a ser usado em nomes DNS. Os valores a seguir são usados.



| Valor                                                                                                | Significado                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | RFC estrito (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Não RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**Beta**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

* * Windows Server 2003: * *

Um valor de "2" indica "any".

</dd> <dt>

**Recursão**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS executa Pesquisas recursivas. VERDADEIRO indica que as pesquisas recursivas não são executadas.

</dd> <dt>

**RecursionRetry**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Segundos decorridos antes de tentar novamente uma pesquisa recursiva. Se a propriedade for indefinida ou zero, as novas tentativas serão feitas após três segundos. Os usuários não são incentivados de alterar essa propriedade. Há certas situações em que a propriedade deve ser alterada; um exemplo é quando o servidor DNS entra em contato com servidores remotos por um link lento e o servidor DNS está tentando novamente antes de receber a resposta do DNS remoto. Nesse caso, aumentar o tempo para ser um pouco mais longo do que o tempo de resposta observado do DNS remoto seria razoável.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Segundos decorridos antes que o servidor DNS forneça uma consulta recursiva. Se a propriedade for indefinida ou zero, o servidor DNS será disponibilizado após 15 segundos. Em geral, o tempo limite de 15 segundos é suficiente para permitir que qualquer resposta pendente volte ao servidor DNS.

Os usuários não são incentivados de alterar essa propriedade. Um cenário em que a propriedade deve ser alterada é quando o servidor DNS entra em contato com servidores remotos por um link lento, e o servidor DNS observa a rejeição de consultas (com falha do servidor \_ ) antes que as respostas sejam recebidas.

Os resolvedores de cliente também tentam consultas novamente, portanto, uma investigação cuidadosa é necessária para determinar se as respostas remotas estão realmente associadas à consulta que atingiu o tempo limite. Nesse caso, elevar o valor de tempo limite para ser um pouco mais longo do que o tempo de resposta observado do DNS remoto seria razoável.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS arredondado Robin vários registros A.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Protocolo RPC ou protocolos sobre os quais o RPC administrativo é executado. O algoritmo a seguir é usado para atribuir um valor específico:



| Valor                                                                                                | Significado                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhuma<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Pipes nomeados<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | LPC<br/>         |



 

A soma dos valores indica os protocolos usados.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo, em horas, entre duas operações de eliminação consecutivas executadas pelo servidor DNS. Zero indica que a limpeza está desabilitada. O valor padrão é 168 horas (sete dias).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS salva exclusivamente os registros de nomes na mesma subárvore que o servidor que os forneceu.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Porta na qual o servidor DNS envia consultas UDP para outros servidores. Por padrão, o servidor DNS envia consultas em um soquete associado à porta DNS.

Em determinadas situações, essa não é a melhor configuração. Um caso óbvio é quando um administrador bloqueia a porta DNS com um firewall para impedir o acesso externo ao servidor DNS, mas ainda quer que o servidor seja capaz de contatar os servidores DNS da Internet para fornecer resolução de nomes para clientes internos. Outro caso é quando o servidor DNS oferece suporte a redes não atendidas (a propriedade **DisjointNets** definida como true identifica esse cenário). Nesses casos, definir a propriedade **SendOnNonDnsPort** como um valor diferente de zero direciona o servidor DNS para se associar a uma porta arbitrária para enviar para servidores DNS remotos.

Se o valor de **SendOnNonDnsPort** for maior que 1024, o servidor DNS será associado explicitamente ao valor de porta fornecido. Essa opção de configuração é útil quando um administrador precisa corrigir a porta de consulta DNS para fins de firewall.

* * Windows Server 2003: * *

Definir a propriedade SendPort como um valor diferente de zero faz com que o servidor DNS se vincule a uma porta arbitrária para enviar para servidores DNS remotos.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Enumera a lista de endereços IP para o servidor DNS.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o servidor DNS analisa os [*arquivos de zona*](z-gly.md) estritamente. Se for indefinido ou igual a zero, o servidor registrará e ignorará dados inválidos no arquivo de zona e continuará a carregar. Se for diferente de zero, o servidor fará o log e falhará em erros de arquivo de zona.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Restringe o tipo de registro que pode ser atualizado dinamicamente no servidor, usado além das configurações de **AllowUpdate** em objetos de servidor e de zona.

* * Windows Server 2003: * *

0: sem restrições.

1: não permitir atualizações dinâmicas de registros SOA.

2: não permitir atualizações dinâmicas de registros NS na raiz da zona.

4: não permitir atualizações dinâmicas de registros NS não na raiz da zona (registros NS de delegação).

Some esses valores para determinar o valor da configuração.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do servidor DNS.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o servidor DNS grava os registros NS e SOA na seção autoridade sobre uma resposta bem-sucedida.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Tempo, em segundos, o servidor DNS aguarda uma conexão TCP bem-sucedida para um servidor remoto ao tentar uma transferência de zona.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Método StartService da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StopService da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





