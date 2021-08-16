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
ms.openlocfilehash: 72c28486bfa3981870ac331ae83f0cbb532bba4d27c44062ce902823e4e3c259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927125"
---
# <a name="protocol-sequence-constants"></a>Constantes de sequência de protocolo

O Microsoft RPC dá suporte às seguintes sequências de protocolo.



| Constante/valor                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>NetBIOS voltado para conexão TCP do ncacn NB sobre TCP (protocolo de controle de transmissão)</dt> <dt>**\_ \_**</dt> </dl>          | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ \_**</dt> <dt>do pacote de NetBIOS orientado a conexão de ipx no Internet Exchange (ipx)</dt> </dl>               | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>interface de usuário avançado NetBIOS (NetBEUI) orientada a conexão do</dt> <dt>**ncacn \_ NB \_ NB**</dt> </dl>                    | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> protocolo <dt>de controle de transmissão orientado a conexão</dt> <dt>**\_ IP \_ TCP do NCACN**</dt> /protocolo TCP/IP </dl>  | somente cliente: MS-DOS, Windows 3. *x* e cliente e servidor Apple Macintosh: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>pipes nomeados orientados a conexão</dt> do <dt>**ncacn \_ NP**</dt> </dl>                                                            | somente cliente: MS-DOS, Windows 3. *x*, Windows cliente 95 e servidor: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>Exchange de pacote sequenciado orientado a conexão do</dt> <dt>**ncacn \_ spx**</dt> (spx) </dl>                                     | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ NSP**</dt> <dt>transporte descnet orientado a conexão</dt> </dl>                                    | somente cliente: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ no \_**</dt> DSP <dt>de DSP orientado a conexão</dt> com o Apple </dl>                                             | cliente: servidor Macintosh da Apple: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> transporte do <dt>**ncacn \_ VNS \_ spp**</dt> <dt>orientado por conexão Vines de processamento paralelo (spp)</dt> </dl>     | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> Datagram <dt>Protocol (UDP/IP) de datagrama de usuário do</dt> <dt>**ncadg \_ IP \_**</dt> (sem conexão) </dl>   | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_**</dt> <dt>de datagrama IPX (sem conexão)</dt> </dl>                                                           | somente cliente: MS-DOS, Windows 3. *x* Client e server: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> datagrama do <dt>**\_ MQ ncadg**</dt> <dt>(sem conexão) no servidor de fila de mensagens da Microsoft (MSMQ)</dt> </dl>                   | somente cliente: Windows eu/98/95 cliente e servidor: Windows server 2003, Windows XP, Windows 2000, Windows NT server 4,0 com SP3 e posterior<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>TCP/IP voltado para conexão http do ncacn usando o servidor de informações da Internet da Microsoft como proxy http</dt> <dt>**\_**</dt> </dl> | somente cliente: Windows eu/98/95 cliente e servidor: Windows server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt></dt> <dt>chamada de procedimento local</dt> Ncalrpc </dl>                                                                           | cliente e servidor: Windows server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Comentários

O transporte [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) dá suporte \_ somente à autenticação RPC C \_ Authn \_ Winnt. Para obter mais informações, consulte [segurança](security.md) e [autenticação-constantes de serviço](authentication-service-constants.md).

O Microsoft RPC dá suporte a [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) somente em aplicativos cliente, não em aplicativos de servidor.

 

