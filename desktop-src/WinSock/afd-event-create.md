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
ms.openlocfilehash: 7ae6f50646ad863be711ab6d48e775aeac9023a053e29044f3921e1dee8c9948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121476"
---
# <a name="afd_event_create-event"></a>Evento AFD \_ EVENT \_ CREATE

O **evento AFD \_ EVENT \_ CREATE** é um evento de rastreamento de rede Winsock para uma operação de criação de soquete.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informações sobre esse evento.

A tabela a seguir lista os valores possíveis para o *parâmetro EnterExit:*



| Valor                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | O início de uma solicitação Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | A solicitação Winsock foi concluída.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | O driver AfD do Winsock fez uma ação interna (anulando uma conexão, por exemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | O driver TCP/IP fez com que esse evento ocorreu. Isso geralmente indica uma notificação de dados.<br/> |
| <dl> <dt>4</dt> </dl> | O driver AFD winsock fez com que esse evento ocorreu (definindo uma opção de soquete, por exemplo).<br/> |



 

</dd> <dt>

*Localização* 
</dt> <dd>

Um campo privado usado internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

O [endereço EPROCESS](/windows-hardware/drivers/kernel/eprocess) do processo que possui o soquete relacionado. Essa é uma estrutura opaca que serve como o objeto de processo para um processo. Para obter mais informações, consulte a documentação Windows driver kit para a [estrutura EPROCESS.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Ponto de extremidade* 
</dt> <dd>

O endereço AFD \_ ENDPOINT do soquete.

</dd> <dt>

*Addressfamily* 
</dt> <dd>

A especificação da família de endereços para o soquete. Os valores possíveis para a família de endereços são definidos no arquivo de título *Ws2def.h.* Observe que o *arquivo de título Ws2def.h* é incluído automaticamente no *Winsock2.h* e nunca deve ser usado diretamente.

Os valores atualmente suportados são AF INET ou AF INET6, que são os formatos de família de endereços da \_ \_ Internet para IPv4 e IPv6. Outras opções para família de endereços (AF NETBIOS para uso com NetBIOS, por exemplo) têm suporte se um provedor de serviços Windows Sockets para a família de \_ endereços estiver instalado.

A tabela a seguir lista valores comuns para a família de endereços, embora muitos outros valores sejam possíveis.



| Af                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ UNSPEC**</dt> <dt>0</dt> </dl>           | A família de endereços não é especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | A família de endereços protocolo IP versão 4 (IPv4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | A família de endereços IPX/SPX. Essa família de endereços só será compatível se o protocolo de transporte compatível com NWLink IPX/SPX NetBIOS estiver instalado. <br/> Não há suporte para essa família de endereços Windows Vista e posterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | A família de endereços do AppleTalk. Essa família de endereços só será suportada se o protocolo AppleTalk estiver instalado. <br/> Não há suporte para essa família de endereços Windows Vista e posterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | A família de endereços NetBIOS. Essa família de endereços só será suportada se o provedor Windows Sockets para NetBIOS estiver instalado. <br/> O provedor Windows Sockets para NetBIOS tem suporte em versões de 32 bits do Windows. Esse provedor é instalado por padrão em versões de 32 bits do Windows. <br/> O Windows de soquetes para NetBIOS não tem suporte em versões de 64 bits do Windows. <br/> O provedor Windows Sockets para NetBIOS dá suporte apenas a soquetes em que o parâmetro *de* tipo está definido como **SOCK \_ DGRAM.**<br/> O provedor Windows Sockets para NetBIOS não está diretamente relacionado à interface de programação [NetBIOS.](/previous-versions/windows/desktop/netbios/portal) Não há suporte para a interface de programação NetBIOS no Windows Vista, Windows Server 2008 e posterior.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | A família de endereços IPv6 (Internet Protocol versão 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | A família de endereços IrDA (Associação de Dados Indecodados). <br/> Essa família de endereços só terá suporte se o computador tiver uma porta e um driver indepesados instalados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | A família Bluetooth endereços de usuário. <br/> Essa família de endereços só terá suporte se o computador tiver um adaptador Bluetooth e driver instalados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*Sockettype* 
</dt> <dd>

A especificação de tipo para o novo soquete. Os valores possíveis para o tipo de soquete são definidos no arquivo de título *Winsock2.h.*

A tabela a seguir lista os valores possíveis para o *parâmetro de* tipo com suporte para Windows Sockets 2:



| Type                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**SOCK \_ STREAM**</dt> <dt>1</dt> </dl>          | Um tipo de soquete que fornece fluxos de byte sequenciados, confiáveis, de duas vias e baseados em conexão com um mecanismo de transmissão de dados OOB. Esse tipo de soquete usa o protocolo TCP para a família de endereços da Internet (AF \_ INET ou AF \_ INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**SOCK \_ DGRAM**</dt> <dt>2</dt> </dl>             | Um tipo de soquete que dá suporte a datagramas, que são buffers não confiáveis sem conexão de um comprimento máximo fixo (normalmente pequeno). Esse tipo de soquete usa o protocolo UDP para a família de endereços da Internet (AF \_ INET ou AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**SOCK \_ RAW**</dt> <dt>3</dt> </dl>                   | Um tipo de soquete que fornece um soquete bruto que permite que um aplicativo manipule o próximo header de protocolo de camada superior. Para manipular o header IPv4, a opção de soquete [**\_ IP HDRINCL**](ipproto-ip-socket-options.md) deve ser definida no soquete. Para manipular o header IPv6, a opção de [**soquete \_ HDRINCL IPV6**](ipproto-ipv6-socket-options.md) deve ser definida no soquete. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**SOCK \_ RDM**</dt> <dt>4</dt> </dl>                   | Um tipo de soquete que fornece um datagrama de mensagem confiável. Um exemplo desse tipo é a implementação do protocolo multicast Pragmatic General Multicast (PGM) no Windows, geralmente conhecido como programação [multicast confiável.](reliable-multicast-programming--pgm-.md) <br/> Esse *valor* de tipo só será suportado se o Reliable Multicast Protocol estiver instalado.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**SOCK \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Um tipo de soquete que fornece um pacote pseudo-fluxo com base em datagramas. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocolo* 
</dt> <dd>

O protocolo a ser usado. As opções possíveis para o *parâmetro de* protocolo são específicas para a família de endereços e o tipo de soquete especificados. Os valores  possíveis para o protocolo são definidos no arquivo de título *Wsrm.h* e no tipo de enumeração **IPPROTO** definido no arquivo de título *Ws2def.h.* Observe que o *arquivo de título Ws2def.h* é incluído automaticamente no *Winsock2.h* e nunca deve ser usado diretamente.

Se um valor de 0 for especificado, o chamador não desejará especificar um protocolo e o provedor de serviços escolherá o *protocolo* a ser usado.

A tabela a seguir lista valores comuns para o *protocolo,* embora muitos outros valores sejam possíveis.



| protocolo                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | O protocolo ICMP. Esse  é um valor possível quando o parâmetro *af* é AF **\_ UNSPEC,** AF **\_ INET** ou AF **\_ INET6** e o parâmetro de tipo é SOCK **\_ RAW** ou não especificado.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | O protocolo IGMP. Esse  é um valor possível quando o parâmetro *af* é AF **\_ UNSPEC,** AF **\_ INET** ou AF **\_ INET6** e o parâmetro de tipo é SOCK **\_ RAW** ou não especificado.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | O Bluetooth rfCOMM (comunicações de Bluetooth radiofrequência). Esse é um valor possível quando o *parâmetro af* é **AF \_ BTH** e o *parâmetro de* tipo é **SOCK \_ STREAM.** <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | O protocolo TCP. Esse é um valor possível quando o *parâmetro af* é **AF \_ INET ou** AF **\_ INET6** e o parâmetro *de* tipo é **SOCK \_ STREAM.**<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | O protocolo UDP. Esse é um valor possível quando o *parâmetro af* é **AF \_ INET** ou **AF \_ INET6** e o parâmetro *de* tipo é **SOCK \_ DGRAM.**<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | O ICMPv6 (Protocolo ICMPv6). Esse  é um valor possível quando o parâmetro *af* é AF **\_ UNSPEC,** AF **\_ INET** ou AF **\_ INET6** e o parâmetro de tipo é SOCK **\_ RAW** ou não especificado.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | O protocolo PGM para multicast confiável. Esse é um valor possível quando o *parâmetro af* é **AF \_ INET** e o *parâmetro de* tipo é **SOCK \_ RDM**. Esse protocolo também é chamado **de IPPROTO \_ PGM.** <br/> Esse *valor* de protocolo só será suportado se o Reliable Multicast Protocol estiver instalado.<br/> |



 

</dd> <dt>

*Processid* 
</dt> <dd>

A ID do processo real ou um indicador se o evento foi resultado da sequência de código Winsock em um processo do sistema ou em um contexto DPC (chamada de procedimento adiado) (contextos fora do processo do usuário).

</dd> <dt>

*Status* 
</dt> <dd>

O código NTSTATUS para a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **evento AFD \_ EVENT \_ CREATE** é rastreado para uma operação de rede Winsock para criar um soquete. O canal para esse evento é Winsock-AFD. O nível desse evento é informacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle do rastreamento winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**DESCRITOR \_ DE EVENTO**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Rastreamento winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de alterações do catálogo winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

