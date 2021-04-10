---
title: Fluxos de pacotes UDP
description: A ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão UDP típica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292516"
---
# <a name="udp-packet-flows"></a>Fluxos de pacotes UDP

Esta seção descreve a ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão UDP típica.

> [!Note]  
> Os fluxos de pacotes UDP para IPv6 seguem o mesmo padrão que para IPv4.

 

> [!Note]  
> Todos os fluxos de pacotes não TCP seguem o mesmo padrão que os fluxos de pacotes UDP.

 

## <a name="udp-connection-establishment"></a>Estabelecimento de conexão UDP

<dl> O servidor (receptor) executa a abertura passiva

-   bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)
-   Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM

  
Cliente (remetente) executa active open

-   bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)
-   Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM
-   SendTo: \_ \_ \_ redirecionamento do FWPM da camada Ale Connect \_ \_ V4 (somente windows 7/Windows Server 2008 R2)
-   SendTo: \_ conexão de \_ autenticação Ale de camada FWPM \_ \_ Connect \_ v4
-   O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4
-   dados: \_ dados de \_ datagramas da camada FWPM \_ \_ v4
-   Mensagem UDP: \_ transporte de saída da camada FWPM \_ \_ \_ v4
-   Datagramas IP: \_ \_ \_ IPPACKET v4 de saída da camada FWPM \_

  
Servidor

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4
-   dados: \_ dados de \_ datagramas da camada FWPM \_ \_ v4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Mensagem UDP recebida sem escuta na porta ou no protocolo

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Datagramas IP: \_ \_ \_ descarte de IPPACKET \_ v4 \_ de entrada na camada FWPM
-   Destino ICMP inacessível: erro de \_ ICMP de saída de camada FWPM \_ \_ \_ \_ v4
-   Destino ICMP inacessível: transporte de \_ saída de camada FWPM \_ \_ \_ v4
-   Destino ICMP inacessível: IPPACKET de \_ saída da camada FWPM \_ \_ \_ v4

> [!Note]  
> O UDP sem nenhum ponto de extremidade é indicado em descartar IPPACKET com uma condição de erro específica. Bloqueie esse pacote em IPPACKET descarte para fazer com que a pilha não envie o evento correspondente (erro de ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Reautorização bem-sucedida de um pacote UDP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   Mensagem UDP: \_ \_ datagrama de camada de FWPM \_ Data \_ V4 (entrada)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Falha na Reautorização de um pacote UDP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Mensagem UDP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   Mensagem UDP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   Mensagem UDP: FWPM \_ camada \_ de \_ autenticação Ale AUT \_ \_ aceitar \_ \_ descarta v4

## <a name="udp-connection-termination"></a>Terminação de conexão UDP

A terminação de conexão UDP não é indicada em nenhuma camada WFP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




