---
title: Recuperando o nome de usuário
description: Para recuperar o nome do usuário associado a um dispositivo local conectado a um recurso de rede ou com o nome de uma rede, um aplicativo pode chamar a função WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162352"
---
# <a name="retrieving-the-user-name"></a>Recuperando o nome de usuário

Para recuperar o nome do usuário associado a um dispositivo local conectado a um recurso de rede ou com o nome de uma rede, um aplicativo pode chamar a função [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

O exemplo a seguir usa o nome do dispositivo para recuperar o nome do usuário. O exemplo chama um manipulador de erro definido pelo aplicativo para processar erros e a função [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para impressão.


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).

 

 