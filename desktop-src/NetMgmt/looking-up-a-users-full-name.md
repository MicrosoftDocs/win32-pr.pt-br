---
title: Pesquisando o nome completo de um usuário
description: Os computadores podem ser organizados em um domínio, que é um conjunto de redes de computadores. O administrador de domínio mantém informações de conta de usuário e grupo centralizadas.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764647"
---
# <a name="looking-up-a-users-full-name"></a>Pesquisando o nome completo de um usuário

Os computadores podem ser organizados em um *domínio*, que é um conjunto de redes de computadores. O administrador de domínio mantém informações de conta de usuário e grupo centralizadas.

Para localizar o nome completo de um usuário, dado o nome de usuário e o nome de domínio:

-   Converta o nome de usuário e o nome de domínio para Unicode, se eles ainda não forem cadeias de caracteres Unicode.
-   Pesquise o nome do computador do controlador de domínio (DC) chamando [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Procure o nome de usuário no computador DC chamando [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Converta o nome de usuário completo para ANSI, a menos que o programa esteja esperando trabalhar com cadeias de caracteres Unicode.

O código de exemplo a seguir é uma função (getcompletaname) que usa um nome de usuário e um nome de domínio nos dois primeiros argumentos e retorna o nome completo do usuário no terceiro argumento.


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



 

 




