---
description: Normalmente, os serviços são aplicativos de console projetados para execução autônoma sem uma GUI (interface gráfica do usuário).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Serviços interativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dda3018b4b37e8c5ee56d67cd1db2c56da9b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829635"
---
# <a name="interactive-services"></a>Serviços interativos

Normalmente, os serviços são aplicativos de console projetados para execução autônoma sem uma GUI (interface gráfica do usuário). No entanto, alguns serviços podem exigir interação ocasional com um usuário. Esta página discute as melhores maneiras de interagir com o usuário a partir de um serviço.

> [!IMPORTANT]
> Os serviços não podem interagir diretamente com um usuário a partir do Windows Vista. Portanto, as técnicas mencionadas na seção intitulada usando um serviço interativo não devem ser usadas no novo código.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interagindo indiretamente com um usuário de um serviço

Você pode usar as seguintes técnicas para interagir com o usuário de um serviço em todas as versões com suporte do Windows:

-   Exiba uma caixa de diálogo na sessão do usuário usando a função [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) .
-   Crie um aplicativo de GUI oculto separado e use a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para executar o aplicativo no contexto do usuário interativo. Projete o aplicativo de GUI para se comunicar com o serviço por meio de algum método de comunicação entre processos (IPC), por exemplo, pipes nomeados. O serviço se comunica com o aplicativo de GUI para informar quando exibir a GUI. O aplicativo comunica os resultados da interação do usuário de volta para o serviço para que o serviço possa executar a ação apropriada. Observe que o IPC pode expor suas interfaces de serviço pela rede, a menos que você use uma ACL (lista de controle de acesso) apropriada.

    Se esse serviço for executado em um sistema multiusuário, adicione o aplicativo à chave a seguir para que ele seja executado em cada sessão: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Execute**. Se o aplicativo usar pipes nomeados para IPC, o servidor poderá distinguir entre vários processos de usuário, fornecendo a cada pipe um nome exclusivo com base na ID da sessão.

A técnica a seguir também está disponível para o Windows Server 2003 e o Windows XP:

-   Exiba uma caixa de mensagem chamando a função [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) com **a \_ \_ notificação de serviço MB**. Isso é recomendado para exibir mensagens de status simples. Não chame **MessageBox** durante a inicialização do serviço ou da rotina [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) , a menos que você chame-o de um thread separado, para que você retorne ao SCM em tempo hábil.

## <a name="using-an-interactive-service"></a>Usando um serviço interativo

Por padrão, os serviços usam uma [estação de janela](/windows/desktop/winstation/window-stations) não interativa e não podem interagir com o usuário. No entanto, um *serviço interativo* pode exibir uma interface do usuário e receber a entrada do usuário.

> [!Caution]  
> Os serviços em execução em um contexto de segurança elevado, como a conta LocalSystem, não devem criar uma janela na área de trabalho interativa porque qualquer outro aplicativo em execução na área de trabalho interativa pode interagir com essa janela. Isso expõe o serviço a qualquer aplicativo executado por um usuário conectado. Além disso, os serviços que estão em execução como LocalSystem não devem acessar a área de trabalho interativa chamando a função [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) ou [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) .

 

Para criar um serviço interativo, faça o seguinte ao chamar a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) :

1.  Especifique NULL para o parâmetro *lpServiceStartName* executar o serviço no contexto da [conta LocalSystem](localsystem-account.md).
2.  Especifique o sinalizador de **\_ \_ processo interativo do serviço** .

Para determinar se um serviço está sendo executado como um serviço interativo, chame a função [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) para recuperar um identificador para a estação de janela e a função [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) para testar se a estação de janela tem o atributo **wsf \_ visível** .

No entanto, observe que a seguinte chave do registro contém um valor, **Nointeractiveservices**, que controla o efeito do \_ processo interativo do serviço \_ :

**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ Windows**

O valor de **Nointeractiveservices** usa como padrão 1, o que significa que nenhum serviço tem permissão para ser executado interativamente, independentemente de ele ter um **\_ \_ processo de serviço interativo**. Quando **Nointeractiveservices** é definido como 0, os serviços com **\_ \_ processo interativo de serviço** têm permissão para serem executados interativamente.

**Windows 7, Windows server 2008 R2, Windows XP e Windows server 2003:** O valor de **Nointeractiveservices** usa como padrão 0, o que significa que os serviços com **\_ \_ processo interativo de serviço** têm permissão para serem executados interativamente. Quando **Nointeractiveservices** é definido como um valor diferente de zero, nenhum serviço iniciado depois tem permissão para ser executado interativamente, independentemente de ele ter um **\_ \_ processo de serviço interativo**.

> [!IMPORTANT]
> Todos os serviços são executados na sessão 0 dos serviços de terminal. Portanto, se um serviço interativo exibir uma interface do usuário, ele ficará visível somente para o usuário que se conectou à sessão 0. Como não há nenhuma maneira de garantir que o usuário interativo esteja conectado à sessão 0, não configure um serviço para ser executado como um serviço interativo em serviços de terminal ou em um sistema que dê suporte à troca rápida de usuário (a troca rápida de usuário é implementada usando os serviços de terminal).

 

 

 
