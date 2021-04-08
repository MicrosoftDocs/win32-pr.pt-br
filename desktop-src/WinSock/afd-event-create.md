---
description: Evento de rastreamento de rede Winsock para uma operação de criação de soquete.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827128"
---
# <a name="afd_event_create-event"></a>Evento de criação de \_ evento de AFD \_

O evento de criação de **\_ \_ evento de AFD** é um evento de rastreamento de rede do Winsock para uma operação de criação de soquete.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informações sobre este evento.

A tabela a seguir lista os possíveis valores para o parâmetro *EnterExit* :



| Valor                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | O início de uma solicitação do Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | A solicitação do Winsock foi concluída.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | O driver do Winsock AFD realizou uma ação interna (anulando uma conexão, por exemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | O driver TCP/IP fez com que esse evento ocorresse. Isso geralmente indica uma notificação de dados.<br/> |
| <dl> <dt>4</dt> </dl> | O driver do Winsock AFD fez com que esse evento ocorresse (definindo uma opção de soquete, por exemplo).<br/> |



 

</dd> <dt>

*Localidade* 
</dt> <dd>

Um campo privado usado internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

O endereço [EPROCESS](/windows-hardware/drivers/kernel/eprocess) do processo que possui o soquete relacionado. Essa é uma estrutura opaca que serve como o objeto de processo para um processo. Para obter mais informações, consulte a documentação do Windows Driver Kit para a estrutura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Ponto de extremidade* 
</dt> <dd>

O \_ endereço do ponto de extremidade de AFD do soquete.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

A especificação da família de endereços para o soquete. Os valores possíveis para a família de endereços são definidos no arquivo de cabeçalho *Ws2def. h* . Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

Os valores atualmente com suporte são \_ INET6 inet ou AF \_ , que são os formatos de família de endereços da Internet para IPv4 e IPv6. Outras opções para a família de endereços (o \_ NetBIOS de AF para uso com NetBIOS, por exemplo) têm suporte se um provedor de serviços do Windows Sockets para a família de endereços estiver instalado.

A tabela a seguir lista os valores comuns para a família de endereços, embora muitos outros valores sejam possíveis.



| AF                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ Inspecs**</dt> <dt>0</dt> </dl>           | A família de endereços não está especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | A família de endereços IPv4 (protocolo IP versão 4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | A família de endereços IPX/SPX. Essa família de endereços só terá suporte se o protocolo de transporte compatível com NetBIOS NWLink IPX/SPX for instalado. <br/> Não há suporte para essa família de endereços no Windows Vista e posterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | A família de endereços AppleTalk. Essa família de endereços só terá suporte se o protocolo AppleTalk estiver instalado. <br/> Não há suporte para essa família de endereços no Windows Vista e posterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | A família de endereços NetBIOS. Essa família de endereços só terá suporte se o provedor do Windows Sockets para NetBIOS estiver instalado. <br/> O Windows Sockets Provider para NetBIOS tem suporte nas versões de 32 bits do Windows. Esse provedor é instalado por padrão nas versões de 32 bits do Windows. <br/> Não há suporte para o Windows Sockets Provider para NetBIOS em versões de 64 bits do Windows. <br/> O provedor do Windows Sockets para NetBIOS só dá suporte a soquetes em que o parâmetro de *tipo* está definido como **Sock \_ DGRAM**.<br/> O provedor do Windows Sockets para NetBIOS não está diretamente relacionado à interface de programação [NetBIOS](/previous-versions/windows/desktop/netbios/portal) . Não há suporte para a interface de programação NetBIOS no Windows Vista, no Windows Server 2008 e posterior.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | A família de endereços IPv6 (protocolo IP versão 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_**</dt> <dt>26</dt> de IrDA </dl>                | A família de endereços da Associação de dados de infravermelho (IrDA). <br/> Essa família de endereços só terá suporte se o computador tiver uma porta de infravermelho e driver instalado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | A família de endereços Bluetooth. <br/> Essa família de endereços só terá suporte se o computador tiver um adaptador Bluetooth e um driver instalado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

A especificação de tipo para o novo soquete. Os valores possíveis para o tipo de soquete são definidos no arquivo de cabeçalho *Winsock2. h* .

A tabela a seguir lista os possíveis valores para o parâmetro de *tipo* com suporte para o Windows Sockets 2:



| Type                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**Sock \_ FLUXO**</dt> <dt>1</dt> </dl>          | Um tipo de soquete que fornece fluxos de bytes seqüenciais, confiáveis e bidirecionais baseados em conexões com um mecanismo de transmissão de dados OOB. Esse tipo de soquete usa o TCP (protocolo de controle de transmissão) para a família de endereços da Internet (AF \_ inet ou AF \_ INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**Sock \_ DGRAM**</dt> <dt>2</dt> </dl>             | Um tipo de soquete que dá suporte a datagrams, que são buffers sem conexão de um tamanho máximo fixo (normalmente pequeno). Esse tipo de soquete usa o UDP (User Datagram Protocol) para a família de endereços da Internet (AF \_ inet ou AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**Sock \_ BRUTO**</dt> <dt>3</dt> </dl>                   | Um tipo de soquete que fornece um soquete bruto que permite que um aplicativo manipule o próximo cabeçalho de protocolo de camada superior. Para manipular o cabeçalho IPv4, a opção [**IP \_ HDRINCL**](ipproto-ip-socket-options.md) Socket deve ser definida no soquete. Para manipular o cabeçalho IPv6, a opção de soquete [**\_ HDRINCL do IPv6**](ipproto-ipv6-socket-options.md) deve ser definida no soquete. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**Sock \_ RDM**</dt> <dt>4</dt> </dl>                   | Um tipo de soquete que fornece um datagrama de mensagem confiável. Um exemplo desse tipo é a implementação do protocolo de multicast Pragmatic General multicast (PGM) no Windows, geralmente conhecida como [programação de multicast confiável](reliable-multicast-programming--pgm-.md). <br/> Esse valor de *tipo* só terá suporte se o protocolo de multicast confiável estiver instalado.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**Sock \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Um tipo de soquete que fornece um pacote de pseudo-fluxo baseado em datagrams. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocolo* 
</dt> <dd>

O protocolo a ser usado. As opções possíveis para o parâmetro de *protocolo* são específicas para a família de endereços e o tipo de soquete especificado. Os valores possíveis para o *protocolo* são definidos no arquivo de cabeçalho *wsrm. h* e no tipo de enumeração **IPPROTO** definido no arquivo de cabeçalho *Ws2def. h* . Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

Se um valor de 0 for especificado, o chamador não deseja especificar um protocolo e o provedor de serviços escolherá o *protocolo* a ser usado.

A tabela a seguir lista os valores comuns para o *protocolo* , embora muitos outros valores sejam possíveis.



| protocolo                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | O protocolo ICMP (Internet Control Message Protocol). Esse é um valor possível quando o parâmetro *AF* é **AF \_ inspec**, **AF \_ inet** ou **AF \_ INET6** e o parâmetro de *tipo* é **Sock \_ RAW** ou não especificado.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | O protocolo IGMP (Internet Group Management Protocol). Esse é um valor possível quando o parâmetro *AF* é **AF \_ inspec**, **AF \_ inet** ou **AF \_ INET6** e o parâmetro de *tipo* é **Sock \_ RAW** ou não especificado.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | O protocolo Bluetooth RFCOMM (comunicação por radiofrequência) do Bluetooth. Esse é um valor possível quando o parâmetro *AF* é **AF \_ BTH** e o parâmetro de *tipo* é **Sock \_ Stream**. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | O protocolo TCP. Esse é um valor possível quando o parâmetro *AF* é AF, **\_ INET6** **\_ inet** ou AF, e o parâmetro de *tipo* é **Sock \_ Stream**.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | O UDP (User Datagram Protocol). Esse é um valor possível quando o parâmetro *AF* é AF, **\_ INET6** **\_ inet** ou AF, e o parâmetro de *tipo* é **Sock \_ DGRAM**.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | O protocolo de mensagem de controle da Internet versão 6 (ICMPv6). Esse é um valor possível quando o parâmetro *AF* é **AF \_ inspec**, **AF \_ inet** ou **AF \_ INET6** e o parâmetro de *tipo* é **Sock \_ RAW** ou não especificado.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | O protocolo PGM para multicast confiável. Esse é um valor possível quando o parâmetro *AF* é **o \_ inet da AF** e o parâmetro de *tipo* é **Sock \_ RDM**. Esse protocolo também é chamado **de \_ PGM IPPROTO**. <br/> Esse valor de *protocolo* só terá suporte se o protocolo de multicast confiável estiver instalado.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

A ID do processo real ou um indicador se o evento foi resultado da execução do código Winsock em um processo do sistema ou em um contexto de DPC (chamada de procedimento deferida) (contextos fora do processo do usuário).

</dd> <dt>

*Status* 
</dt> <dd>

O código NTSTATUS para a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento de **\_ \_ criação de evento de AFD** é rastreado para uma operação de rede Winsock para criar um soquete. O canal para esse evento é o Winsock-AFD. O nível desse evento é informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_descritor de evento**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

