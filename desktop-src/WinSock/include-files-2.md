---
description: o arquivo de inclusão original para uso com Windows sockets 1,1 era o arquivo de cabeçalho Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Arquivos de inclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051524"
---
# <a name="include-files"></a>Arquivos de inclusão

o arquivo de inclusão original para uso com Windows sockets 1,1 era o arquivo de cabeçalho *Winsock. h* . para facilitar a portabilidade do código-fonte existente com base em soquetes de UNIX de Berkeley para Windows soquetes, os Windows sockets development kits para Winsock 1,1 foram incentivados a serem fornecidos com vários arquivos de inclusão com os mesmos nomes dos arquivos de UNIX padrão (os arquivos de cabeçalho *sys/socket. h* e arpa/inet. h, por exemplo). No entanto, esses arquivos de cabeçalho Winsock de nome semelhante simplesmente continham uma diretiva para incluir o arquivo de cabeçalho *Winsock2. h* .

quando o Windows sockets 2 foi liberado, o arquivo de inclusão primário para uso com Windows soquetes foi renomeado para *Winsock2. h*. O arquivo de cabeçalho *Winsock. h* original mais antigo para o Winsock 1,1 também foi retido para compatibilidade com aplicativos mais antigos. o desenvolvimento de aplicativos compatíveis com o Winsock 1,1 foi preterido desde que Windows 2000 foi lançado. Todos os aplicativos agora devem usar o uso da diretiva *Winsock2. h* em arquivos de origem do aplicativo Winsock.

O arquivo de cabeçalho *Winsock2. h* contém a maioria das funções, estruturas e definições do Winsock. O arquivo de cabeçalho *Ws2tcpip. h* contém definições introduzidas no documento WinSock 2 Protocol-Specific anexo para TCP/IP que inclui funções e estruturas mais recentes usadas para recuperar endereços IP. Isso inclui a família de funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que fornecem resolução de nomes para endereços IPv4 ou IPv6. O arquivo de cabeçalho *Ws2tcpip. h* só será necessário se essas funções de nomenclatura independentes de IP forem exigidas pelo aplicativo.

o arquivo de cabeçalho *Mswsock. h* contém definições para extensões específicas da Microsoft para os soquetes de Windows 2 ([**transmitfile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), por exemplo). O arquivo de cabeçalho *mswsock. h* normalmente não é necessário, a menos que essas extensões específicas da Microsoft sejam usadas pelo aplicativo.

o arquivo de cabeçalho *Winsock2. h* inclui internamente elementos principais do arquivo de cabeçalho *Windows. h* , de modo que normalmente não há uma \# linha de inclusão para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock. se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro MEAN e média do WIN32. por motivos históricos, o cabeçalho *Windows. h* usa como padrão a inclusão do arquivo de cabeçalho *Winsock. h* para Windows sockets 1,1. as declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows sockets 2. a \_ macro de LEAN \_ e MEAN do WIN32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* . Um exemplo ilustrando isso é mostrado abaixo.


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

 

 
