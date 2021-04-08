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
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="31ce6-105">Como bloquear a estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="31ce6-105">How to Lock the Workstation</span></span>

<span data-ttu-id="31ce6-106">O exemplo a seguir bloqueia a estação de trabalho usando a função [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) .</span><span class="sxs-lookup"><span data-stu-id="31ce6-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="31ce6-107">O sistema exibe a caixa de diálogo **Bloquear estação de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="31ce6-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="31ce6-108">O texto da caixa de diálogo diz que a estação de trabalho está em uso e foi bloqueada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="31ce6-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


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



<span data-ttu-id="31ce6-109">Para determinar se a estação de trabalho está bloqueada, teste se a janela está visível.</span><span class="sxs-lookup"><span data-stu-id="31ce6-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="31ce6-110">A estação de trabalho pode ser desbloqueada pelo usuário ou por um administrador.</span><span class="sxs-lookup"><span data-stu-id="31ce6-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="31ce6-111">Para desbloquear o sistema, pressione Ctrl + Alt + Del e faça logon.</span><span class="sxs-lookup"><span data-stu-id="31ce6-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="31ce6-112">Para receber uma notificação quando o usuário fizer logon, use a função [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) para se registrar para receber mensagens de [**alteração do WM \_ WTSSESSION \_**](../termserv/wm-wtssession-change.md) .</span><span class="sxs-lookup"><span data-stu-id="31ce6-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="31ce6-113">Quando essa mensagem for recebida, verifique se o parâmetro *wParam* é igual ao \_ bloqueio de sessão WTS \_ .</span><span class="sxs-lookup"><span data-stu-id="31ce6-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
