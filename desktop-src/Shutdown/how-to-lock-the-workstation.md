---
description: O exemplo a seguir bloqueia a estação de trabalho usando a função LockWorkStation. O sistema exibe a caixa de diálogo Bloquear estação de trabalho. O texto da caixa de diálogo diz que a estação de trabalho está em uso e foi bloqueada pelo usuário.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Como bloquear a estação de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828686"
---
# <a name="how-to-lock-the-workstation"></a>Como bloquear a estação de trabalho

O exemplo a seguir bloqueia a estação de trabalho usando a função [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) . O sistema exibe a caixa de diálogo **Bloquear estação de trabalho** . O texto da caixa de diálogo diz que a estação de trabalho está em uso e foi bloqueada pelo usuário.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



Para determinar se a estação de trabalho está bloqueada, teste se a janela está visível.

A estação de trabalho pode ser desbloqueada pelo usuário ou por um administrador. Para desbloquear o sistema, pressione Ctrl + Alt + Del e faça logon. Para receber uma notificação quando o usuário fizer logon, use a função [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) para se registrar para receber mensagens de [**alteração do WM \_ WTSSESSION \_**](../termserv/wm-wtssession-change.md) . Quando essa mensagem for recebida, verifique se o parâmetro *wParam* é igual ao \_ bloqueio de sessão WTS \_ .

 

 
