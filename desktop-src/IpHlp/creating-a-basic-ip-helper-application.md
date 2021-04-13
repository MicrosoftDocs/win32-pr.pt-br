---
description: Como criar um aplicativo auxiliar de IP básico.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Criando um aplicativo auxiliar de IP básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297702"
---
# <a name="creating-a-basic-ip-helper-application"></a>Criando um aplicativo auxiliar de IP básico

**Para criar um aplicativo auxiliar de IP básico**

1.  Crie um novo projeto vazio.
2.  Adicione um arquivo de origem C++ vazio ao projeto.
3.  Verifique se o ambiente de compilação refere-se aos diretórios include, lib e src do SDK (Software Development Kit) da plataforma.
4.  Verifique se o ambiente de compilação é vinculado ao arquivo de biblioteca auxiliar de IP Iphlpapi. lib e ao arquivo de biblioteca do Winsock WS2 \_ 32. lib.
    > [!Note]  
    > Algumas funções básicas do Winsock são usadas para retornar valores de endereço IP e outras informações.

     

5.  Comece a programar o aplicativo auxiliar de IP. Use a API do IP Helper, incluindo o arquivo de cabeçalho do auxiliar de IP.

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > O arquivo de cabeçalho *Iphlpapi. h* é necessário para aplicativos que usam as funções auxiliares de IP. O arquivo de cabeçalho *Iphlpapi. h* inclui automaticamente outros arquivos de cabeçalhos com estruturas e enumerações usadas pelas funções auxiliares de IP.
    >
    > As novas funções auxiliares de IP introduzidas no Windows Vista e versões posteriores são definidas no arquivo de cabeçalho *Netioapi. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Iphlpapi. h* . O arquivo de cabeçalho *Netioapi. h* nunca deve ser usado diretamente.
    >
    > Muitas das estruturas e enumerações usadas pelas funções auxiliares de IP são definidas nos arquivos de cabeçalho *Iprtrmib. h*, *ipexport. h* e *Iptypes. h* . Esses arquivos de cabeçalho são incluídos automaticamente no arquivo de cabeçalho *Iphlpapi. h* e nunca devem ser usados diretamente.
    >
    > No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada. Algumas das estruturas agora são definidas nos arquivos de cabeçalho *Ipmib. h*, *Tcpmib. h* e *Udpmib. h* , não no arquivo de cabeçalho *Iprtrmib. h* . O arquivo de cabeçalho *Ipmib. h* inclui automaticamente o arquivo de cabeçalho *Ifmib. h* . Observe que esses arquivos de cabeçalho são incluídos automaticamente no *Iprtrmib. h*, que é incluído automaticamente no arquivo de cabeçalho *Iphlpapi. h* .
    >
    > O arquivo de cabeçalho *Winsock2. h* para o Windows sockets 2,0 é exigido pela maioria dos aplicativos que usam as APIs auxiliares de IP. Quando o arquivo de cabeçalho *Winsock2. h* é necessário, a \# linha de inclusão desse arquivo deve ser colocada antes da \# linha de inclusão para o arquivo de cabeçalho *Iphlpapi. h* .
    >
    > O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos auxiliares de IP. Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32. Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1. As declarações no arquivo de cabeçalho *Winsock. h* para o Windows sockets 1,1 entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2,0. A \_ macro de Lean \_ e Mean do Win32 impede que \_ o arquivo de cabeçalho *Winsock. h* seja incluído pelo arquivo de cabeçalho do *Windows. h* . Um exemplo ilustrando isso é mostrado abaixo.

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Esse aplicativo auxiliar de IP básico usa apenas algumas estruturas de dados de endereço IP e o endereço IP para funções de conversão de cadeia de caracteres do Windows Sockets 2,0. Essas funções do Windows Sockets podem ser usadas sem chamar o [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar recursos do Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando terminar de usar esses recursos.
    >
    > Em aplicativos auxiliares de IP que usam outras funções do Winsock que não sejam esse endereço IP para funções de cadeia de caracteres, a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve ser chamada para inicializar recursos do Windows Sockets antes de chamar qualquer função do Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) deve ser chamado quando o aplicativo é feito usando recursos do Windows Sockets.

     

    > [!Note]
    >
    > O arquivo de cabeçalho *stdio. h* é necessário para o uso de várias funções padrão do C neste aplicativo auxiliar de IP básico.

     

    Próxima etapa: [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 
