---
description: Ao adicionar suporte para IPv6, você deve garantir que seu aplicativo defina estruturas de dados corretamente dimensionadas.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Alterando estruturas de dados para aplicativos Winsock do IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797610"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Alterando estruturas de dados para aplicativos Winsock do IPv6

Ao adicionar suporte para IPv6, você deve garantir que seu aplicativo defina estruturas de dados corretamente dimensionadas. O tamanho de um endereço IPv6 é muito maior do que um endereço IPv4. Estruturas que são embutidas em código para lidar com o tamanho de um endereço IPv4 ao armazenar um endereço IP causarão problemas em seu aplicativo e devem ser modificadas.

Melhor prática

A melhor abordagem para garantir que suas estruturas sejam dimensionadas corretamente é usar a estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) . A estrutura de **\_ armazenamento SOCKADDR** é independente da versão do endereço IP. Quando a estrutura de **\_ armazenamento SOCKADDR** é usada para armazenar endereços IP, os endereços IPv4 e IPv6 podem ser manipulados adequadamente com uma base de código.

O exemplo a seguir, que é um trecho extraído do arquivo Server. c encontrado no apêndice B, identifica um uso apropriado da estrutura de **\_ armazenamento SOCKADDR** . Observe que a estrutura, quando usada corretamente, como mostra este exemplo, trata normalmente de um endereço IPv4 ou IPv6.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> A estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) é nova para o Windows XP.

 

Código a ser evitado

Normalmente, muitos aplicativos usaram a estrutura [**SOCKADDR**](sockaddr-2.md) para armazenar endereços independentes de protocolo ou o **SOCKADDR \_ na** estrutura de endereços IP. Nem a estrutura sockaddr nem a **SOCKADDR \_ na** estrutura é grande o suficiente para conter endereços IPv6 e, portanto, ambas são insuficientes se seu aplicativo for compatível com IPv6.

Tarefa de codificação

**Para modificar sua base de código existente de IPv4 para IPv4 e IPv6-interoperabilidade**

1.  Adquira o utilitário Checkv4.exe. O utilitário está incluído no SDK (Software Development Kit) do Microsoft Windows, que é disponibilizado por meio de sua assinatura do MSDN ou da Web como um download.
2.  Execute o utilitário Checkv4.exe em relação ao seu código. Saiba mais sobre como executar o utilitário de Checkv4.exe em seus arquivos na seção sobre como [usar o utilitário de Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  O utilitário alerta você sobre o uso de **SOCKADDR** ou **SOCKADDR \_ em** estruturas e fornece recomendações sobre como substituir por uma estrutura compatível com IPv6 [**SOCKADDR \_ armazenamento**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Substitua essas instâncias e o código associado, conforme apropriado, para usar a estrutura de **\_ armazenamento SOCKADDR** .

Como alternativa, você pode pesquisar sua base de código em busca de instâncias de **SOCKADDR** e **SOCKADDR \_ em** estruturas e alterar todo esse uso (e outro código associado, conforme apropriado) para a estrutura de **\_ armazenamento SOCKADDR** .

> [!Note]  
> As estruturas de **\_ armazenamento** **addrinfo** e SOCKADDR incluem membros da família de protocolos e endereços (**\_ família de ia** e **\_ família SS**), respectivamente. A RFC 2553 especifica o membro da **\_ família ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como um int, enquanto a **\_ família SS** é especificada como um curto; dessa forma, uma cópia direta entre esses membros resulta em um erro do compilador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock do IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso de endereços IPv4 codificados](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de interface do usuário para aplicativos Winsock do IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
