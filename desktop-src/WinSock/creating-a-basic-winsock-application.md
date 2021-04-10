---
description: Como criar um aplicativo básico do Windows Sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Criando um aplicativo Winsock básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090400"
---
# <a name="creating-a-basic-winsock-application"></a>Criando um aplicativo Winsock básico

**Para criar um aplicativo Winsock básico**

1.  Crie um novo projeto vazio.
2.  Adicione um arquivo de origem C++ vazio ao projeto.
3.  Verifique se o ambiente de compilação refere-se aos diretórios include, lib e src do SDK (Software Development Kit) do Microsoft Windows ou do SDK (Software Development Kit) anterior da plataforma.
4.  Verifique se o ambiente de compilação é vinculado ao arquivo de biblioteca do Winsock Ws2 \_ 32. lib. Os aplicativos que usam o Winsock devem ser vinculados ao \_ arquivo de biblioteca Ws2 32. lib. O \# Comentário pragma indica ao vinculador que o arquivo *Ws2 \_ 32. lib* é necessário.
5.  Comece a programar o aplicativo Winsock. Use a API do Winsock incluindo os arquivos de cabeçalho do Winsock 2. O arquivo de cabeçalho *Winsock2. h* contém a maioria das funções, estruturas e definições do Winsock. O arquivo de cabeçalho *Ws2tcpip. h* contém definições introduzidas no documento WinSock 2 Protocol-Specific anexo para TCP/IP que inclui funções e estruturas mais recentes usadas para recuperar endereços IP.
    > [!Note]  
    > Stdio. h é usado para entrada e saída padrão, especificamente a função **printf ()** .

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> O arquivo de cabeçalho *Iphlpapi. h* será necessário se um aplicativo estiver usando as APIs auxiliares de IP. Quando o arquivo de cabeçalho *Iphlpapi. h* é necessário, a \# linha de inclusão para o arquivo de cabeçalho *Winsock2. h* deve ser colocada antes da \# linha de inclusão para o arquivo de cabeçalho *Iphlpapi. h* .
>
> O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock. Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32. Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1. As declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2,0. A \_ macro de Lean \_ e Mean do Win32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* . Um exemplo ilustrando isso é mostrado abaixo.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Próxima etapa: [inicializando o Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Sobre servidores e clientes](about-clients-and-servers.md)
</dt> </dl>

 

 



