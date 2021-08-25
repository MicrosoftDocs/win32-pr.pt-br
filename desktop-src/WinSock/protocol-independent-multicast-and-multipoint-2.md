---
description: Windows O Sockets 2 fornece um método genérico para utilizar os recursos do MultiPoint e multicast dos transportes.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multicast e MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238949f017c2ecb910b533d12a809aa1c04af02e64d08aa0ef4e8d4f3d39b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857896"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent multicast e MultiPoint

Windows O Sockets 2 fornece um método genérico para utilizar os recursos do MultiPoint e multicast dos transportes. Esse método genérico implementa esses recursos da mesma forma que permite que os recursos básicos de transporte de dados de vários protocolos de transporte sejam acessados. O termo MultiPoint, é usado daqui em diante para se referir a comunicações de multicast e de MultiPoint.

As implementações atuais do MultiPoint (por exemplo, multicast de IP, ST-II, T. 120 e ATM UNI) variam muito. Como os nós ingressam em uma sessão do MultiPoint, se um nó específico é designado como um nó central ou raiz e se os dados são trocados entre todos os nós ou somente entre um nó raiz e os vários nós folha diferem entre as implementações. a estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para Windows sockets 2 é usada para declarar os vários atributos do multipoint de um protocolo. examinando esses atributos, o programador sabe quais convenções seguir com as funções aplicáveis do Windows sockets 2 para configurar, utilizar e subdividir as sessões do multipoint.

O seguinte resume os recursos do Winsock que dão suporte ao MultiPoint:

-   Bits de dois atributos na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatro sinalizadores definidos para o parâmetro *dwFlags* da função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Uma função, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para adicionar nós folha em uma sessão do MultiPoint
-   Dois códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar o loopback do MultiPoint e estabelecer o escopo para transmissões multicast. (O último corresponde ao parâmetro de tempo de vida ou TTL do IP multicast.)

> [!Note]  
> a inclusão desses recursos do multipoint no Windows sockets 2 não impede que um aplicativo use uma interface dependente de protocolo existente, como as opções de soquete Deering para multicast de IP.

 

consulte [semântica do multipoint e Multicast](multipoint-and-multicast-semantics-2.md) para obter informações detalhadas sobre como os vários esquemas do multipoint são caracterizados e como os recursos aplicáveis do Windows sockets 2 são utilizados.

 

 
