---
title: Enumerando recursos de rede
description: O exemplo a seguir ilustra uma função definida pelo aplicativo (EnumerateFunc) que enumera todos os recursos em uma rede.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633a8b03dd538853a0b339ee727c18fb05b2231b7690d89dea0a83264f7faf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053324"
---
# <a name="enumerating-network-resources"></a>Enumerando recursos de rede

O exemplo a seguir ilustra uma função definida pelo aplicativo (EnumerateFunc) que enumera todos os recursos em uma rede. O exemplo especifica **NULL** para o ponteiro para a estrutura do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) porque, quando [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) recebe um ponteiro **NULL** , ele recupera um identificador para a raiz da rede.

Para iniciar a enumeração de um recurso de contêiner de rede, seu aplicativo deve executar as seguintes etapas:

1.  Passe o endereço de uma estrutura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que representa o recurso para a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .
2.  Aloque um buffer grande o suficiente para manter a matriz de estruturas do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) retorna, além das cadeias de caracteres para as quais seus membros apontam.
3.  Passe o identificador de recurso retornado por [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) .
4.  Feche o identificador de recursos quando ele não for mais necessário chamando a função [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) .

Você pode continuar enumerando um recurso de contêiner descrito na matriz de estruturas de [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperadas por [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea). Se o membro **dwUsage** da estrutura **NETRESOURCE** for igual ao contêiner RESOURCEUSAGE \_ , passe o endereço da estrutura para a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para abrir o contêiner e continuar a enumeração. Se **dwUsage** for igual a RESOURCEUSAGE \_ conectável, o aplicativo poderá passar o endereço da estrutura para a [**função WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou a função [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) para se conectar ao recurso.

Primeiro, o exemplo chama a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para iniciar a enumeração. O exemplo chama a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) para alocar o buffer necessário e, em seguida, chama a função [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para definir o conteúdo do buffer como zero. Em seguida, o exemplo chama a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) para continuar a enumeração. Sempre que o membro **dwUsage** de uma estrutura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperada por **WNETENUMRESOURCE** for igual ao \_ contêiner RESOURCEUSAGE, a função EnumerateFunc chamará recursivamente e usará um ponteiro para essa estrutura em sua chamada para **WnetOpenEnum**. Por fim, o exemplo chama a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para liberar a memória alocada e o [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) para encerrar a enumeração.


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).

 

 