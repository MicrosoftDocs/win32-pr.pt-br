---
title: Pesquisando texto para números de código de erro
description: Às vezes, é necessário exibir o texto de erro associado aos códigos de erro retornados das funções relacionadas à rede. Talvez seja necessário executar essa tarefa com as funções de gerenciamento de rede fornecidas pelo sistema.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770470"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Pesquisando texto para números de código de erro

Às vezes, é necessário exibir o texto de erro associado aos códigos de erro retornados das funções relacionadas à rede. Talvez seja necessário executar essa tarefa com as funções de gerenciamento de rede fornecidas pelo sistema.

O texto de erro para essas mensagens é encontrado no arquivo de tabela de mensagens chamado Netmsg.dll, que é encontrado em% SystemRoot% \\ System32. Esse arquivo contém mensagens de erro no intervalo NERR \_ base (2100) a Max \_ NERR (NERR \_ base + 899). Esses códigos de erro são definidos no arquivo de cabeçalho do SDK lmerr. h.

As funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) podem carregar Netmsg.dll. A função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) mapeia um código de erro para o texto da mensagem, dado um identificador de módulo ao arquivo Netmsg.dll.

O exemplo a seguir ilustra como exibir o texto de erro associado às funções de gerenciamento de rede, além de exibir o texto de erro associado a códigos de erro relacionados ao sistema. Se o número de erro fornecido estiver em um intervalo específico, o módulo netmsg.dll mensagem será carregado e usado para pesquisar o número de erro especificado com a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



Depois de compilar esse programa, você pode inserir o número de código de erro como um argumento e o programa exibirá o texto. Por exemplo:

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 