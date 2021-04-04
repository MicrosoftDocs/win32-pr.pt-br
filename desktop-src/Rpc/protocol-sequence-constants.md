---
title: Constantes de sequência de protocolo
description: O Microsoft RPC dá suporte às seguintes sequências de protocolo.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007994"
---
# <a name="protocol-sequence-constants"></a>Constantes de sequência de protocolo

O Microsoft RPC dá suporte às seguintes sequências de protocolo.



| Constante/valor                                                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>NetBIOS voltado para conexão TCP do ncacn NB sobre TCP (protocolo de controle de transmissão)</dt> <dt>**\_ \_**</dt> </dl>          | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>NetBIOS voltado para a conexão IPX do ncacn NB sobre o IPX (Internet Packet Exchange)</dt> <dt>**\_ \_**</dt> </dl>               | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>interface de usuário avançado NetBIOS (NetBEUI) orientada a conexão do</dt> <dt>**ncacn \_ NB \_ NB**</dt> </dl>                    | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> protocolo <dt>de controle de transmissão orientado a conexão</dt> <dt>**\_ IP \_ TCP do NCACN**</dt> /protocolo TCP/IP </dl>  | Somente cliente: MS-DOS, Windows 3. *x* e cliente e servidor Apple Macintosh: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>pipes nomeados orientados a conexão</dt> do <dt>**ncacn \_ NP**</dt> </dl>                                                            | Somente cliente: MS-DOS, Windows 3. *x*, cliente do Windows 95 e servidor: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>SPX (troca de pacotes sequenciado) orientado a conexão</dt> <dt>**ncacn \_ SPX**</dt> </dl>                                     | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ NSP**</dt> <dt>transporte descnet orientado a conexão</dt> </dl>                                    | Somente cliente: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ no \_**</dt> DSP <dt>de DSP orientado a conexão</dt> com o Apple </dl>                                             | Cliente: servidor Apple Macintosh: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> transporte do <dt>**ncacn \_ VNS \_ spp**</dt> <dt>orientado por conexão Vines de processamento paralelo (spp)</dt> </dl>     | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> Datagram <dt>Protocol (UDP/IP) de datagrama de usuário do</dt> <dt>**ncadg \_ IP \_**</dt> (sem conexão) </dl>   | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_**</dt> <dt>de datagrama IPX (sem conexão)</dt> </dl>                                                           | Somente cliente: MS-DOS, Windows 3. *x* Client e Server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> datagrama do <dt>**\_ MQ ncadg**</dt> <dt>(sem conexão) no servidor de fila de mensagens da Microsoft (MSMQ)</dt> </dl>                   | Somente cliente: cliente e servidor do Windows me/98/95: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 com SP3 e posterior<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>TCP/IP voltado para conexão http do ncacn usando o servidor de informações da Internet da Microsoft como proxy http</dt> <dt>**\_**</dt> </dl> | Somente cliente: cliente e servidor do Windows me/98/95: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt></dt> <dt>chamada de procedimento local</dt> Ncalrpc </dl>                                                                           | Cliente e servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Comentários

O transporte [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) dá suporte \_ somente à autenticação RPC C \_ Authn \_ Winnt. Para obter mais informações, consulte [segurança](security.md) e [autenticação-constantes de serviço](authentication-service-constants.md).

O Microsoft RPC dá suporte a [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) somente em aplicativos cliente, não em aplicativos de servidor.

 

