---
description: Ao adicionar suporte para IPv6, você deve garantir que seu aplicativo defina estruturas de dados dimensionadas corretamente.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Alterando estruturas de dados para aplicativos Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741546"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Alterando estruturas de dados para aplicativos Winsock IPv6

Ao adicionar suporte para IPv6, você deve garantir que seu aplicativo defina estruturas de dados dimensionadas corretamente. O tamanho de um endereço IPv6 é muito maior do que um endereço IPv4. Estruturas em código para lidar com o tamanho de um endereço IPv4 ao armazenar um endereço IP causarão problemas em seu aplicativo e devem ser modificadas.

Melhor prática

A melhor abordagem para garantir que suas estruturas sejam dimensionadas corretamente é usar a estrutura [**DE ARMAZENAMENTO \_ SOCKADDR.**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) A **estrutura DE \_ ARMAZENAMENTO SOCKADDR** é agnostic para a versão do endereço IP. Quando a **estrutura \_ DE ARMAZENAMENTO SOCKADDR** é usada para armazenar endereços IP, os endereços IPv4 e IPv6 podem ser tratados corretamente com uma base de código.

O exemplo a seguir, que é um trecho extraído do arquivo Server.c encontrado no Apêndice B, identifica um uso apropriado da estrutura **SOCKADDR \_ STORAGE.** Observe que a estrutura, quando usada corretamente como mostra este exemplo, lida normalmente com um endereço IPv4 ou IPv6.


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
> A [**estrutura DE \_ ARMAZENAMENTO SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) é nova para Windows XP.

 

Código a ser evitado

Normalmente, muitos aplicativos usavam a estrutura [**sockaddr**](sockaddr-2.md) para armazenar endereços independentes de protocolo ou o **sockaddr \_ na** estrutura para endereços IP. Nem a estrutura sockaddr nem **o sockaddr na \_** estrutura são grandes o suficiente para manter endereços IPv6 e, portanto, ambos são insuficientes se seu aplicativo for compatível com IPv6.

Tarefa Codificação

**Para modificar sua base de código existente de IPv4 para interoperabilidade IPv4 e IPv6**

1.  Adquira o Checkv4.exe utilitário. O utilitário está incluído no SDK (Software Development Kit) do Microsoft Windows, que é disponibilizado por meio de sua assinatura do MSDN ou da Web como um download.
2.  Execute o utilitário Checkv4.exe em seu código. Saiba mais sobre como executar o utilitário Checkv4.exe em seus arquivos na seção usando [o utilitário Checkv4.exe .](using-the-checkv4-exe-utility-2.md)
3.  O utilitário alerta você sobre o uso de **sockaddr** ou **\_ sockaddr** em estruturas e fornece recomendações sobre como substituir pela estrutura compatível com IPv6 [**SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Substitua essas instâncias e o código associado, conforme apropriado, para usar a estrutura **DE ARMAZENAMENTO \_ SOCKADDR.**

Como alternativa, você pode pesquisar em sua base de código instâncias do **sockaddr** e **\_ sockaddr** em estruturas e alterar todo esse uso (e outro código associado, conforme apropriado) para a estrutura **SOCKADDR \_ STORAGE.**

> [!Note]  
> As **estruturas addrinfo** e **SOCKADDR \_ STORAGE** incluem membros de família de protocolo e endereço (**família ai \_** e **ss \_ ),** respectivamente. O RFC 2553 especifica o membro da família **\_ ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como um int, enquanto a família **\_ ss** é especificada como um curto; como tal, uma cópia direta entre esses membros resulta em um erro do compilador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia IPv6 para aplicativos Windows soquetes](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso de endereços IPv4 em código](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interface do Usuário problemas para aplicativos Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
