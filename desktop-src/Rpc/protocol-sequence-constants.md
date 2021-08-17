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



| Constante/valor                                                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ nb \_ tcp**</dt> <dt>Connection-oriented NetBIOS over Transmission Control Protocol (TCP)</dt> </dl>          | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ nb \_ ipx**</dt> <dt>Connection-oriented NetBIOS over Internet Packet Exchange (IPX)</dt> </dl>               | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ nb \_ nb**</dt> <dt>NetBIOS Enhanced Interface do Usuário (NetBEUI)</dt> </dl>                    | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> Protocolo TCP/IP <dt>**\_ \_ (protocolo**</dt> <dt>TCP/IP)</dt> orientado à conexão </dl>  | Somente cliente: MS-DOS, Windows 3. *x* e Apple Macintosh Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> Pipes nomeados <dt>orientados a conexão</dt> <dt>**ncacn \_ np**</dt> </dl>                                                            | Somente cliente: MS-DOS, Windows 3. *x*, Windows cliente e servidor 95: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ spx**</dt> <dt>Connection-oriented Sequenced Packet Exchange (SPX)</dt> </dl>                                     | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ nsp**</dt> <dt>Transporte de DECnet orientado</dt> a conexão </dl>                                    | Somente cliente: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ no \_ DSP**</dt> do AppleTalk orientado <dt>a conexão dsp</dt> </dl>                                             | Cliente: Apple Macintosh Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> Transporte SPP (processamento paralelo escalonável) de Vines orientado a <dt>**ncacn \_ vns \_ spp**</dt> <dt></dt> </dl>     | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ ip \_ udp**</dt> <dt>Datagram (sem conexão) Protocolo de Datagrama de Usuário/Protocolo de Internet (UDP/IP)</dt> </dl>   | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**Ncadg \_ ipx**</dt> <dt>Datagram (sem conexão) IPX</dt> </dl>                                                           | Somente cliente: MS-DOS, Windows 3. *X* Cliente e Servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ mq**</dt> <dt>Datagram (sem conexão) no MSMQ (Servidor</dt> de Fila de Mensagens da Microsoft) </dl>                   | Somente cliente: Windows Cliente e Servidor Me/98/95: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4.0 com SP3 e posterior<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**ncacn \_ http**</dt> <dt>Connection-oriented TCP/IP using Microsoft Internet Information Server as HTTP proxy</dt> </dl> | Somente cliente: Windows Cliente e Servidor me/98/95: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**ncalrpc**</dt> <dt>Chamada de procedimento local</dt> </dl>                                                                           | Cliente e servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Comentários

O [**transporte ncalrpc dá**](/windows/desktop/Midl/ncalrpc) suporte apenas à \_ \_ autenticação AUTHN WINNT do RPC \_ C. Para obter mais informações, consulte [Segurança](security.md) e [constantes de serviço de autenticação](authentication-service-constants.md).

O Microsoft RPC dá [**suporte a RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) somente em aplicativos cliente, não em aplicativos de servidor.

 

