---
title: Identificadores de protocolo
description: Os seguintes identificadores de protocolo também estão listados em Routprot. h para o SDK do Windows e iprtmib. h para o SDK (Software Development Kit) da plataforma.
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ac515eb4b5090c0b4f75fd923d8345538ff5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294330"
---
# <a name="protocol-identifiers"></a>Identificadores de protocolo

Os seguintes identificadores de protocolo também estão listados em Routprot. h para o SDK do Windows e iprtmib. h para o SDK (Software Development Kit) da plataforma.

## <a name="ip-protocols"></a>Protocolos de IP

Os seguintes protocolos de roteamento estão associados ao transporte IP.



| Protocolo                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IP de PROTO \_ \_ diferente, \_ IPPROTO \_ MIB                        | Algum outro protocolo não especificado no RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_IP proto \_ local, MIB \_ IPPROTO \_ local                        | Uma interface local.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ netger, MIB \_ IPPROTO \_ netmgmt                    | Uma rota estática. Esse valor é usado para identificar informações de rota para o roteamento de IP definido por meio do gerenciamento de rede, como o protocolo DHCP, o protocolo SNMP (Simple Network Management Protocol) ou chamadas para as funções [**CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)ou [**SetIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry) .                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | O resultado do redirecionamento de ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | O protocolo de gateway exterior (EGP), um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | O protocolo de gateway para gateway (GGP), um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ Olá, MIB \_ IPPROTO \_ Olá                        | O protocolo Hellospeak, um protocolo de roteamento dinâmico. Essa é uma entrada histórica que não está mais em uso e foi um protocolo de roteamento inicial usado pelos roteadores da ARPANET originais que executaram software especial chamado de protocolo de roteamento Fuzzball, às vezes chamado de Hellospeak, conforme descrito em RFC 891 e RFC 1305. Para obter mais informações, confira [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) e [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | O RIP (Berkeley Routing Information Protocol) ou o RIP-II, um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| o \_ IP proto é \_ , o \_ MIB \_ IPPROTO \_ é \_                      | O protocolo IS-IS (sistema intermediário de sistema a intermediário), um protocolo de roteamento dinâmico. O protocolo IS-IS foi desenvolvido para uso no pacote de protocolo OSI (interconexão de sistemas abertos).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ es \_ é, MIB \_ IPPROTO \_ es \_ is                      | O protocolo ES-IS (sistema-to-intermediário System-IS), um protocolo de roteamento dinâmico. O protocolo ES-IS foi desenvolvido para uso no pacote de protocolo OSI (interconexão de sistemas abertos).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ Cisco, MIB \_ IPPROTO \_ Cisco                        | O protocolo de roteamento de gateway do Cisco interior (IGRP), um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | O Beranek (protocolo de gateway interior) do Newman (BBN) que usou o algoritmo SPF (caminho mais curto primeiro). Esse era um protocolo de roteamento dinâmico antecipado.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | O protocolo OSPF (Open Shortest Path First), um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | O Border Gateway Protocol (BGP), um protocolo de roteamento dinâmico.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP, MIB \_ IPPROTO \_ BOOTP                        | O protocolo bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPv6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | O protocolo de retransmissão DHCPv6.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ autoestático, MIB \_ IPNT \_ autoestático             | Uma entrada específica do Windows adicionada originalmente por um protocolo de roteamento, mas que agora é estático.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ static, MIB \_ IPNT \_ estático                     | Uma entrada específica do Windows adicionada como uma rota estática da interface do usuário de roteamento ou um comando de roteamento.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ estático \_ não \_ DOD, MIB \_ IPNT \_ estático \_ não \_ DOD | Uma entrada específica do Windows adicionada como uma rota estática da interface do usuário de roteamento ou um comando de roteamento, exceto que essas rotas não causam a demanda por discagem (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

As rotas com um identificador de protocolo de \_ IP \_ local proto incluem:

-   A rota de loopback
-   A rota da sub-rede
-   Rota de difusão de todas as redes para interfaces de sub-rede
-   Toda rota de difusão de "1"
-   Rota de multicast local
-   Rotear para extremidade remota de um link PPP

O identificador para o Gerenciador do roteador IP é:

IPRTRMGR \_ PID

Esse identificador pode ser usado em vez de um identificador de protocolo de roteamento para chamadas de MIB com o Gerenciador de roteador de IP. Esse identificador é usado para MIB-II, encaminhamento de MIB e algumas informações específicas da empresa. Esse identificador também está listado em Iprtrmib. h.

## <a name="ipx-protocols"></a>Protocolos IPX

Os seguintes protocolos de roteamento estão associados ao transporte IPX.



| Protocolo            | Descrição                          |
|---------------------|--------------------------------------|
| \_Rip do protocolo IPX \_  | Protocolo de informações de roteamento para IPX |
| \_protocolo IPX \_ SAP  | Protocolo de anúncio de serviço       |
| \_protocolo IPX \_ NLSP | Protocolo de serviços de link do NetWare       |



 

O identificador para o Gerenciador de roteador IPX é:

\_base do protocolo IPX \_

Use esse identificador em vez de um identificador de protocolo de roteamento para chamadas MIB com o Gerenciador de roteador IPX.

 

 