---
description: Um aplicativo usa a função WSAEnumProtocols para determinar quais protocolos de transporte e cadeias de protocolo estão presentes e para obter informações sobre cada um conforme contido na estrutura de informações do WSAPROTOCOL associada \_ .
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Usando vários protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090352"
---
# <a name="using-multiple-protocols"></a>Usando vários protocolos

Um aplicativo usa a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para determinar quais protocolos de transporte e cadeias de protocolo estão presentes e para obter informações sobre cada um conforme contido na estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associada.

Na maioria dos casos, há uma única estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada protocolo ou cadeia de protocolos. No entanto, alguns protocolos apresentam vários comportamentos. Por exemplo, o protocolo SPX é orientado a mensagens (ou seja, os limites de mensagem do remetente são preservados pela rede), mas o soquete de recebimento pode ignorar esses limites de mensagem e tratá-los como um fluxo de bytes. Portanto, duas entradas de estrutura de **\_ informações de WSAPROTOCOL** diferentes podem existir para o SPX — uma para cada comportamento.

No Windows Sockets 2, vários novos valores de família de endereços, tipos de soquete e protocolo são exibidos. O Windows Sockets 1,1 oferecia suporte a uma única família de endereços (série AF \_ ) para IPv4 que consistia em um pequeno número de tipos de soquete e identificadores de protocolo bem conhecidos. O Windows Sockets 2 retém a família de endereços existente, o tipo de soquete e os identificadores de protocolo por motivos de compatibilidade, mas também oferece suporte a novos valores de família de endereços para novos protocolos de transporte com novos tipos de mídia.

Os identificadores novos e exclusivos não são necessariamente bem conhecidos, mas isso não deve representar um problema. Os aplicativos que precisam ser independentes de protocolo são incentivados a selecionar um protocolo com base em sua adequação, em vez dos valores atribuídos aos seus parâmetros de *protocolo* ou *\_ tipo de soquete* . A adequação de protocolo é indicada pelos atributos de comunicação, como fluxo de mensagens e de bytes, e confiabilidade-versus-não confiável, que estão contidos na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de protocolo. A seleção de protocolos com base em adequação, em oposição aos nomes de protocolo e tipos de soquete conhecidos, permite que aplicativos independentes de protocolo aproveitem os novos protocolos de transporte e seus tipos de mídia associados, pois eles se tornam disponíveis.

A metade do servidor de um aplicativo cliente/servidor beneficia-se estabelecendo soquetes de escuta em todos os protocolos de transporte adequados. Em seguida, o cliente pode estabelecer sua conexão usando qualquer protocolo adequado. Por exemplo, isso permitiria que um aplicativo cliente fosse cancelado se estava sendo executado em um sistema de desktop conectado por meio de LAN ou em um laptop usando uma rede sem fio.

 

 
