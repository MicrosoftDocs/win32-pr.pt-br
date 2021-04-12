---
title: Atribuindo uma unidade a um compartilhamento
description: O exemplo a seguir demonstra como conectar uma letra da unidade a um compartilhamento de servidor remoto com uma chamada para a função WNetAddConnection2. O exemplo informa ao usuário se a chamada foi ou não bem-sucedida.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366357"
---
# <a name="assigning-a-drive-to-a-share"></a>Atribuindo uma unidade a um compartilhamento

O exemplo a seguir demonstra como conectar uma letra da unidade a um compartilhamento de servidor remoto com uma chamada para a função [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) . O exemplo informa ao usuário se a chamada foi ou não bem-sucedida.

Para testar o exemplo de código a seguir, execute as seguintes etapas:

1.  Altere as seguintes linhas para cadeias de caracteres válidas:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Adicione o arquivo a um aplicativo de console chamado AddConn2.
3.  Vincule a biblioteca MPR. LIB para a lista de bibliotecas do compilador.
4.  Compile e execute o programa AddConn2.EXE.


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 