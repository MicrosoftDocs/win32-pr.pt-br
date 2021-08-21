---
description: A família de endereços IPX define a estrutura de endereçamento para protocolos que usam o endereçamento de soquete IPX padrão. Para esses transportes, um endereço de ponto de extremidade consiste em um número de rede, um endereço de nó e um número de soquete.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Família de endereços AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3915eefab8e6fc6c18cf4e2b81835b8c6821d0cdd65f5683f509504d4d2c24bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112799"
---
# <a name="af_ipx-address-family"></a>\_Família de endereços IPX AF

A família de endereços IPX define a estrutura de endereçamento para protocolos que usam o endereçamento de soquete IPX padrão. Para esses transportes, um endereço de ponto de extremidade consiste em um número de rede, um endereço de nó e um número de soquete.

O número de rede é um domínio administrativo e normalmente nomeia um único segmento Ethernet ou token ring. O número do nó é um endereço físico de uma estação. A combinação de NET e node formam um endereço de estação exclusivo que presume ser exclusivo no mundo. Os números de nó e de rede são representados em texto ASCII em uma notação de bloco ou tracejado como: ' 0101a040, 00001b498765 ' ou ' 01-01-a0-40, 00-00-1B-49-87-65 '. Os zeros à esquerda não precisam estar presentes.

O número de soquete IPX é um número de serviço de rede/transporte muito parecido com um número de porta TCP e não deve ser confundido com o descritor de soquete Winsock. Os números de soquete IPX são globais para a estação final e não podem ser associados a endereços de rede/nó específicos. Por exemplo, se a estação final tiver duas placas de interface de rede, um soquete associado poderá enviar e receber em ambos os cartões. Em particular, os soquetes de datagramas receberão datagramas de difusão em ambos os cartões.

> [!Caution]  
> SOCKADDR \_ IPX tem 14 bytes de comprimento e é menor que a estrutura de referência de [**SOCKADDR**](sockaddr-2.md) de 16 bytes. As implementações de IPX/SPX podem aceitar o comprimento de 16 bytes, bem como o comprimento real. Se você usar \_ o sockaddr IPX e um comprimento embutido em código de 16 bytes, a implementação poderá assumir que ele tem acesso aos 2 bytes após sua estrutura.

 



| Campo           | Valor                                    |
|-----------------|------------------------------------------|
| **\_família SA**  | Endereço IPX da família \_ de endereços em ordem de host.    |
| **\_Netnum SA**  | Identificador de rede IPX na ordem de rede. |
| **\_Nodenum SA** | Endereço do nó de estação, liberado à direita.     |
| **\_Soquete SA**  | Número de soquete IPX na ordem de rede.      |



 

 

 



