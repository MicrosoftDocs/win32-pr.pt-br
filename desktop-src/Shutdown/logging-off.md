---
description: A função ExitWindows faz logoff do usuário atual. Você também pode chamar a função ExitWindowsEx com o \_ sinalizador de logoff EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Fazendo logoff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837496"
---
# <a name="logging-off"></a>Fazendo logoff

A função [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) faz logoff do usuário atual. Você também pode chamar a função [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) com o \_ sinalizador de logoff EXW.

Por padrão, quando um aplicativo usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para fazer logoff, o sistema envia a mensagem do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) para cada janela. Os aplicativos concordam em terminar retornando **true** quando recebem esta mensagem. Se qualquer aplicativo retornar **false** ao processar essa mensagem, a operação de logoff será cancelada. Se seu aplicativo manipula a mensagem do **WM \_ QUERYENDSESSION** , você pode permitir que o usuário cancele a operação de logoff, mesmo que outro aplicativo ou o sistema tenha originado a solicitação de sessão de término. Para obter um exemplo, consulte [como fazer logoff do usuário atual](how-to-log-off-the-current-user.md).

Quando um aplicativo retorna **true** para o [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), ele recebe a mensagem de [**\_ EndSession do WM**](wm-endsession.md) e é encerrado, independentemente de como os outros aplicativos respondem à mensagem do **WM \_ QUERYENDSESSION** .

Para forçar a finalização de todos os aplicativos, use o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)e especifique o \_ sinalizador de força EXW. Isso impede que o sistema envie mensagens do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .

O sistema também envia o \_ sinal de controle de evento CTRL logoff \_ para cada processo durante uma operação de logoff. Um aplicativo de console pode registrar um [**HandlerRoutine**](/windows/console/handlerroutine) para processar essas mensagens.

Se o processo que chamou o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) estiver em execução na sessão de logon do usuário interativo, todos os processos na sessão de logon serão encerrados. Se o processo que chama o **ExitWindowsEx** estiver em alguma outra sessão de logon, somente as notificações serão feitas; nenhum processo foi encerrado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como fazer logoff do usuário atual](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
