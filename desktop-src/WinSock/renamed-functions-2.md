---
description: Em dois casos, era necessário renomear funções que são usadas em soquetes de Berkeley para evitar conflitos com outras funções da API do Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funções renomeadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827737"
---
# <a name="renamed-functions"></a>Funções renomeadas

Em dois casos, era necessário renomear funções que são usadas em soquetes de Berkeley para evitar conflitos com outras funções da API do Microsoft Windows.

## <a name="close-and-closesocket"></a>Fechar e fechamento

Os soquetes são representados por descritores de arquivo padrão em Berkeley Sockets, portanto, a função **Close** pode ser usada para fechar soquetes, bem como arquivos regulares. Embora nada no Windows Sockets impeça uma implementação de usar identificadores de arquivo regulares para identificar soquetes, nada também exige isso. No Windows, os soquetes devem ser fechados usando a rotina [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) . NO Windows, o uso da função **Close** para fechar um soquete está incorreto e os efeitos dessa especificação são indefinidos.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>IOCTL e ioctlsocket/WSAIoctl

Vários sistemas de tempo de execução de linguagem C usam os IOCTLs para fins não relacionados ao Windows Sockets. Como consequência, a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) e a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) foram definidas para lidar com funções de soquete que foram executadas pelo **IOCTL** e pelo **fcntl** na distribuição de software Berkeley.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



