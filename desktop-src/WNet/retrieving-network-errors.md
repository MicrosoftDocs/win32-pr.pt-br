---
title: Recuperando erros de rede
description: As funções WNet retornam códigos de erro para compatibilidade com o Windows para Workgroups. Cada função WNet também define o valor do código de erro retornado por GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436d63b51d0f57698403d206774710450eee1c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105771596"
---
# <a name="retrieving-network-errors"></a><span data-ttu-id="adfac-104">Recuperando erros de rede</span><span class="sxs-lookup"><span data-stu-id="adfac-104">Retrieving Network Errors</span></span>

<span data-ttu-id="adfac-105">As funções WNet retornam códigos de erro para compatibilidade com o Windows para Workgroups.</span><span class="sxs-lookup"><span data-stu-id="adfac-105">The WNet functions return error codes for compatibility with Windows for Workgroups.</span></span> <span data-ttu-id="adfac-106">Cada função WNet também define o valor do código de erro retornado por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="adfac-106">Each WNet function also sets the error code value returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="adfac-107">Quando uma das funções WNet retorna \_ erro estendido de erro \_ , um aplicativo pode chamar a função [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) para recuperar informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="adfac-107">When one of the WNet functions returns ERROR\_EXTENDED\_ERROR, an application can call the [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) function to retrieve additional information about the error.</span></span> <span data-ttu-id="adfac-108">Essas informações geralmente são específicas para o provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="adfac-108">This information is usually specific to the network provider.</span></span>

<span data-ttu-id="adfac-109">O exemplo a seguir ilustra uma função de manipulação de erros definida pelo aplicativo (NetErrorHandler).</span><span class="sxs-lookup"><span data-stu-id="adfac-109">The following example illustrates an application-defined error-handling function (NetErrorHandler).</span></span> <span data-ttu-id="adfac-110">A função usa três argumentos: um identificador de janela, o código de erro retornado por uma das funções WNet e o nome da função que produziu o erro.</span><span class="sxs-lookup"><span data-stu-id="adfac-110">The function takes three arguments: a window handle, the error code returned by one of the WNet functions, and the name of the function that produced the error.</span></span> <span data-ttu-id="adfac-111">Se o código de erro for erro \_ estendido \_ , NetErrorHandler chamará **WNetGetLastError** para obter informações de erro estendidas e imprimirá as informações.</span><span class="sxs-lookup"><span data-stu-id="adfac-111">If the error code is ERROR\_EXTENDED\_ERROR, NetErrorHandler calls **WNetGetLastError** to get extended error information and prints the information.</span></span> <span data-ttu-id="adfac-112">O exemplo chama a função [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) para processar mensagens.</span><span class="sxs-lookup"><span data-stu-id="adfac-112">The sample calls the [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function to process messages.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 