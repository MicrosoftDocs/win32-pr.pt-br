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
# <a name="include-files"></a><span data-ttu-id="7dbbb-103">Arquivos de inclusão</span><span class="sxs-lookup"><span data-stu-id="7dbbb-103">Include Files</span></span>

<span data-ttu-id="7dbbb-104">O arquivo de inclusão original para uso com o Windows Sockets 1,1 era o arquivo de cabeçalho *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="7dbbb-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="7dbbb-105">Para facilitar a portabilidade do código-fonte existente com base em soquetes UNIX do Berkeley para o Windows Sockets, os kits de desenvolvimento do Windows Sockets para Winsock 1,1 foram incentivados a serem fornecidos com vários arquivos de inclusão com os mesmos nomes dos arquivos de inclusão padrão do UNIX (os arquivos de cabeçalho *sys/socket. h* e ARPA/inet. h, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="7dbbb-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="7dbbb-106">No entanto, esses arquivos de cabeçalho Winsock de nome semelhante simplesmente continham uma diretiva para incluir o arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="7dbbb-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="7dbbb-107">Quando o Windows Sockets 2 foi lançado, o arquivo de inclusão primário para uso com o Windows Sockets foi renomeado para *Winsock2. h*.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="7dbbb-108">O arquivo de cabeçalho *Winsock. h* original mais antigo para o Winsock 1,1 também foi retido para compatibilidade com aplicativos mais antigos.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="7dbbb-109">O desenvolvimento de aplicativos compatíveis com o Winsock 1,1 foi preterido desde que o Windows 2000 foi lançado.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="7dbbb-110">Todos os aplicativos agora devem usar o uso da diretiva *Winsock2. h* em arquivos de origem do aplicativo Winsock.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="7dbbb-111">O arquivo de cabeçalho *Winsock2. h* contém a maioria das funções, estruturas e definições do Winsock.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="7dbbb-112">O arquivo de cabeçalho *Ws2tcpip. h* contém definições introduzidas no documento WinSock 2 Protocol-Specific anexo para TCP/IP que inclui funções e estruturas mais recentes usadas para recuperar endereços IP.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="7dbbb-113">Isso inclui a família de funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que fornecem resolução de nomes para endereços IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="7dbbb-114">O arquivo de cabeçalho *Ws2tcpip. h* só será necessário se essas funções de nomenclatura independentes de IP forem exigidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="7dbbb-115">O arquivo de cabeçalho *mswsock. h* contém definições para extensões específicas da Microsoft para o Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), por exemplo).</span><span class="sxs-lookup"><span data-stu-id="7dbbb-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="7dbbb-116">O arquivo de cabeçalho *mswsock. h* normalmente não é necessário, a menos que essas extensões específicas da Microsoft sejam usadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="7dbbb-117">O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="7dbbb-118">Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="7dbbb-119">Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="7dbbb-120">As declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="7dbbb-121">A \_ macro de Lean \_ e Mean do Win32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="7dbbb-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="7dbbb-122">Um exemplo ilustrando isso é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="7dbbb-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="7dbbb-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7dbbb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dbbb-124">Criando um aplicativo Winsock básico</span><span class="sxs-lookup"><span data-stu-id="7dbbb-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="7dbbb-125">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="7dbbb-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="7dbbb-126">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="7dbbb-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="7dbbb-127">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="7dbbb-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
