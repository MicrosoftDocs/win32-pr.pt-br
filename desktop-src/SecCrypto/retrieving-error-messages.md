---
description: Quando uma chamada de método produz um erro, muitas funções retornam um código de erro.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Recuperando mensagens de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828336"
---
# <a name="retrieving-error-messages"></a>Recuperando mensagens de erro

Quando uma chamada de método produz um erro, muitas funções retornam um código de erro. Para a maioria das interfaces de serviços de certificados e elementos de API que retornam um código de erro, o texto da mensagem de erro pode ser recuperado chamando [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) com um identificador de módulo **nulo** . Se **FormatMessage** não for bem sucedido, o código de erro provavelmente resultou de um erro relacionado a um elemento ou banco de dados da API de backup; chamar **FormatMessage** com um identificador de módulo correspondente à biblioteca de Ntdsbmsg.dll deve recuperar o texto da mensagem de erro. O exemplo a seguir mostra como recuperar o texto da mensagem de erro em um aplicativo de serviços de certificados.


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
