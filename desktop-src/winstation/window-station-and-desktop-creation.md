---
title: Estação de janela e criação de área de trabalho
description: O sistema cria automaticamente a estação de janela interativa.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52a3cc85a3194bea6c8eaea00a7ce794901426e794c962e1b23713561f8fc744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030512"
---
# <a name="window-station-and-desktop-creation"></a>Estação de janela e criação de área de trabalho

O sistema cria automaticamente a estação de janela interativa. Quando um usuário interativo faz logon, o sistema associa a estação de janela interativa à sessão de logon do usuário. O sistema também cria a área de trabalho de entrada padrão para a estação de janela interativa (Winsta0 \\ padrão). Os processos iniciados pelo usuário conectado são associados à \\ área de trabalho padrão do Winsta0.

Um processo pode usar a função [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) para criar uma nova estação de janela e a função **createdesktop** ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) para criar uma nova área de trabalho. O número de áreas de trabalho que podem ser criadas é limitado pelo tamanho do heap da área de trabalho do sistema. Para obter mais informações, consulte [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Quando um processo não interativo, como um aplicativo de serviço, tenta se conectar a uma estação de janela e não existe nenhuma estação de janela para a sessão de logon do processo, o sistema tenta criar uma estação de janela e uma área de trabalho para a sessão. O nome da estação de janela criada é baseado no identificador de sessão de logon, e a área de trabalho é denominada padrão, conforme descrito aqui:

-   Se um serviço estiver em execução no contexto de segurança da conta LocalSystem, mas não incluir o \_ atributo processo interativo do serviço \_ , ele usará a seguinte estação de janela e área de trabalho: Service-0x0-3e7 $ \\ Default. Esta estação de janela não é interativa, portanto o serviço não pode exibir uma interface do usuário. Além disso, os processos criados pelo serviço não podem exibir uma interface do usuário.
-   Se o serviço estiver em execução no contexto de segurança de uma conta de usuário, o nome da estação de janela será baseado no serviço SID do usuário-0x *Z1* - *Z2*$, em que *Z1* é a parte superior do Sid de logon e *Z2* é a parte inferior do Sid de logon. Como um SID é exclusivo para a sessão de logon, dois serviços em execução no mesmo contexto de segurança recebem estações de janela exclusivas. Essas estações de janela não são interativas.

A DACL (lista de controle de acesso discricionário) para a estação de janela e área de trabalho inclui os seguintes direitos de acesso para a conta de usuário do serviço:

Estação de janela:

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEdesktop  
WINSTA \_ EXITWINDOWS  
WINSTA \_ ReadAttributes  
\_direitos padrão \_ necessários  
</dl>

Área de trabalho:

<dl> CreateMenu da área de trabalho \_  
CREATEWINDOW da área de trabalho \_  
enumerar área de trabalho \_  
\_HOOKCONTROL desktop  
\_READOBJECTS desktop  
\_WRITEOBJECTS desktop  
\_direitos padrão \_ necessários  
</dl>

 

 