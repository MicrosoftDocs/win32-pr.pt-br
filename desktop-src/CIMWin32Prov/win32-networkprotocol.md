---
description: O Win32 \_ NetworkProtocol&\# 8194; A classe WMI representa um protocolo e suas características de rede em um sistema de computador Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457142"
---
# <a name="win32_networkprotocol-class"></a>\_Classe Win32 NetworkProtocol

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol do Win32** representa um protocolo e suas características de rede em um sistema de computador Win32.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ NetworkProtocol** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ NetworkProtocol** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações \| dwServiceFlags \| XP1 sem \_ conexão")
</dt> </dl>

O protocolo oferece suporte ao serviço sem conexão. Um serviço sem conexão (datagrama) descreve um protocolo de comunicação ou transporte no qual os pacotes de dados são roteados independentemente um do outro e podem seguir rotas diferentes e chegam em uma ordem diferente da que foram enviados. Por outro lado, um serviço orientado a conexão fornece um circuito virtual por meio do qual os pacotes de dados são recebidos na mesma ordem em que foram transmitidos. Se a conexão entre os computadores falhar, o aplicativo será notificado.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ garantido \_ Delivery")
</dt> </dl>

O protocolo oferece suporte à entrega de pacotes de dados. Se esse sinalizador for **false**, é incerteza que todos os dados enviados atingirão o destino pretendido.

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ asguaranteed \_ Order")
</dt> </dl>

O protocolo garante que os dados chegarão na ordem em que foram enviados. Lembre-se de que essa característica não garante a entrega dos dados, apenas sua ordem.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| iMaxSockAddr"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")
</dt> </dl>

Comprimento máximo de um endereço de soquete com suporte pelo protocolo. Os endereços de soquete podem ser itens como uma URL ( `www.microsoft.com` ) ou um endereço IP ( `130.215.24.1` ).

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwMessageSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")
</dt> </dl>

Tamanho máximo de mensagem suportado pelo protocolo. Esse é o tamanho máximo de uma mensagem que pode ser enviada ou recebida pelo host. Para protocolos que não dão suporte ao enquadramento de mensagens, o tamanho máximo real de uma mensagem que pode ser enviada para um determinado endereço pode ser menor que esse valor.

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 do \_ \| Windows Sockets \| Protocol \_ info do \| dwServiceFlags \| XP \_ \_ orientado a mensagens")
</dt> </dl>

O protocolo é orientado a mensagens. Um protocolo orientado a mensagens usa pacotes de dados para transferir informações. Por outro lado, os protocolos orientados a fluxo transferem dados como um fluxo contínuo de bytes.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| iMinSockAddr"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")
</dt> </dl>

Comprimento mínimo de um endereço de soquete com suporte pelo protocolo.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| lpProtocol")
</dt> </dl>

Nome para o protocolo.

Exemplo: "TCP/IP"

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ pseudo \_ Stream")
</dt> </dl>

O protocolo é um protocolo orientado a mensagens que pode receber pacotes de dados de comprimento variável ou dados transmitidos para todas as operações de recebimento. Essa capacidade opcional é útil quando um aplicativo não quer o protocolo para enquadrar mensagens e requer características orientadas a fluxo. Se **for true**, o protocolo será orientado a um pseudo-fluxo.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ suporta \_ Broadcast")
</dt> </dl>

O protocolo dá suporte a um mecanismo de transmissão de mensagens pela rede.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Connect \_ Data")
</dt> </dl>

O protocolo permite que os dados sejam conectados pela rede.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Desconectar \_ dados")
</dt> </dl>

O protocolo permite que os dados sejam desconectados pela rede.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações \| dwServiceFlags \| XP \_ criptografas")
</dt> </dl>

O protocolo dá suporte à criptografia de dados.

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ expedited \_ Data")
</dt> </dl>

O protocolo oferece suporte a dados emitidos (também conhecidos como dados urgentes) na rede. Os dados acelerados podem ignorar o controle de fluxo e receber a prioridade sobre pacotes de dados normais.

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 do \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Fragmentation")
</dt> </dl>

O protocolo dá suporte à transmissão de dados em fragmentos. A unidade de transferência máxima (MTU) da rede física está oculta dos aplicativos. Cada tipo de mídia tem um tamanho de quadro máximo que não pode ser excedido. A camada de link descobre a MTU e a relata para os protocolos usados.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ normal \_ Close")
</dt> </dl>

O protocolo dá suporte a operações de fechamento de duas fases, também conhecidas como "operações de fechamento normais". Caso contrário, o protocolo oferece suporte apenas a operações de fechamento anuladas.

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações de alocação de largura de \| \| banda dwServiceFlags XP \_ \_ ")
</dt> </dl>

O protocolo tem um mecanismo para estabelecer e manter uma largura de banda.

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("as \_ informações do protocolo de estruturas do Windows Sockets de API do Win32 \| \| \_ \| dwServiceFlags \| XP \_ dão suporte a \_ multicast")
</dt> </dl>

O protocolo dá suporte a multicast.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets estruturas \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ supported")
</dt> </dl>

O protocolo é capaz de dar suporte à qualidade de serviço (QoS) pelo provedor de serviços em camadas subjacente ou pela operadora de transporte. QoS é uma coleção de componentes que habilitam a diferenciação e o tratamento preferencial para subconjuntos de dados transmitidos pela rede. QoS significa que os subconjuntos de dados recebem maior prioridade ou serviço garantido ao atravessar uma rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ NetworkProtocol** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir demonstra como recuperar uma lista de serviços em execução de instâncias do **Win32 \_ NetworkProtocol**.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



O exemplo de código Perl a seguir demonstra como recuperar uma lista de serviços em execução de instâncias do **Win32 \_ NetworkProtocol**.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
