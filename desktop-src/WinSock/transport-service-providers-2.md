---
description: Provedores de serviços de transporte e Windows soquetes (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Provedores de serviços de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860db59b5a27d19cdc5263069161f105d79e15cfd7353789f8fdcf9944799ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927167"
---
# <a name="transport-service-providers"></a>Provedores de serviços de transporte

Um determinado provedor de serviços de transporte dá suporte a um ou mais protocolos. Por exemplo, um provedor TCP/IP forneceria, no mínimo, os protocolos TCP e UDP, enquanto um provedor IPX/SPX pode fornecer IPX, SPX e SPX II. Cada protocolo com suporte de um provedor específico é descrito por uma estrutura [**INFO WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) e o conjunto total dessas estruturas pode ser pensado como o catálogo de protocolos instalados. Os aplicativos podem recuperar o conteúdo desse catálogo (para obter mais informações, consulte [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)) e examinando as estruturas **de INFORMAÇÕES \_ WSAPROTOCOL** disponíveis, descubra os atributos de comunicação associados a cada protocolo.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Protocolos em camadas e cadeias de protocolo na SPI

Windows Os soquetes 2 acomodam o conceito de um protocolo em camadas. Um protocolo em camadas é aquele que implementa apenas funções de comunicação de nível superior, enquanto depende de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto. Um exemplo desse protocolo em camadas seria uma camada de segurança que adiciona protocolo ao processo de estabelecimento de conexão para executar a autenticação e estabelecer um esquema de criptografia mutuamente estabelecido. Esse protocolo de segurança geralmente exigiria os serviços de um protocolo de transporte confiável subjacente, como TCP ou SPX. O termo protocolo base refere-se a um protocolo como TCP ou SPX que é totalmente capaz de executar comunicações de dados com um ponto de extremidade remoto e o termo protocolo em camadas é usado para descrever um protocolo que não pode ficar sozinho. Em seguida, uma cadeia de protocolos seria definida como um ou mais protocolos em camadas juntos e ancorados por um protocolo base.

Essa cadeia de caracteres de protocolos em camadas e protocolos base em cadeias pode ser realizada organizando os protocolos em camadas para dar suporte à SPI winsock em suas bordas superior e inferior. Uma estrutura [**especial de \_ INFORMAÇÕES WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) é criada que se refere à cadeia de protocolo como um todo e que descreve a ordem explícita na qual os protocolos em camadas são unidos. Isso é ilustrado no gráfico a seguir.

![cadeia de protocolos](images/ovrvw2-3.png)

 

 
