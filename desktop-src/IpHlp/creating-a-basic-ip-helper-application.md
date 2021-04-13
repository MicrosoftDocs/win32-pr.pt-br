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
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="0928b-103">Criando um aplicativo auxiliar de IP básico</span><span class="sxs-lookup"><span data-stu-id="0928b-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="0928b-104">**Para criar um aplicativo auxiliar de IP básico**</span><span class="sxs-lookup"><span data-stu-id="0928b-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="0928b-105">Crie um novo projeto vazio.</span><span class="sxs-lookup"><span data-stu-id="0928b-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="0928b-106">Adicione um arquivo de origem C++ vazio ao projeto.</span><span class="sxs-lookup"><span data-stu-id="0928b-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="0928b-107">Verifique se o ambiente de compilação refere-se aos diretórios include, lib e src do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="0928b-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="0928b-108">Verifique se o ambiente de compilação é vinculado ao arquivo de biblioteca auxiliar de IP Iphlpapi. lib e ao arquivo de biblioteca do Winsock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="0928b-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="0928b-109">Algumas funções básicas do Winsock são usadas para retornar valores de endereço IP e outras informações.</span><span class="sxs-lookup"><span data-stu-id="0928b-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="0928b-110">Comece a programar o aplicativo auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="0928b-111">Use a API do IP Helper, incluindo o arquivo de cabeçalho do auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-111">Use the IP Helper API by including the IP Helper header file.</span></span>

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
    > <span data-ttu-id="0928b-112">O arquivo de cabeçalho *Iphlpapi. h* é necessário para aplicativos que usam as funções auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="0928b-113">O arquivo de cabeçalho *Iphlpapi. h* inclui automaticamente outros arquivos de cabeçalhos com estruturas e enumerações usadas pelas funções auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="0928b-114">As novas funções auxiliares de IP introduzidas no Windows Vista e versões posteriores são definidas no arquivo de cabeçalho *Netioapi. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="0928b-115">O arquivo de cabeçalho *Netioapi. h* nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="0928b-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="0928b-116">Muitas das estruturas e enumerações usadas pelas funções auxiliares de IP são definidas nos arquivos de cabeçalho *Iprtrmib. h*, *ipexport. h* e *Iptypes. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="0928b-117">Esses arquivos de cabeçalho são incluídos automaticamente no arquivo de cabeçalho *Iphlpapi. h* e nunca devem ser usados diretamente.</span><span class="sxs-lookup"><span data-stu-id="0928b-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="0928b-118">No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada.</span><span class="sxs-lookup"><span data-stu-id="0928b-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="0928b-119">Algumas das estruturas agora são definidas nos arquivos de cabeçalho *Ipmib. h*, *Tcpmib. h* e *Udpmib. h* , não no arquivo de cabeçalho *Iprtrmib. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="0928b-120">O arquivo de cabeçalho *Ipmib. h* inclui automaticamente o arquivo de cabeçalho *Ifmib. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="0928b-121">Observe que esses arquivos de cabeçalho são incluídos automaticamente no *Iprtrmib. h*, que é incluído automaticamente no arquivo de cabeçalho *Iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="0928b-122">O arquivo de cabeçalho *Winsock2. h* para o Windows sockets 2,0 é exigido pela maioria dos aplicativos que usam as APIs auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="0928b-123">Quando o arquivo de cabeçalho *Winsock2. h* é necessário, a \# linha de inclusão desse arquivo deve ser colocada antes da \# linha de inclusão para o arquivo de cabeçalho *Iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="0928b-124">O arquivo de cabeçalho *Winsock2. h* inclui internamente os elementos principais do arquivo de cabeçalho *Windows. h* , de modo que geralmente não há uma \# linha include para o arquivo de cabeçalho *Windows. h* em aplicativos auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="0928b-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="0928b-125">Se uma \# linha de inclusão for necessária para o arquivo de cabeçalho *Windows. h* , isso deverá ser precedido com a \# definição da \_ \_ \_ macro Mean e média do Win32.</span><span class="sxs-lookup"><span data-stu-id="0928b-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="0928b-126">Por motivos históricos, o cabeçalho *Windows. h* usa como padrão o arquivo de cabeçalho *Winsock. h* para o Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="0928b-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="0928b-127">As declarações no arquivo de cabeçalho *Winsock. h* para o Windows sockets 1,1 entrarão em conflito com as declarações no arquivo de cabeçalho *Winsock2. h* exigido pelo Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="0928b-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="0928b-128">A \_ macro de Lean \_ e Mean do Win32 impede que \_ o arquivo de cabeçalho *Winsock. h* seja incluído pelo arquivo de cabeçalho do *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="0928b-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="0928b-129">Um exemplo ilustrando isso é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="0928b-129">An example illustrating this is shown below.</span></span>

     

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
    > <span data-ttu-id="0928b-130">Esse aplicativo auxiliar de IP básico usa apenas algumas estruturas de dados de endereço IP e o endereço IP para funções de conversão de cadeia de caracteres do Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="0928b-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="0928b-131">Essas funções do Windows Sockets podem ser usadas sem chamar o [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar recursos do Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando terminar de usar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="0928b-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="0928b-132">Em aplicativos auxiliares de IP que usam outras funções do Winsock que não sejam esse endereço IP para funções de cadeia de caracteres, a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve ser chamada para inicializar recursos do Windows Sockets antes de chamar qualquer função do Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) deve ser chamado quando o aplicativo é feito usando recursos do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="0928b-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="0928b-133">O arquivo de cabeçalho *stdio. h* é necessário para o uso de várias funções padrão do C neste aplicativo auxiliar de IP básico.</span><span class="sxs-lookup"><span data-stu-id="0928b-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="0928b-134">Próxima etapa: [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="0928b-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
