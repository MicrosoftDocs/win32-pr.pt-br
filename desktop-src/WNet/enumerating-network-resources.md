---
title: Enumerando recursos de rede
description: O exemplo a seguir ilustra uma função definida pelo aplicativo (EnumerateFunc) que enumera todos os recursos em uma rede.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366356"
---
# <a name="enumerating-network-resources"></a><span data-ttu-id="98f57-103">Enumerando recursos de rede</span><span class="sxs-lookup"><span data-stu-id="98f57-103">Enumerating Network Resources</span></span>

<span data-ttu-id="98f57-104">O exemplo a seguir ilustra uma função definida pelo aplicativo (EnumerateFunc) que enumera todos os recursos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="98f57-104">The following example illustrates an application-defined function (EnumerateFunc) that enumerates all the resources on a network.</span></span> <span data-ttu-id="98f57-105">O exemplo especifica **NULL** para o ponteiro para a estrutura do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) porque, quando [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) recebe um ponteiro **NULL** , ele recupera um identificador para a raiz da rede.</span><span class="sxs-lookup"><span data-stu-id="98f57-105">The sample specifies **NULL** for the pointer to the [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure because when [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) receives a **NULL** pointer, it retrieves a handle to the root of the network.</span></span>

<span data-ttu-id="98f57-106">Para iniciar a enumeração de um recurso de contêiner de rede, seu aplicativo deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="98f57-106">To begin the enumeration of a network container resource, your application should perform the following steps:</span></span>

1.  <span data-ttu-id="98f57-107">Passe o endereço de uma estrutura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que representa o recurso para a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .</span><span class="sxs-lookup"><span data-stu-id="98f57-107">Pass the address of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure that represents the resource to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function.</span></span>
2.  <span data-ttu-id="98f57-108">Aloque um buffer grande o suficiente para manter a matriz de estruturas do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) que a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) retorna, além das cadeias de caracteres para as quais seus membros apontam.</span><span class="sxs-lookup"><span data-stu-id="98f57-108">Allocate a buffer large enough to hold the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures that the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function returns, plus the strings to which their members point.</span></span>
3.  <span data-ttu-id="98f57-109">Passe o identificador de recurso retornado por [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) .</span><span class="sxs-lookup"><span data-stu-id="98f57-109">Pass the resource handle returned by [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) to the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function.</span></span>
4.  <span data-ttu-id="98f57-110">Feche o identificador de recursos quando ele não for mais necessário chamando a função [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) .</span><span class="sxs-lookup"><span data-stu-id="98f57-110">Close the resource handle when it is no longer needed by calling the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) function.</span></span>

<span data-ttu-id="98f57-111">Você pode continuar enumerando um recurso de contêiner descrito na matriz de estruturas de [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperadas por [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span><span class="sxs-lookup"><span data-stu-id="98f57-111">You can continue enumerating a container resource described in the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures retrieved by [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span></span> <span data-ttu-id="98f57-112">Se o membro **dwUsage** da estrutura **NETRESOURCE** for igual ao contêiner RESOURCEUSAGE \_ , passe o endereço da estrutura para a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para abrir o contêiner e continuar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="98f57-112">If the **dwUsage** member of the **NETRESOURCE** structure is equal to RESOURCEUSAGE\_CONTAINER, pass the address of the structure to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to open the container and continue the enumeration.</span></span> <span data-ttu-id="98f57-113">Se **dwUsage** for igual a RESOURCEUSAGE \_ conectável, o aplicativo poderá passar o endereço da estrutura para a [**função WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou a função [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) para se conectar ao recurso.</span><span class="sxs-lookup"><span data-stu-id="98f57-113">If **dwUsage** is equal to RESOURCEUSAGE\_CONNECTABLE, the application can pass the structure's address to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function to connect to the resource.</span></span>

<span data-ttu-id="98f57-114">Primeiro, o exemplo chama a função [**WnetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) para iniciar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="98f57-114">First the sample calls the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to begin the enumeration.</span></span> <span data-ttu-id="98f57-115">O exemplo chama a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) para alocar o buffer necessário e, em seguida, chama a função [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) para definir o conteúdo do buffer como zero.</span><span class="sxs-lookup"><span data-stu-id="98f57-115">The sample calls the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function to allocate the required buffer, and then calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to set the buffer contents to zero.</span></span> <span data-ttu-id="98f57-116">Em seguida, o exemplo chama a função [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) para continuar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="98f57-116">Then the sample calls the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function to continue the enumeration.</span></span> <span data-ttu-id="98f57-117">Sempre que o membro **dwUsage** de uma estrutura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperada por **WNETENUMRESOURCE** for igual ao \_ contêiner RESOURCEUSAGE, a função EnumerateFunc chamará recursivamente e usará um ponteiro para essa estrutura em sua chamada para **WnetOpenEnum**.</span><span class="sxs-lookup"><span data-stu-id="98f57-117">Whenever the **dwUsage** member of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure retrieved by **WNetEnumResource** is equal to RESOURCEUSAGE\_CONTAINER, the EnumerateFunc function calls itself recursively and uses a pointer to that structure in its call to **WNetOpenEnum**.</span></span> <span data-ttu-id="98f57-118">Por fim, o exemplo chama a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) para liberar a memória alocada e o [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) para encerrar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="98f57-118">Finally, the sample calls the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function to free the allocated memory, and the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) to end the enumeration.</span></span>


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



<span data-ttu-id="98f57-119">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="98f57-119">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 