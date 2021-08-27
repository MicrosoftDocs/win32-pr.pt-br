---
description: Representa os atributos e comportamentos de um adaptador de rede. Essa classe inclui propriedades e métodos extras que dão suporte ao gerenciamento do protocolo TCP/IP que são independentes do adaptador de rede.
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
ms.openlocfilehash: aab5f52a3e8dbb910227eb91eb34c7d562a26ad7915f0d61b25d46c825c101a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958925"
---
# <a name="win32_networkadapterconfiguration-class"></a>\_Classe Win32 NetworkAdapterConfiguration

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterConfiguration do Win32** representa os atributos e comportamentos de um adaptador de rede. Essa classe inclui propriedades e métodos extras que dão suporte ao gerenciamento do protocolo TCP/IP que são independentes do adaptador de rede.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Win32 \_ NetworkAdapterConfiguration** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ NetworkAdapterConfiguration** tem esses métodos.



| Método                                                                                                                       | Descrição                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Desabilita o IPsec neste adaptador de rede habilitado para TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita o DHCP (protocolo de configuração dinâmica de hosts) para o serviço com este adaptador de rede.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Habilita o DNS (sistema de nomes de domínio) para o serviço neste adaptador de rede associado a TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Habilita o IPsec globalmente em todos os adaptadores de rede vinculados por IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Habilita o IPsec neste adaptador de rede específico habilitado para TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Habilita o endereçamento TCP/IP estático para o adaptador de rede de destino.<br/>                                                                           |
| [**EnableWINS ativa**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Habilita configurações do WINS específicas para TCP/IP, mas independente do adaptador de rede.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Libera o endereço IP associado a um adaptador de rede habilitado para DHCP específico.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Libera os endereços IP associados a todos os adaptadores de rede habilitados para DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Renova o endereço IP em adaptadores de rede habilitados para DHCP específicos.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Renova os endereços IP em todos os adaptadores de rede habilitados para DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Define a transmissão de consultas ARP pelo TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Permite que os pacotes Ethernet usem a codificação de ajuste 802,3.<br/>                                                                                       |
| [**DatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Define o caminho para os arquivos de banco de dados da Internet padrão (HOSTs, LMHOSTs, redes e protocolos).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita a detecção de gateway inativo.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsoleto. Esse método define o valor do tipo de serviço (TOS) padrão no cabeçalho dos pacotes de IP de saída.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Define o valor da TTL (vida útil) padrão no cabeçalho dos pacotes IP de saída.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Define o domínio DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Define a ordem de pesquisa do servidor como uma matriz de elementos.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Define a ordem de pesquisa de sufixo como uma matriz de elementos.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indica o registro DNS dinâmico de endereços IP para este adaptador associado a IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Especifica a quantidade de memória que o IP aloca para armazenar dados de pacote na fila de pacotes do roteador.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Especifica uma lista de gateways para os pacotes de roteamento destinados a uma sub-rede diferente daquela à qual esse adaptador está conectado.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Define a extensão à qual o sistema dá suporte a multicast de IP e participa do protocolo de gerenciamento de grupo da Internet.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Define a métrica de roteamento associada a este adaptador associado a IP.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Define o uso de difusão zero de IP.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | define os pares de número/quadro de rede IPX (Exchange de pacotes) para este adaptador de rede.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | define o número de rede virtual de Exchange de pacotes de rede (IPX) no sistema de computador de destino.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Define o intervalo que separa as retransmissões Keep Alive até que uma resposta seja recebida.<br/>                                                      |
| [**Setkeepalivetime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Define a frequência com que o TCP tenta verificar se uma conexão ociosa ainda está disponível enviando um pacote keep alive.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Define a MTU (unidade máxima de transmissão) padrão para uma interface de rede.<br/> Não há suporte para o método.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Define o número de cabeçalhos de pacotes IP alocados para a fila de pacotes do roteador.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Habilita a detecção de roteadores buraco negro.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Habilita a descoberta de MTU (unidade máxima de transmissão).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Define a operação padrão de NetBIOS sobre TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Define o número de tentativas que o TCP retransmitirá uma solicitação de conexão antes de abortar.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Define o número de vezes que o TCP retransmitirá um segmento de dados individual antes de abortar a conexão.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Define o número máximo de conexões que o TCP pode ter aberto simultaneamente.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Especifica se o TCP usa a especificação RFC 1122 para dados urgentes ou o modo usado pelos sistemas derivados do BSD (Berkeley Software Design).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Define o tamanho máximo da janela de recepção TCP oferecida pelo sistema.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | define os servidores WINS (Windows de Internet Serviço de Nomenclatura) primários e secundários neste adaptador de rede associado a TCP/IP.<br/>                        |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ NetworkAdapterConfiguration** tem essas propriedades.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

Se **verdadeiro**, o TCP/IP transmite consultas de ARP (protocolo de resolução de endereço) com o roteamento de origem habilitado em redes de token ring. Por padrão (FALSE), o ARP primeiro consulta sem roteamento de origem e, em seguida, tenta novamente com o roteamento de origem habilitado se nenhuma resposta for recebida. O roteamento de origem permite o roteamento de pacotes de rede entre diferentes tipos de redes.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

Se **for verdadeiro**, os pacotes de Ethernet seguem a codificação de snap (protocolo de acesso Sub-Network) do IEEE 802,3. Definir esse parâmetro como 1 força o TCP/IP a transmitir pacotes Ethernet usando a codificação de encaixe 802,3. Por padrão (FALSE), a pilha transmite pacotes no formato de Ethernet DIX.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet os \\ \\ \\ \\ \\ \\ parâmetros tcpip \| DatabasePath")
</dt> </dl>

caminho de arquivo de Windows válido para arquivos de banco de dados da Internet padrão (hosts, lmhosts, redes e protocolos). o caminho do arquivo é usado pela interface do Windows sockets.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

Se **for true**, ocorrerá a detecção de gateway inativo. Com esse recurso habilitado, o protocolo TCP solicita que o protocolo Internet (IP) mude para um gateway de backup se retransmitir um segmento várias vezes sem receber uma resposta.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ parâmetros de serviços \| \| DefaultGateway")
</dt> </dl>

Matriz de endereços IP de gateways padrão que o sistema de computador usa.

Exemplo: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Valor padrão de TOS (tipo de serviço) definido no cabeçalho dos pacotes de IP de saída. A RFC (solicitação de comentários) 791 define os valores. Padrão: 0 (zero), intervalo válido: 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTtl")
</dt> </dl>

Valor de TTL (vida útil) padrão definido no cabeçalho dos pacotes de IP de saída. O TTL especifica o número de roteadores que um pacote IP pode passar para alcançar seu destino antes de ser Descartado. Cada roteador diminui em uma contagem de TTL de um pacote à medida que ele passa e descarta os pacotes — se o TTL for 0 (zero). Padrão: 32, intervalo válido: 1-255.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Se **for true**, o servidor de protocolo DHCP atribuirá automaticamente um endereço IP ao sistema de computador ao estabelecer uma conexão de rede.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Data e hora de expiração de um endereço IP concedido que foi atribuído ao computador pelo servidor de protocolo DHCP.

Exemplo: 20521201000230, 0

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Data e hora em que a concessão foi obtida para o endereço IP atribuído ao computador pelo servidor DHCP (protocolo de configuração dinâmica de hosts).

Exemplo: 19521201000230, 0

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

Endereço IP do servidor de protocolo DHCP.

Exemplo: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Domain")
</dt> </dl>

Nome da organização seguido por um ponto e uma extensão que indica o tipo de organização, como "microsoft.com". O nome pode ser qualquer combinação das letras de a a Z, os numerais de 0 a 9 e o hífen (-), além do caractere de ponto (.) usado como separador.

Exemplo: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| SearchList")
</dt> </dl>

Matriz de sufixos de domínio DNS a serem acrescentados ao final dos nomes de host durante a resolução de nomes. Ao tentar resolver um FQDN (nome de domínio totalmente qualificado) de um nome somente de host, o sistema primeiro acrescentará o nome de domínio local. Se isso não for bem-sucedido, o sistema usará a lista de sufixos de domínio para criar FQDNs adicionais na ordem listada e consultar servidores DNS para cada um.

Exemplo: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS")
</dt> </dl>

Se **TRUE**, o DNS (Sistema de Nomes de Domínio) será habilitado para resolução de nomes Windows resolução wins (Internet Serviço de Nomenclatura). Se o nome não puder ser resolvido usando DNS, a solicitação de nome será encaminhada para WINS para resolução.

</dd> <dt>

**Dnshostname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname")
</dt> </dl>

Nome do host usado para identificar o computador local para autenticação por alguns utilitários. Outros utilitários baseados em TCP/IP podem usar esse valor para adquirir o nome do computador local. Os nomes de host são armazenados em servidores DNS em uma tabela que mapeia nomes para endereços IP para uso pelo DNS. O nome pode ser qualquer combinação das letras A a Z, dos numerais de 0 a 9 e do hífen (-), além do caractere de ponto (.) usado como separador. Por padrão, esse valor é o nome do computador de rede da Microsoft, mas o administrador de rede pode atribuir outro nome de host sem afetar o nome do computador.

Exemplo: "corpdns"

</dd> <dt>

**Dnsserversearchorder**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NameServer")
</dt> </dl>

Matriz de endereços IP do servidor a serem usados na consulta para servidores DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, os endereços IP dessa conexão serão registrados no DNS sob o nome de domínio dessa conexão, além de serem registrados no nome DNS completo do computador. O nome de domínio dessa conexão é definido usando o [**método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() ou atribuído por DSCP. O nome registrado é o nome do host do computador com o nome de domínio anexado.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Memória alocada pelo IP para armazenar dados de pacote na fila de pacotes do roteador. Quando esse espaço de buffer é preenchido, o roteador começa a descartar pacotes aleatoriamente de sua fila. Os buffers de dados da fila de pacotes têm 256 bytes de comprimento, portanto, o valor desse parâmetro deve ser um múltiplo de 256. Vários buffers são encadeados para pacotes maiores. O header IP de um pacote é armazenado separadamente. Esse parâmetro será ignorado e nenhum buffer será alocado se o roteador IP não estiver habilitado. O tamanho do buffer pode variar da MTU de rede para um valor menor que 0xFFFFFFFF. Padrão: 74240 (1480 pacotes de 1480 byte, arredondados para um múltiplo de 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, os endereços IP dessa conexão serão registrados no DNS com o nome DNS completo do computador. O nome DNS completo do computador é exibido na guia **Identificação de** Rede no aplicativo Sistema no Painel de Controle.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de valores de métrica de custo inteiro (variando de 1 a 9999) a serem usados no cálculo das rotas mais rápidas, mais confiáveis ou menos intensivas em recursos. Esse argumento tem uma correspondência um-para-um com a **propriedade DefaultIPGateway.**

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Até que ponto o sistema dá suporte a multicast de IP e participa do protocolo IGMP. No nível 0 (zero), o sistema não oferece suporte a multicast. No nível 1, o sistema só pode enviar pacotes de multicast IP. No nível 2, o sistema pode enviar pacotes de multicast IP e participar totalmente do IGMP para receber pacotes multicast.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Sem Multicast** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multicast de IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Multicast IGMP** & IP (2)


</dt> <dd>

Multicast IP e IGMP (padrão)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Classe de controle Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Número de índice da configuração Windows adaptador de rede. O número do índice é usado quando há mais de uma configuração disponível.

</dd> <dt>

**Interfaceindex**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor de índice que identifica exclusivamente um interface de rede local. O valor nessa propriedade é o mesmo que o valor na propriedade **InterfaceIndex** na instância de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa o interface de rede na tabela de rotas.

</dd> <dt>

**EndereçoIP**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip \| IPAddress")
</dt> </dl>

Matriz de todos os endereços IP associados ao adaptador de rede atual. Essa propriedade pode conter endereços IPv6 ou endereços IPv4. Para obter mais informações, consulte [Suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Endereço IPv6 de exemplo: "2010:836B:4179::836B:4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O custo de usar as rotas configuradas para o adaptador de limite de IP e é o valor ponderado para essas rotas na tabela de roteamento de IP. Se houver várias rotas para um destino na tabela de roteamento de IP, a rota com a métrica mais baixa será usada. O valor padrão é 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ Tcpip")
</dt> </dl>

Se **TRUE**, o TCP/IP será vinculado e habilitado nesse adaptador de rede.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled")
</dt> </dl>

Se **TRUE**, a segurança da porta IP será habilitada globalmente em todos os adaptadores de rede associados ao IP e os valores de segurança associados a adaptadores de rede individuais entrarão em vigor. Essa propriedade é usada em conjunto com **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**. Se **FALSE**, a segurança do filtro IP será desabilitada em todos os adaptadores de rede e permitirá que todo o tráfego de porta e protocolo flua sem filtro.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Se **TRUE**, a segurança da porta IP será habilitada globalmente em todos os adaptadores de rede vinculados a IP. Esta propriedade está obsoleta. No lugar dessa propriedade, você deve usar **IPFilterSecurityEnabled**.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Parâmetros Tcpip \\ \\ \| RawIPAllowedProtocols")
</dt> </dl>

Matriz dos protocolos permitidos para executar o IP. A lista de protocolos é definida usando o [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) A lista estará vazia ou conterá valores numéricos. Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todos os protocolos. Uma cadeia de caracteres vazia indica que nenhum protocolo tem permissão para ser executado quando **IPFilterSecurityEnabled** é **TRUE.**

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TCPAllowedPorts")
</dt> </dl>

Matriz das portas que receberão permissão de acesso para TCP. A lista de protocolos é definida usando o [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) A lista estará vazia ou conterá valores numéricos. Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas. Uma cadeia de caracteres vazia indica que nenhuma porta recebe permissão de acesso quando **IPFilterSecurityEnabled** é **TRUE.**

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UDPAllowedPorts")
</dt> </dl>

Matriz das portas que receberão permissão de acesso UDP (User Datagram Protocol). A lista de protocolos é definida usando o [**método EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) A lista estará vazia ou conterá valores numéricos. Um valor numérico de 0 (zero) indica que a permissão de acesso é concedida para todas as portas. Uma cadeia de caracteres vazia indica que nenhuma porta recebe permissão de acesso quando **IPFilterSecurityEnabled** é **TRUE.**

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| SubnetMask")
</dt> </dl>

Matriz de todas as máscaras de sub-rede associadas ao adaptador de rede atual.

Exemplo: "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast")
</dt> </dl>

Se **TRUE**, serão usados zeros-difusões de IP (0.0.0.0) e o sistema usará difusões de ones (255.255.255.255). Os sistemas de computador geralmente usam difusões de um, mas aqueles derivados de implementações BSD usam zeros-broadcasts. Sistemas que não usam as mesmas difusões não interoperarão na mesma rede. O padrão é **FALSE.**

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Versão 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet SNAP** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| MediaType")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Anel de token** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber")
</dt> </dl>

A tecnologia IPX (Internetwork Packet Exchange) não tem mais suporte e essa propriedade não contém dados úteis.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

Intervalo que separa as Retransmissões Keep Alive até que uma resposta seja recebida. Depois que uma resposta é recebida, o atraso até a próxima Transmissão Keep Alive é controlado novamente pelo **valor de KeepAliveTime**. A conexão será anulada depois que o número de retransmissões especificado por **TcpMaxDataRetransmissions** ficar sem resposta. Padrão: 1000, Intervalo válido: 1 – 0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

A **propriedade KeepAliveTime** indica com que frequência o TCP tenta verificar se uma conexão ociosa ainda está intacta enviando um pacote Keep Alive. Um sistema remoto acessível reconhecerá a keep alive remota. Os pacotes Keep Alive não são enviados por padrão. Esse recurso pode ser habilitado em uma conexão por um aplicativo. Padrão: 7.200.000 (duas horas).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de entrada e saída do dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Endereço MAC (Controle de Acesso à Mídia) do adaptador de rede. Um endereço MAC é atribuído pelo fabricante para identificar exclusivamente o adaptador de rede.

Exemplo: "00:80:C7:8F:6C:96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| MTU"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Substitui a MTU (Unidade máxima de transmissão) padrão para um interface de rede. A MTU é o tamanho máximo do pacote (incluindo o header de transporte) que o transporte transmitirá pela rede subjacente. O datagrama IP pode abranger vários pacotes. O intervalo desse valor abrange o tamanho mínimo do pacote (68) para a MTU com suporte da rede subjacente.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NumForwardPackets")
</dt> </dl>

Número de headers de pacotes IP alocados para a fila de pacotes do roteador. Quando todos os headers estão em uso, o roteador começará a descartar pacotes da fila aleatoriamente. Esse valor deve ser pelo menos tão grande quanto o **valor ForwardBufferMemory** dividido pelo tamanho máximo de dados IP das redes conectadas ao roteador. Ele não deve ser maior que o **valor ForwardBufferMemory** dividido por 256, uma vez que pelo menos 256 bytes de memória de buffer de avanço são usados para cada pacote. O número ideal de pacotes de encaminhamento para um determinado tamanho **forwardBufferMemory** depende do tipo de tráfego na rede. Ele estará em algum lugar entre esses dois valores. Se o roteador não estiver habilitado, esse parâmetro será ignorado e nenhum headers será alocado. Padrão: 50, Intervalo válido: 1 – 0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

Se **TRUE**, a detecção de roteadores de orifício preto ocorrerá enquanto o TCP descobre o caminho da Unidade de Transmissão Máxima. Um roteador de orifício preto não retorna mensagens inacessível de destino ICMP quando precisa fragmentar um datagrama IP com o conjunto de bits Não Fragmentar. O TCP depende do recebimento dessas mensagens para executar a Descoberta de MTU de Caminho. Com esse recurso habilitado, o TCP tentará enviar segmentos sem o conjunto de bits Não Fragmentar se várias retransmissões de um segmento não são conhecidas. Se o segmento for confirmado como resultado, o MSS será reduzido e o bit Não Fragmentar será definido em pacotes futuros na conexão. A habilitação da detecção de orifícios pretos aumenta o número máximo de retransmissões executadas para um determinado segmento. O valor padrão dessa propriedade é **FALSE.**

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

Se **TRUE**, o caminho MTU (Unidade máxima de transmissão) será descoberto no caminho para um host remoto. Ao descobrir o caminho da MTU e limitar segmentos TCP a esse tamanho, o TCP pode eliminar a fragmentação em roteadores ao longo do caminho que conectam redes com diferentes MTUs. A fragmentação afeta negativamente a taxa de transferência TCP e o congestionamento de rede. Definir esse parâmetro como **FALSE** faz com que uma MTU de 576 bytes seja usada para todas as conexões que não são para máquinas na sub-rede local. O padrão é **TRUE.**

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nome do serviço do adaptador de rede. Esse nome geralmente é menor que o nome completo do produto.

Exemplo: "Elnkii"

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Bitmap das possíveis configurações relacionadas ao NetBIOS por TCP/IP. Os valores são identificados na lista a seguir.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Tcpip Parameters TcpMaxConnectRetransmissions")
</dt> </dl>

Número de vezes que o TCP tenta retransmitir uma solicitação Conexão antes de encerrar a conexão. O tempo de retransmissão inicial é de 3 segundos. O tempo de retransmissão dobra para cada tentativa. Padrão: 3, Intervalo válido: 0 – 0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpipMaxDataRetransmissions")
</dt> </dl>

Número de vezes que o TCP retransmite um segmento de dados individual (segmento não conectado) antes de encerrar a conexão. O tempo de retransmissão dobra com cada retransmissão sucessiva em uma conexão. Padrão: 5, Intervalo válido: 0 – 0xFFFFFFFF.

</dd> <dt>

**Tcpnumconnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Tcpip Parameters TcpNumConnections")
</dt> </dl>

Número máximo de conexões que o TCP pode ter aberto simultaneamente. Padrão: 0xFFFFFE, Intervalo válido: 0 – 0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122EntPointer**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ Tcpip Parameters Tcpip Parameters \| TcpUseRFC1122EntPointer")
</dt> </dl>

Se **TRUE**, o TCP usará a especificação RFC 1122 para dados urgentes. Se **FALSE** (padrão), o TCP usará o modo usado pelos sistemas derivados do BSD (Design de Software Berkeley). Os dois mecanismos interpretam o ponteiro urgente de forma diferente e não são interoperáveis. O valor padrão é **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho máximo da janela de recepção TCP oferecido pelo sistema. A janela de recepção especifica o número de bytes que um remetente pode transmitir sem receber uma confirmação. Em geral, as janelas de recebimento maiores melhorarão o desempenho em redes de alto atraso e alta largura de banda. Para a eficiência, a janela de recebimento deve ser um múltiplo par do MSS (tamanho máximo de segmento) do TCP. Padrão: quatro vezes o tamanho máximo dos dados TCP ou um múltiplo par de tamanho de dados TCP arredondado para o múltiplo mais próximo de 8192. As redes Ethernet padrão são 8760. Intervalo válido: 0-65535.

> [!Note]  
> Windows Vista: essa propriedade acessa a `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrada do registro, que não é usada na implementação atual do sistema operacional.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableLMHOSTS")
</dt> </dl>

Se **for true**, os arquivos de pesquisa local serão usados. Arquivos de pesquisa conterão um mapa de endereços IP para nomes de host. Se existirem no sistema local, eles serão encontrados em% SystemRoot% \\ System32 \\ drivers \\ etc.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Informações do Sistema funções \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers, \\ \\ etc. \\ \\ lmhosts")
</dt> </dl>

Caminho para um arquivo de pesquisa WINS no sistema local. Esse arquivo conterá um mapa de endereços IP para nomes de host. Se o arquivo especificado nessa propriedade for encontrado, ele será copiado para a pasta% SystemRoot% \\ System32 \\ drivers \\ etc do sistema local. Válido somente se a propriedade **WINSEnableLMHostsLookup** for **true**.

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de entrada e saída de dispositivo do win32api \| DeviceIoControl")
</dt> </dl>

Endereço IP do servidor WINS primário.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Scope Identificação_do_escopo")
</dt> </dl>

Valor acrescentado ao final do nome NetBIOS que isola um grupo de sistemas de computador que se comunicam entre si. Ele é usado para todas as transações NetBIOS em comunicações TCP/IP desse sistema de computador. Computadores configurados com identificadores de escopo idênticos podem se comunicar com este computador. Clientes TCP/IP com diferentes identificadores de escopo desconsideram pacotes de computadores com esse identificador de escopo. Válido somente quando o método [**EnableWINS ativa**](enablewins-method-in-class-win32-networkadapterconfiguration.md) é executado com êxito.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de entrada e saída de dispositivo do win32api \| DeviceIoControl")
</dt> </dl>

Endereço IP do servidor WINS secundário.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ NetworkAdapterConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ NetworkAdapterConfiguration** para recuperar informações de configuração de rede de vários computadores remotos.

As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo **Win32 \_ NetworkAdapterConfiguration**, para exibir informações sobre um sistema local ou remoto.

O código do PowerShell a seguir recupera as definições de configuração para o adaptador Microsoft ISTAP.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



O exemplo C a seguir \# recupera a descrição e o número de índice de todas as instâncias de configuração do adaptador de rede. Observe que esse \# exemplo de C usa o namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , que geralmente é dimensionado de forma mais eficiente do que as classes WMI de namespace [System. Management](/dotnet/api/system.management) .


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



O exemplo C a seguir \# recupera a descrição e o número de índice de todas as instâncias de configuração do adaptador de rede. Observe que este \# exemplo de C usa o namespace [System. Management](/dotnet/api/system.management) original, que foi substituído por [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


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



O exemplo a seguir recupera informações da classe **Win32 \_ NetworkAdapterConfiguration** .


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Tarefas do WMI: rede](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Tarefas do WMI: contas e domínios](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
