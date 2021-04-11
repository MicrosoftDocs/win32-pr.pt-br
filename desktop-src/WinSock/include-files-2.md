---
description: O arquivo de inclusão original para uso com o Windows Sockets 1,1 era o arquivo de cabeçalho Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Arquivos de inclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296349"
---
# <a name="include-files"></a>Arquivos de inclusão

O arquivo de inclusão original para uso com o Windows Sockets 1,1 era o arquivo de cabeçalho *Winsock. h* . Para facilitar a portabilidade do código-fonte existente com base em soquetes UNIX do Berkeley para o Windows Sockets, os kits de desenvolvimento do Windows Sockets para Winsock 1,1 foram incentivados a serem fornecidos com vários arquivos de inclusão com os mesmos nomes dos arquivos de inclusão padrão do UNIX (os arquivos de cabeçalho *sys/socket. h* e ARPA/inet. h, por exemplo). No entanto, esses arquivos de cabeçalho Winsock de nome semelhante simplesmente continham uma diretiva para incluir o arquivo de cabeçalho *Winsock2. h* .

Quando o Windows Sockets 2 foi lançado, o arquivo de inclusão primário para uso com o Windows Sockets foi renomeado para *Winsock2. h*. O arquivo de cabeçalho *Winsock. h* original mais antigo para o Winsock 1,1 também foi retido para compatibilidade com aplicativos mais antigos. O desenvolvimento de aplicativos compatíveis com o Winsock 1,1 foi preterido desde que o Windows 2000 foi lançado. Todos os aplicativos agora devem usar o uso da diretiva *Winsock2. h* em arquivos de origem do aplicativo Winsock.

O arquivo de cabeçalho *Winsock2. h* contém a maioria das funções, estruturas e definições do Winsock. O arquivo de cabeçalho *Ws2tcpip. h* contém definições introduzidas no documento WinSock 2 Protocol-Specific anexo para TCP/IP que inclui funções e estruturas mais recentes usadas para recuperar endereços IP. Isso inclui a família de funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que fornecem resolução de nomes para endereços IPv4 ou IPv6. O arquivo de cabeçalho *Ws2tcpip. h* só será necessário se essas funções de nomenclatura independentes de IP forem exigidas pelo aplicativo.

O arquivo de cabeçalho *mswsock. h* contém definições para extensões específicas da Microsoft para o Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), por exemplo). O arquivo de cabeçalho *mswsock. h* normalmente não é necessário, a menos que essas extensões específicas da Microsoft sejam usadas pelo aplicativo.

O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock. Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32. Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1. As declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2. A \_ macro de Lean \_ e Mean do Win32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* . Um exemplo ilustrando isso é mostrado abaixo.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)
</dt> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
