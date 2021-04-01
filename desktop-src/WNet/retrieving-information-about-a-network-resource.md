---
title: Recuperando informações sobre um recurso de rede
description: Para identificar o provedor de rede que possui um recurso, um aplicativo pode chamar a função WNetGetResourceInformation, conforme ilustrado no exemplo de código a seguir.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084707"
---
# <a name="retrieving-information-about-a-network-resource"></a><span data-ttu-id="a22bc-103">Recuperando informações sobre um recurso de rede</span><span class="sxs-lookup"><span data-stu-id="a22bc-103">Retrieving Information About a Network Resource</span></span>

<span data-ttu-id="a22bc-104">Para identificar o provedor de rede que possui um recurso, um aplicativo pode chamar a função [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , conforme ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a22bc-104">To identify the network provider that owns a resource, an application can call the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, as illustrated in the following code sample.</span></span>

<span data-ttu-id="a22bc-105">O exemplo a seguir é uma função (CheckServer) que usa um nome de servidor como parâmetro e retorna informações sobre esse servidor.</span><span class="sxs-lookup"><span data-stu-id="a22bc-105">The following sample is a function (CheckServer) that takes a server name as a parameter and returns information about that server.</span></span> <span data-ttu-id="a22bc-106">Primeiro, a função chama a função [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para inicializar o conteúdo de um bloco de memória para zero.</span><span class="sxs-lookup"><span data-stu-id="a22bc-106">First the function calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to initialize the contents of a block of memory to zero.</span></span> <span data-ttu-id="a22bc-107">Em seguida, o exemplo chama a função [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , especificando um buffer grande o suficiente para manter apenas uma estrutura de [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="a22bc-107">Then the sample calls the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, specifying a buffer large enough to hold only a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure.</span></span> <span data-ttu-id="a22bc-108">A rotina inclui o processamento de erro para lidar com o caso quando um buffer desse tamanho é insuficiente para manter as cadeias de caracteres de comprimento variável para as quais os membros do ponto da estrutura do **NETRESOURCE** .</span><span class="sxs-lookup"><span data-stu-id="a22bc-108">The routine includes error processing to handle the case when a buffer of this size is insufficient to hold the variable-length strings to which members of the **NETRESOURCE** structure point.</span></span> <span data-ttu-id="a22bc-109">Se esse erro ocorrer, o exemplo aloca memória suficiente e chama **WNetGetResourceInformation** novamente.</span><span class="sxs-lookup"><span data-stu-id="a22bc-109">If this error occurs, the sample allocates sufficient memory and calls **WNetGetResourceInformation** again.</span></span> <span data-ttu-id="a22bc-110">Por fim, a amostra libera a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="a22bc-110">Finally, the sample frees the allocated memory.</span></span>

<span data-ttu-id="a22bc-111">Observe que o exemplo pressupõe que o parâmetro *pszServer* aponta para um nome de servidor que um dos provedores de rede no computador local reconhece.</span><span class="sxs-lookup"><span data-stu-id="a22bc-111">Note that the sample assumes that the *pszServer* parameter points to a server name that one of the network providers on the local computer recognizes.</span></span>


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 