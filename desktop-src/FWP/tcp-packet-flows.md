---
title: Fluxos de pacotes TCP
description: A ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão TCP típica.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916443"
---
# <a name="tcp-packet-flows"></a>Fluxos de pacotes TCP

Esta seção descreve a ordem na qual as camadas do mecanismo de filtro da WFP (Windows Filtering Platform) são percorridas durante uma sessão TCP típica.

> [!Note]  
> Os fluxos de pacotes TCP para IPv6 seguem o mesmo padrão que para IPv4.

 

> [!Note]  
> Os fluxos de pacotes não TCP seguem o mesmo padrão que os [fluxos de pacotes UDP](udp-packet-flows.md).

 

## <a name="tcp-connection-establishment"></a>Estabelecimento de conexão TCP

<dl> O servidor (receptor) executa a abertura passiva

-   bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)
-   Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM
-   escutar: FWPM \_ da \_ autenticação Ale de camada de conexão \_ \_ \_ v4

  
Cliente (remetente) executa active open

-   bind: \_ \_ \_ \_ redirecionamento de associação Ale de camada FWPM \_ (somente windows 7/Windows Server 2008 R2)
-   Associação: \_ v4 de \_ \_ atribuição de \_ recursos \_ da camada FWPM
-   Connect: \_ \_ redirecionamento da camada Ale do FWPM layer para \_ \_ \_ V4 (somente windows 7/Windows Server 2008 R2)
-   conectar: \_ conexão de \_ autenticação Ale de camada FWPM \_ \_ Connect \_ v4
-   SYN: transporte de saída da camada do FWPM \_ \_ \_ \_ v4
-   SYN: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4

  
Servidor

-   SYN: \_ IPPACKET de entrada da camada FWPM \_ \_ \_ v4
-   SYN: transporte de entrada da camada do FWPM \_ \_ \_ \_ v4
-   SYN: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   SYN-ACK: \_ transporte de saída de camada FWPM \_ \_ \_ v4
-   SYN-ACK: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4

  
Cliente

-   SYN-ACK: \_ entrada da camada FWPM \_ \_ IPPACKET \_ v4
-   SYN-ACK: FWPM \_ de \_ transporte de entrada da camada \_ \_ v4
-   O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4
-   ACK: \_ transporte de saída da camada FWPM \_ \_ \_ v4
-   ACK: FWPM \_ IPPACKET de saída da camada \_ \_ \_ v4

  
Servidor

-   ACK: \_ \_ \_ IPPACKET v4 de entrada na camada FWPM \_
-   ACK: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   O \_ fluxo de Ale de camada de FWPM \_ \_ \_ estabeleceu \_ v4
-   A escuta é concluída. O servidor pode executar uma aceitação.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN recebido sem escuta na porta ou no protocolo

Servidor (receptor)

-   SYN: \_ IPPACKET de entrada da camada FWPM \_ \_ \_ v4
-   SYN: \_ \_ \_ \_ descarte v4 de transporte de entrada da camada FWPM \_
-   RST: \_ transporte de saída de camada FWPM \_ \_ \_ v4
-   RST: \_ IPPACKET de saída da camada FWPM \_ \_ \_ v4

> [!Note]  
> O TCP SYN sem nenhum ponto de extremidade é indicado em descarte de transporte com uma condição de erro específica. Bloquear este pacote no descarte de transporte para fazer com que a pilha não envie o evento correspondente (RST). Para obter um exemplo de filtragem de modo furtivo, consulte [impedindo a verificação de porta](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Dados transmitidos por uma conexão TCP

<dl> Cliente (remetente)

-   Enviar
-   dados: \_ fluxo de camada FWPM \_ \_ v4
-   Segmentos TCP: \_ v4 de \_ transporte de saída da camada FWPM \_ \_
-   Datagramas IP: \_ \_ \_ IPPACKET v4 de saída da camada FWPM \_

  
Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Segmentos TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   dados: \_ fluxo de camada FWPM \_ \_ v4
-   Os dados estão disponíveis para leitura.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Reautorização bem-sucedida de um pacote TCP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Segmento TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   Segmento TCP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   dados: \_ \_ fluxo de camada FWPM \_ V4 (entrada)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Falha na Reautorização de um pacote TCP

Servidor (receptor)

-   Datagramas IP: \_ \_ \_ IPPACKET v4 de entrada da camada FWPM \_
-   Segmento TCP: \_ transporte de entrada da camada FWPM \_ \_ \_ v4
-   Segmento TCP: \_ aceitação de \_ recepção de autenticação Ale de camada de FWPM \_ \_ \_ \_ v4
-   Segmento TCP: FWPM \_ camada \_ de \_ autenticação \_ Ale \_ aceitar aceitação \_ v4 \_ descartar

## <a name="tcp-connection-termination"></a>Término da conexão TCP

A terminação de conexão TCP não é indicada em nenhuma camada WFP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




