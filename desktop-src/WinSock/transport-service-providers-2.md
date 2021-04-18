---
description: Provedores de serviço de transporte e Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Provedores de serviço de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760952"
---
# <a name="transport-service-providers"></a>Provedores de serviço de transporte

Um determinado provedor de serviço de transporte dá suporte A um ou mais protocolos. Por exemplo, um provedor TCP/IP forneceria, como um mínimo, os protocolos TCP e UDP, enquanto um provedor de IPX/SPX pode fornecer IPX, SPX e SPX II. Cada protocolo com suporte de um provedor específico é descrito por uma estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) e o conjunto total dessas estruturas pode ser considerado como o catálogo de protocolos instalados. Os aplicativos podem recuperar o conteúdo deste catálogo (para obter mais informações, consulte [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)) e examinando as estruturas de **\_ informações do WSAPROTOCOL** disponíveis, descubra os atributos de comunicação associados a cada protocolo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolos em camadas e cadeias de protocolo no SPI

O Windows Sockets 2 acomoda o conceito de um protocolo em camadas. Um protocolo em camadas é aquele que implementa apenas funções de comunicação de nível mais alto, enquanto dependem de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto. Um exemplo de tal protocolo em camadas seria uma camada de segurança que adiciona o protocolo ao processo de estabelecimento da conexão para executar a autenticação e estabelecer um esquema de criptografia acordado mutuamente. Esse protocolo de segurança, em geral, exigiria os serviços de um protocolo de transporte confiável subjacente, como TCP ou SPX. O termo protocolo base refere-se a um protocolo como TCP ou SPX, que é totalmente capaz de executar comunicações de dados com um ponto de extremidade remoto e o termo protocolo em camadas é usado para descrever um protocolo que não pode ser autônomo. Uma cadeia de protocolos seria então definida como um ou mais protocolos em camadas são agrupados e ancorados por um protocolo base.

Essa cadeia de caracteres de protocolos em camadas e protocolos de base em cadeias pode ser realizada organizando os protocolos em camadas para dar suporte à SPI do Winsock nas bordas superiores e inferiores. Uma estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial é criada, que se refere à cadeia de protocolos como um todo e que descreve a ordem explícita na qual os protocolos em camadas são associados. Isso é ilustrado no gráfico a seguir.

![Cadeia de protocolos](images/ovrvw2-3.png)

 

 
