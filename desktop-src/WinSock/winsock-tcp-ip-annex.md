---
description: Esta seção descreve as funções TCP/IP (Protocolo TCP/IP), estruturas de dados e controles.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Winsock TCP/IP Anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5cc403f0ff7f7e6b1daeb979ae9b7ec6ab3c3bed455843cec7ae4f43469975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822360"
---
# <a name="winsock-tcpip-annex"></a>Winsock TCP/IP Anexo

Esta seção descreve as funções TCP/IP (Protocolo TCP/IP), estruturas de dados e controles.



| Elemento          | Descrição                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nomes de protocolo | TCP, UDP                                                                                                                                    |
| Descrição      | Fornece serviços de transporte pela camada de rede IP: UDP para datagramas não confiáveis, TCP para fluxos de byte confiáveis orientados a conexão. |
| Família de endereços   | **AF \_ INET,** **AF \_ INET6**                                                                                                                 |
| Arquivo de cabeçalho      | *Ws2tcpip.h*                                                                                                                                |



 

Dois tipos básicos de serviços de transporte são oferecidos: UDP (datagramas não confiáveis) e fluxos de byte orientados a conexão confiável (TCP). Além disso, opcionalmente, há suporte para um soquete bruto. Soquetes brutos permitem que um aplicativo se comunique por meio de protocolos que não são TCP e UDP, como ICMP. Soquetes brutos têm suporte nas famílias de endereços **AF \_ INET** e **AF \_ INET6** com algumas limitações.

Esta seção aborda extensões do Winsock que são específicas para protocolos TCP/IP. Ele também descreve aspectos de funções Winsock base que exigem consideração especial ou que podem apresentar um comportamento exclusivo ao usar TCP/IP.

 

 



