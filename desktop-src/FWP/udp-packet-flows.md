---
title: Fluxos de pacotes UDP
description: A ordem na qual as camadas do mecanismo de filtro Windows WFP (Plataforma de Filtragem de Dados) são percorridas durante uma sessão UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e850f67bce9a001d41ebb54b17d3d0d86b94b22f083529e4589d6b69841b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746636"
---
# <a name="udp-packet-flows"></a>Fluxos de pacotes UDP

Esta seção descreve a ordem na qual as camadas do mecanismo de filtro WFP (plataforma de filtragem Windows) são percorridas durante uma sessão UDP típica.

> [!Note]  
> Os fluxos de pacotes UDP para IPv6 seguem o mesmo padrão do IPv4.

 

> [!Note]  
> Todos os fluxos de pacotes não TCP seguem o mesmo padrão que os fluxos de pacotes UDP.

 

## <a name="udp-connection-establishment"></a>Estabelecimento de conexão UDP

<dl> Servidor (receptor) executa Abertura Passiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (Windows 7/Windows Server 2008 R2 somente)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4

  
O cliente (remetente) executa o Active Open

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (Windows 7/Windows Server 2008 R2 somente)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   sendto: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (somente Windows 7/Windows Server 2008 R2)
-   sendto: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   dados: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   Datagramas IP: \_ \_ \_ IPPACKET \_ V4 DE SAÍDA DA CAMADA FWPM

  
Servidor

-   Datagramas IP: \_ \_ \_ IPPACKET \_ V4 DA CAMADA FWPM
-   Mensagem UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   dados: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Mensagem UDP recebida sem ninguém escutando na porta ou no protocolo

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET \_ V4 DA CAMADA FWPM
-   Datagramas IP: DESCARTE DE \_ \_ \_ IPPACKET \_ V4 \_ DA CAMADA FWPM
-   IcMP Dest Inacessível: ERRO ICMP DE SAÍDA DA CAMADA FWPM \_ \_ \_ \_ \_ V4
-   IcMP Dest Inacessível: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   IcMP Dest Inacessível: \_ \_ \_ IPPACKET \_ V4 de SAÍDA DA CAMADA FWPM

> [!Note]  
> UDP sem ponto de extremidade é indicado no descarte de IPPACKET com uma condição de erro específica. Bloqueie esse pacote no descarte de IPPACKET para fazer com que a pilha não envie o evento correspondente (erro ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Reautorização bem-sucedida de um pacote UDP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET \_ V4 DA CAMADA FWPM
-   Mensagem UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ DATA DATA \_ \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Falha na reautorização de um pacote UDP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET \_ V4 DA CAMADA FWPM
-   Mensagem UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Mensagem UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="udp-connection-termination"></a>Terminação de conexão UDP

A terminação de conexão UDP não é indicada em nenhuma camada WFP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




