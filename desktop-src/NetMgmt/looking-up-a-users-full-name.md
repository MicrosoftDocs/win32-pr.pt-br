---
title: Procurando o nome completo de um usuário
description: Os computadores podem ser organizados em um domínio, que é uma coleção de rede de computadores. O administrador de domínio mantém informações centralizadas de conta de usuário e grupo.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdff00483b38ef12355af4dcda4a48d60bf849a8fd5d6829640ae8907e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012514"
---
# <a name="looking-up-a-users-full-name"></a>Procurando o nome completo de um usuário

Os computadores podem ser organizados em *um domínio*, que é uma coleção de rede de computadores. O administrador de domínio mantém informações centralizadas de conta de usuário e grupo.

Para encontrar o nome completo de um usuário, considerando o nome de usuário e o nome de domínio:

-   Converta o nome de usuário e o nome de domínio em Unicode, se eles ainda não são cadeias de caracteres Unicode.
-   Procure o nome do computador do controlador de domínio (DC) chamando [**NetGetDCName.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)
-   Procure o nome de usuário no computador DC chamando [**NetUserGetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)
-   Converta o nome de usuário completo em ANSI, a menos que o programa esteja esperando trabalhar com cadeias de caracteres Unicode.

O código de exemplo a seguir é uma função (GetFullName) que recebe um nome de usuário e um nome de domínio nos dois primeiros argumentos e retorna o nome completo do usuário no terceiro argumento.


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




