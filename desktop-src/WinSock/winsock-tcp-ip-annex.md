---
description: Esta seção descreve as funções do protocolo TCP/IP, as estruturas de dados e os controles.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164862"
---
# <a name="winsock-tcpip-annex"></a>Anexo TCP/IP do Winsock

Esta seção descreve as funções do protocolo TCP/IP, as estruturas de dados e os controles.



| Elemento          | Descrição                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nome (s) de protocolo | TCP, UDP                                                                                                                                    |
| Descrição      | Fornece serviços de transporte pela camada de rede IP: UDP para datagramas não confiáveis, TCP para fluxos de bytes confiáveis e orientados a conexões. |
| Família de endereços   | **AF \_ INET**, **AF \_ INET6**                                                                                                                 |
| Arquivo de cabeçalho      | *Ws2tcpip. h*                                                                                                                                |



 

Dois tipos básicos de serviços de transporte são oferecidos: datagrams (UDP) não confiáveis e orientado a conexão confiável – fluxos de bytes (TCP). Além disso, um soquete bruto tem suporte opcional. Os soquetes brutos permitem que um aplicativo se comunique por meio de protocolos diferentes de TCP e UDP, como ICMP. Os soquetes brutos têm suporte nas famílias de endereços **\_ inet** e **AF \_ INET6** de AF, com algumas limitações.

Esta seção aborda extensões para Winsock que são específicas para protocolos TCP/IP. Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar um comportamento exclusivo ao usar TCP/IP.

 

 



