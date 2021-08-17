---
description: Um aplicativo usa a função WSAEnumProtocols para determinar quais protocolos de transporte e cadeias de protocolo estão presentes e para obter informações sobre cada um, conforme contido na estrutura de INFORMAÇÕES WSAPROTOCOL \_ associada.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Usando vários protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9e1641c8e1ed308561b9e85425005933fceac17b156d1161895f13ad06d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739956"
---
# <a name="using-multiple-protocols"></a>Usando vários protocolos

Um aplicativo usa a [**função WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para determinar quais protocolos de transporte e cadeias de protocolo estão presentes e para obter informações sobre cada um, conforme contido na estrutura [**de INFORMAÇÕES WSAPROTOCOL \_ associada.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Na maioria das instâncias, há uma única estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada protocolo ou cadeia de protocolo. No entanto, alguns protocolos apresentam vários comportamentos. Por exemplo, o protocolo SPX é orientado a mensagens (ou seja, os limites de mensagem do remetente são preservados pela rede), mas o soquete receptor pode ignorar esses limites de mensagem e tratá-los como um fluxo de byte. Portanto, duas entradas **de estrutura WSAPROTOCOL \_ INFO** diferentes podem existir para SPX– uma para cada comportamento.

No Windows Soquetes 2, várias novas famílias de endereços, tipo de soquete e valores de protocolo são exibidos. Windows Os soquetes 1.1 eram suportados por uma família de endereço único (AF INET) para IPv4 que consistia em um pequeno número de tipos de soquete conhecidos e identificadores \_ de protocolo. Windows Os soquetes 2 retêm a família de endereços existente, o tipo de soquete e os identificadores de protocolo por motivos de compatibilidade, mas também dá suporte a novos valores de família de endereços para novos protocolos de transporte com novos tipos de mídia.

Identificadores novos e exclusivos não são necessariamente bem conhecidos, mas isso não deve representar um problema. Os aplicativos que precisam ser independentes de protocolo são incentivados a selecionar um protocolo com base em sua adequação, em vez dos valores atribuídos a seus parâmetros de protocolo ou tipo *de* soquete. *\_* A adequação do protocolo é indicada pelos atributos de comunicação, como fluxo de mensagem versus byte e reliable-versus-unreliable, que estão contidos na estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) do protocolo. Selecionar protocolos com base na adequação em vez de nomes de protocolo e tipos de soquete conhecidos permite que os aplicativos independentes de protocolo aproveitem novos protocolos de transporte e seus tipos de mídia associados, conforme eles se tornam disponíveis.

A metade do servidor de um aplicativo cliente/servidor se beneficia ao estabelecer soquetes de escuta em todos os protocolos de transporte adequados. Em seguida, o cliente pode estabelecer sua conexão usando qualquer protocolo adequado. Por exemplo, isso permite que um aplicativo cliente não seja modificado se ele estava em execução em um sistema de área de trabalho conectado por meio de LAN ou em um laptop usando uma rede sem fio.

 

 
