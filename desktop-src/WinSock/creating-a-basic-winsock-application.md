---
description: como criar um aplicativo de basic Windows sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Criando um aplicativo Winsock básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860946"
---
# <a name="creating-a-basic-winsock-application"></a>Criando um aplicativo Winsock básico

**Para criar um aplicativo Winsock básico**

1.  Crie um novo projeto vazio.
2.  Adicione um arquivo de origem C++ vazio ao projeto.
3.  verifique se o ambiente de compilação refere-se aos diretórios Include, Lib e Src do sdk (software development kit) do Microsoft Windows ou do sdk (software development kit) da plataforma anterior.
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
> o arquivo de cabeçalho *Winsock2. h* inclui internamente elementos principais do arquivo de cabeçalho *Windows. h* , de modo que normalmente não há uma \# linha de inclusão para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock. se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro MEAN e média do WIN32. por motivos históricos, o cabeçalho *Windows. h* usa como padrão a inclusão do arquivo de cabeçalho *Winsock. h* para Windows sockets 1,1. as declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows sockets 2,0. a \_ macro de LEAN \_ e MEAN do WIN32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* . Um exemplo ilustrando isso é mostrado abaixo.

 


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

 

 



