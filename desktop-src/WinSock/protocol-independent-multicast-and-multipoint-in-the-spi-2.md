---
description: Recursos de transmissão e multicast do Windows Sockets (Winsock) e de protocolos de transporte independentes.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multicast e MultiPoint no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091384"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multicast e MultiPoint no SPI

Assim como o Windows Sockets 2 permite que os recursos básicos de transporte de dados de vários protocolos de transporte sejam acessados de maneira genérica, ele também fornece uma maneira genérica de usar os recursos de MultiPoint e multicast de transportes que implementam esses recursos. Para simplificar, o termo *MultiPoint* é usado daqui em diante para se referir a comunicações de multicast e de MultiPoint.

As implementações atuais do MultiPoint (por exemplo, multicast de IP, ST-II, T. 120, ATM UNI) variam muito em relação ao modo como os nós ingressam em uma sessão do MultiPoint, se um nó específico é designado como um nó central ou raiz e se os dados são trocados entre todos os nós ou somente entre um nó raiz e vários nós folha. A estrutura de [**\_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) do Windows Sockets 2 é usada para declarar os atributos do MultiPoint de um protocolo. Examinando esses atributos, o programador saberá quais convenções seguir no uso das funções Winsock aplicáveis para configurar, usar e subdividir as sessões do MultiPoint.

Os recursos do Windows Sockets 2 que oferecem suporte a multicast podem ser resumidos da seguinte maneira:

-   Três bits de atributo na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatro sinalizadores definidos para o parâmetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Uma função, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), para adicionar nós folha em uma sessão do MultiPoint.
-   Dois códigos de comando [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para controlar o loopback do MultiPoint e estabelecer o escopo para transmissões multicast. (O último corresponde ao parâmetro de tempo de vida ou TTL do IP multicast.)

> [!Note]  
> A inclusão desses recursos do MultiPoint no Windows Sockets 2 não impede que um provedor de serviços também dê suporte a uma interface dependente de protocolo existente, como as opções de Soquete Deering para multicast de IP.

 

 

 
