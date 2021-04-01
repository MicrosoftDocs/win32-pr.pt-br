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
# <a name="retrieving-information-about-a-network-resource"></a>Recuperando informações sobre um recurso de rede

Para identificar o provedor de rede que possui um recurso, um aplicativo pode chamar a função [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , conforme ilustrado no exemplo de código a seguir.

O exemplo a seguir é uma função (CheckServer) que usa um nome de servidor como parâmetro e retorna informações sobre esse servidor. Primeiro, a função chama a função [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para inicializar o conteúdo de um bloco de memória para zero. Em seguida, o exemplo chama a função [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , especificando um buffer grande o suficiente para manter apenas uma estrutura de [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . A rotina inclui o processamento de erro para lidar com o caso quando um buffer desse tamanho é insuficiente para manter as cadeias de caracteres de comprimento variável para as quais os membros do ponto da estrutura do **NETRESOURCE** . Se esse erro ocorrer, o exemplo aloca memória suficiente e chama **WNetGetResourceInformation** novamente. Por fim, a amostra libera a memória alocada.

Observe que o exemplo pressupõe que o parâmetro *pszServer* aponta para um nome de servidor que um dos provedores de rede no computador local reconhece.


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



 

 