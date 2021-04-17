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
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="d1661-103">Alterando estruturas de dados para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d1661-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="d1661-104">Ao adicionar suporte para IPv6, você deve garantir que seu aplicativo defina estruturas de dados corretamente dimensionadas.</span><span class="sxs-lookup"><span data-stu-id="d1661-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="d1661-105">O tamanho de um endereço IPv6 é muito maior do que um endereço IPv4.</span><span class="sxs-lookup"><span data-stu-id="d1661-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="d1661-106">Estruturas que são embutidas em código para lidar com o tamanho de um endereço IPv4 ao armazenar um endereço IP causarão problemas em seu aplicativo e devem ser modificadas.</span><span class="sxs-lookup"><span data-stu-id="d1661-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="d1661-107">Melhor prática</span><span class="sxs-lookup"><span data-stu-id="d1661-107">Best Practice</span></span>

<span data-ttu-id="d1661-108">A melhor abordagem para garantir que suas estruturas sejam dimensionadas corretamente é usar a estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1661-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="d1661-109">A estrutura de **\_ armazenamento SOCKADDR** é independente da versão do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="d1661-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="d1661-110">Quando a estrutura de **\_ armazenamento SOCKADDR** é usada para armazenar endereços IP, os endereços IPv4 e IPv6 podem ser manipulados adequadamente com uma base de código.</span><span class="sxs-lookup"><span data-stu-id="d1661-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="d1661-111">O exemplo a seguir, que é um trecho extraído do arquivo Server. c encontrado no apêndice B, identifica um uso apropriado da estrutura de **\_ armazenamento SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="d1661-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="d1661-112">Observe que a estrutura, quando usada corretamente, como mostra este exemplo, trata normalmente de um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="d1661-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


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
> <span data-ttu-id="d1661-113">A estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) é nova para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1661-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="d1661-114">Código a ser evitado</span><span class="sxs-lookup"><span data-stu-id="d1661-114">Code To Avoid</span></span>

<span data-ttu-id="d1661-115">Normalmente, muitos aplicativos usaram a estrutura [**SOCKADDR**](sockaddr-2.md) para armazenar endereços independentes de protocolo ou o **SOCKADDR \_ na** estrutura de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="d1661-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="d1661-116">Nem a estrutura sockaddr nem a **SOCKADDR \_ na** estrutura é grande o suficiente para conter endereços IPv6 e, portanto, ambas são insuficientes se seu aplicativo for compatível com IPv6.</span><span class="sxs-lookup"><span data-stu-id="d1661-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="d1661-117">Tarefa de codificação</span><span class="sxs-lookup"><span data-stu-id="d1661-117">Coding Task</span></span>

<span data-ttu-id="d1661-118">**Para modificar sua base de código existente de IPv4 para IPv4 e IPv6-interoperabilidade**</span><span class="sxs-lookup"><span data-stu-id="d1661-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="d1661-119">Adquira o utilitário Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="d1661-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="d1661-120">O utilitário está incluído no SDK (Software Development Kit) do Microsoft Windows, que é disponibilizado por meio de sua assinatura do MSDN ou da Web como um download.</span><span class="sxs-lookup"><span data-stu-id="d1661-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="d1661-121">Execute o utilitário Checkv4.exe em relação ao seu código.</span><span class="sxs-lookup"><span data-stu-id="d1661-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="d1661-122">Saiba mais sobre como executar o utilitário de Checkv4.exe em seus arquivos na seção sobre como [usar o utilitário de Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="d1661-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="d1661-123">O utilitário alerta você sobre o uso de **SOCKADDR** ou **SOCKADDR \_ em** estruturas e fornece recomendações sobre como substituir por uma estrutura compatível com IPv6 [**SOCKADDR \_ armazenamento**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1661-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="d1661-124">Substitua essas instâncias e o código associado, conforme apropriado, para usar a estrutura de **\_ armazenamento SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="d1661-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="d1661-125">Como alternativa, você pode pesquisar sua base de código em busca de instâncias de **SOCKADDR** e **SOCKADDR \_ em** estruturas e alterar todo esse uso (e outro código associado, conforme apropriado) para a estrutura de **\_ armazenamento SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="d1661-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="d1661-126">As estruturas de **\_ armazenamento** **addrinfo** e SOCKADDR incluem membros da família de protocolos e endereços (**\_ família de ia** e **\_ família SS**), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d1661-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="d1661-127">A RFC 2553 especifica o membro da **\_ família ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como um int, enquanto a **\_ família SS** é especificada como um curto; dessa forma, uma cópia direta entre esses membros resulta em um erro do compilador.</span><span class="sxs-lookup"><span data-stu-id="d1661-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d1661-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1661-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1661-129">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d1661-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="d1661-130">Soquetes de pilha dupla para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d1661-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="d1661-131">Chamadas de função para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="d1661-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="d1661-132">Uso de endereços IPv4 codificados</span><span class="sxs-lookup"><span data-stu-id="d1661-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="d1661-133">Problemas de interface do usuário para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d1661-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="d1661-134">Protocolos subjacentes para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="d1661-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
