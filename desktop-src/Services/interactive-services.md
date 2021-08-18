---
description: Normalmente, os serviços são aplicativos de console projetados para executar autônomos sem uma GUI (interface gráfica do usuário).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Serviços Interativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6b99eb41d26d6740a30a314654d92fdd4522f5597ea6e4cbb2a3d443de8120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889464"
---
# <a name="interactive-services"></a>Serviços Interativos

Normalmente, os serviços são aplicativos de console projetados para executar autônomos sem uma GUI (interface gráfica do usuário). No entanto, alguns serviços podem exigir interação ocasional com um usuário. Esta página discute as melhores maneiras de interagir com o usuário de um serviço.

> [!IMPORTANT]
> Os serviços não podem interagir diretamente com um usuário a partir Windows Vista. Portanto, as técnicas mencionadas na seção intitulada Usando um serviço interativo não devem ser usadas em um novo código.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interagindo com um usuário de um serviço indiretamente

Você pode usar as seguintes técnicas para interagir com o usuário de um serviço em todas as versões com suporte do Windows:

-   Exibe uma caixa de diálogo na sessão do usuário usando a [**função WTSSendMessage.**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea)
-   Crie um aplicativo gui oculto separado e use a [**função CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para executar o aplicativo dentro do contexto do usuário interativo. Projete o aplicativo gui para se comunicar com o serviço por meio de algum método de comunicação entre processos (IPC), por exemplo, pipes nomeados. O serviço se comunica com o aplicativo de GUI para informar quando exibir a GUI. O aplicativo comunica os resultados da interação do usuário de volta com o serviço para que o serviço possa tomar a ação apropriada. Observe que o IPC pode expor suas interfaces de serviço pela rede, a menos que você use uma ACL (lista de controle de acesso) apropriada.

    Se esse serviço for executado em um sistema multiusuário, adicione o aplicativo à seguinte chave para que ele seja executado em cada sessão: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**. Se o aplicativo usar pipes nomeados para IPC, o servidor poderá distinguir entre vários processos de usuário, dando a cada pipe um nome exclusivo com base na ID da sessão.

A técnica a seguir também está disponível para Windows Server 2003 e Windows XP:

-   Exibir uma caixa de mensagem chamando a [**função MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) com **MB SERVICE \_ \_ NOTIFICATION**. Isso é recomendado para exibir mensagens de status simples. Não chame **MessageBox** durante a inicialização do serviço ou da rotina [**HandlerEx,**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) a menos que você a chame de um thread separado, para que você retorne ao SCM em tempo hábil.

## <a name="using-an-interactive-service"></a>Usando um serviço interativo

Por padrão, os serviços usam uma estação de janela não [interativa](/windows/desktop/winstation/window-stations) e não podem interagir com o usuário. No entanto, um *serviço interativo* pode exibir uma interface do usuário e receber a entrada do usuário.

> [!Caution]  
> Os serviços em execução em um contexto de segurança elevado, como a conta LocalSystem, não devem criar uma janela na área de trabalho interativa porque qualquer outro aplicativo em execução na área de trabalho interativa pode interagir com essa janela. Isso expõe o serviço a qualquer aplicativo executado por um usuário conectado. Além disso, os serviços que estão sendo executados como LocalSystem não devem acessar a área de trabalho interativa chamando a [**função OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) ou [**GetThreadDesktop.**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop)

 

Para criar um serviço interativo, faça o seguinte ao chamar a [**função CreateService:**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)

1.  Especifique NULL para *o parâmetro lpServiceStartName* para executar o serviço no contexto da [conta LocalSystem](localsystem-account.md).
2.  Especifique **o sinalizador SERVICE INTERACTIVE \_ \_ PROCESS.**

Para determinar se um serviço está em execução como um serviço interativo, chame a função [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) para recuperar um alça para a estação de janela e a função [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) para testar se a estação de janela tem o **atributo WSF \_ VISIBLE.**

No entanto, observe que a seguinte chave do Registro contém um **valor, NoInteractiveServices**, que controla o efeito do PROCESSO \_ INTERATIVO DO \_ SERVIÇO:

**Controle HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ Windows**

O **valor NoInteractiveServices** assume como padrão 1, o que significa que nenhum serviço tem permissão para ser executado interativamente, independentemente de ter **o PROCESSO INTERATIVO DO \_ \_ SERVIÇO.** Quando **NoInteractiveServices** é definido como 0, os serviços com **SERVICE INTERACTIVE \_ \_ PROCESS** têm permissão para executar interativamente.

**Windows 7, Windows Server 2008 R2, Windows XP e Windows Server 2003:** O **valor NoInteractiveServices** assume como padrão 0, o que significa que os serviços com **o SERVICE INTERACTIVE \_ \_ PROCESS** têm permissão para executar interativamente. Quando **NoInteractiveServices** é definido como um valor diferente de zero, nenhum serviço iniciado depois disso tem permissão para ser executado interativamente, independentemente de ter **o SERVICE INTERACTIVE \_ \_ PROCESS**.

> [!IMPORTANT]
> Todos os serviços são executados na sessão 0 dos Serviços de Terminal. Portanto, se um serviço interativo exibir uma interface do usuário, ele será visível somente para o usuário que se conectou à sessão 0. Como não há nenhuma maneira de garantir que o usuário interativo esteja conectado à sessão 0, não configure um serviço para ser executado como um serviço interativo em Serviços de Terminal ou em um sistema que dá suporte à troca rápida de usuários (a troca rápida de usuário é implementada usando os Serviços de Terminal).

 

 

 
