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
# <a name="looking-up-a-users-full-name"></a><span data-ttu-id="c2ceb-104">Pesquisando o nome completo de um usuário</span><span class="sxs-lookup"><span data-stu-id="c2ceb-104">Looking Up a User's Full Name</span></span>

<span data-ttu-id="c2ceb-105">Os computadores podem ser organizados em um *domínio*, que é um conjunto de redes de computadores.</span><span class="sxs-lookup"><span data-stu-id="c2ceb-105">Computers can be organized into a *domain*, which is a collection of computers network.</span></span> <span data-ttu-id="c2ceb-106">O administrador de domínio mantém informações de conta de usuário e grupo centralizadas.</span><span class="sxs-lookup"><span data-stu-id="c2ceb-106">The domain administrator maintains centralized user and group account information.</span></span>

<span data-ttu-id="c2ceb-107">Para localizar o nome completo de um usuário, dado o nome de usuário e o nome de domínio:</span><span class="sxs-lookup"><span data-stu-id="c2ceb-107">To find the full name of a user, given the user name and domain name:</span></span>

-   <span data-ttu-id="c2ceb-108">Converta o nome de usuário e o nome de domínio para Unicode, se eles ainda não forem cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2ceb-108">Convert the user name and domain name to Unicode, if they are not already Unicode strings.</span></span>
-   <span data-ttu-id="c2ceb-109">Pesquise o nome do computador do controlador de domínio (DC) chamando [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span><span class="sxs-lookup"><span data-stu-id="c2ceb-109">Look up the computer name of the domain controller (DC) by calling [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span></span>
-   <span data-ttu-id="c2ceb-110">Procure o nome de usuário no computador DC chamando [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span><span class="sxs-lookup"><span data-stu-id="c2ceb-110">Look up the user name on the DC computer by calling [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span></span>
-   <span data-ttu-id="c2ceb-111">Converta o nome de usuário completo para ANSI, a menos que o programa esteja esperando trabalhar com cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2ceb-111">Convert the full user name to ANSI, unless the program is expecting to work with Unicode strings.</span></span>

<span data-ttu-id="c2ceb-112">O código de exemplo a seguir é uma função (getcompletaname) que usa um nome de usuário e um nome de domínio nos dois primeiros argumentos e retorna o nome completo do usuário no terceiro argumento.</span><span class="sxs-lookup"><span data-stu-id="c2ceb-112">The following sample code is a function (GetFullName) that takes a user name and a domain name in the first two arguments and returns the user's full name in the third argument.</span></span>


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



 

 




