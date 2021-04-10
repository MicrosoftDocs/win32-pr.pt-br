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
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="a11d0-103">Criando um aplicativo Winsock básico</span><span class="sxs-lookup"><span data-stu-id="a11d0-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="a11d0-104">**Para criar um aplicativo Winsock básico**</span><span class="sxs-lookup"><span data-stu-id="a11d0-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="a11d0-105">Crie um novo projeto vazio.</span><span class="sxs-lookup"><span data-stu-id="a11d0-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="a11d0-106">Adicione um arquivo de origem C++ vazio ao projeto.</span><span class="sxs-lookup"><span data-stu-id="a11d0-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="a11d0-107">Verifique se o ambiente de compilação refere-se aos diretórios include, lib e src do SDK (Software Development Kit) do Microsoft Windows ou do SDK (Software Development Kit) anterior da plataforma.</span><span class="sxs-lookup"><span data-stu-id="a11d0-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="a11d0-108">Verifique se o ambiente de compilação é vinculado ao arquivo de biblioteca do Winsock Ws2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="a11d0-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="a11d0-109">Os aplicativos que usam o Winsock devem ser vinculados ao \_ arquivo de biblioteca Ws2 32. lib.</span><span class="sxs-lookup"><span data-stu-id="a11d0-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="a11d0-110">O \# Comentário pragma indica ao vinculador que o arquivo *Ws2 \_ 32. lib* é necessário.</span><span class="sxs-lookup"><span data-stu-id="a11d0-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="a11d0-111">Comece a programar o aplicativo Winsock.</span><span class="sxs-lookup"><span data-stu-id="a11d0-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="a11d0-112">Use a API do Winsock incluindo os arquivos de cabeçalho do Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="a11d0-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="a11d0-113">O arquivo de cabeçalho *Winsock2. h* contém a maioria das funções, estruturas e definições do Winsock.</span><span class="sxs-lookup"><span data-stu-id="a11d0-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="a11d0-114">O arquivo de cabeçalho *Ws2tcpip. h* contém definições introduzidas no documento WinSock 2 Protocol-Specific anexo para TCP/IP que inclui funções e estruturas mais recentes usadas para recuperar endereços IP.</span><span class="sxs-lookup"><span data-stu-id="a11d0-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="a11d0-115">Stdio. h é usado para entrada e saída padrão, especificamente a função **printf ()** .</span><span class="sxs-lookup"><span data-stu-id="a11d0-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


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
> <span data-ttu-id="a11d0-116">O arquivo de cabeçalho *Iphlpapi. h* será necessário se um aplicativo estiver usando as APIs auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="a11d0-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="a11d0-117">Quando o arquivo de cabeçalho *Iphlpapi. h* é necessário, a \# linha de inclusão para o arquivo de cabeçalho *Winsock2. h* deve ser colocada antes da \# linha de inclusão para o arquivo de cabeçalho *Iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="a11d0-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="a11d0-118">O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos Winsock.</span><span class="sxs-lookup"><span data-stu-id="a11d0-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="a11d0-119">Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32.</span><span class="sxs-lookup"><span data-stu-id="a11d0-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="a11d0-120">Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="a11d0-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="a11d0-121">As declarações no arquivo de cabeçalho *Winsock. h* entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="a11d0-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="a11d0-122">A \_ macro de Lean \_ e Mean do Win32 impede que \_ o *Winsock. h* seja incluído pelo cabeçalho *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="a11d0-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="a11d0-123">Um exemplo ilustrando isso é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="a11d0-123">An example illustrating this is shown below.</span></span>

 


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



<span data-ttu-id="a11d0-124">Próxima etapa: [inicializando o Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="a11d0-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a11d0-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a11d0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a11d0-126">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="a11d0-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="a11d0-127">Sobre servidores e clientes</span><span class="sxs-lookup"><span data-stu-id="a11d0-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



