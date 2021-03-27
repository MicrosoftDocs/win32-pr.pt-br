---
description: As contas de usuário do Windows XP permitem que vários usuários sejam conectados simultaneamente, cada um com suas próprias configurações e cada um executando seus próprios aplicativos.
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: Contas de usuário com troca rápida de usuário e Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104989005"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>Contas de usuário com troca rápida de usuário e Área de Trabalho Remota

As contas de usuário do Windows XP permitem que vários usuários sejam conectados simultaneamente, cada um com suas próprias configurações e cada um executando seus próprios aplicativos. Como um usuário não precisa fazer logoff para permitir o acesso a outro usuário, a área de trabalho de cada usuário é facilmente acessada usando o recurso de troca rápida de usuário. As contas de usuário também incluem o recurso de Terminal Server pessoal ou Área de Trabalho Remota, que permite aos usuários acessar sua conta de área de trabalho por meio de sistemas remotos.

Os tópicos a seguir são discutidos.

-   [Requisitos de uso da infraestrutura](#infrastructure-usage-requirements)
-   [Compatibilidade com aplicativos existentes](#compatibility-with-existing-applications)
-   [Registrando para notificação de alternância de sessão](#registering-for-session-switching-notification)
-   [Garantindo que apenas uma instância do seu aplicativo esteja em execução](#ensuring-only-one-instance-of-your-application-is-running)
-   [Desligando seu aplicativo em todas as sessões](#shutting-down-your-application-across-all-sessions)
-   [Interação com serviços do sistema](#interaction-with-system-services)
-   [Área de Trabalho Remota e largura de banda](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>Requisitos de uso da infraestrutura

A infraestrutura subjacente herdada do Windows 2000 dá suporte à separação de estado dos dados do usuário, configurações do usuário e configurações do computador. Aproveitando essa infraestrutura, os itens a seguir são necessários para executar com êxito o aplicativo no Windows XP.

-   O padrão é a pasta **meus documentos** para armazenamento de dados criados pelo usuário.
-   Classifique e armazene dados de aplicativo corretamente.
-   Degradar normalmente as mensagens de "acesso negado".

Arquivos temporários, arquivos mapeados por memória e documentos devem ser armazenados no subdiretório apropriado do diretório de perfil do usuário. Use [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para determinar o local de armazenamento apropriado para esses arquivos. Passar o sinalizador [**CSIDL \_ AppData**](csidl.md) para essas funções retorna o caminho de um diretório do sistema de arquivos que serve como um repositório comum para dados específicos do aplicativo. Use o sinalizador [**CSIDL \_ local de \_ AppData**](csidl.md) no lugar da **CSIDL \_ AppData** para dados que devem ser alterados quando o usuário mudar, como arquivos temporários.

Os requisitos listados acima são um subconjunto daqueles no programa de certificação da Microsoft. Para obter mais informações, consulte a página **Certified for Windows Program** em https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx .

## <a name="compatibility-with-existing-applications"></a>Compatibilidade com aplicativos existentes

A troca rápida de usuário e a Terminal Server pessoal usam a tecnologia de serviços de terminal e, portanto, são compatíveis com a maioria dos aplicativos Microsoft Win32 mais antigos. Se um aplicativo for compatível com o logotipo do Windows 2000, implementando recursos básicos de separação de perfil e gerenciamento de energia, esse aplicativo deverá ser executado corretamente em contas de usuário individuais do Windows XP.

## <a name="registering-for-session-switching-notification"></a>Registrando para notificação de alternância de sessão

Normalmente, um aplicativo não precisa ser notificado quando ocorre uma comutador de área de trabalho. No entanto, os aplicativos que devem ser notificados quando a conta sob a qual estão sendo executados são a área de trabalho atual, como aplicativos que acessam a porta serial ou outros recursos compartilhados, podem se registrar para a notificação do comutador da área de trabalho. Para registrar-se para uma notificação, use a função [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) .

Depois que essa função for chamada, a janela com o identificador *HWND* será registrada para receber uma mensagem de [**alteração do WM \_ \_ WTSSESSION**](../termserv/wm-wtssession-change.md) por meio de sua função **WndProc** . A ID de sessão é enviada no parâmetro **lParam** e um código que indica o evento que gerou a mensagem é enviado em **wParam** como um dos sinalizadores a seguir.

-   \_conexão do console do WTS \_
-   desconexão do console do WTS \_ \_
-   \_conexão remota \_ WTS
-   \_desconexão remota WTS \_
-   \_logoff de sessão WTS \_
-   \_logon de sessão do WTS \_

Os aplicativos podem usar essa mensagem para controlar seu estado, bem como para liberar e adquirir recursos específicos do console. As áreas de trabalho do usuário podem ser alternadas dinamicamente entre o controle remoto e o console. Os aplicativos devem usar a mensagem de [**\_ \_ alteração do WM WTSSESSION**](../termserv/wm-wtssession-change.md) para sincronizar com o estado de conexão remota ou local.

Quando o processo não exige mais essas notificações ou está sendo encerrado, ele deve chamar [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) para cancelar o registro de sua notificação.

> [!IMPORTANT]
> Os valores de **HWND** passados para [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) são contados como referência, portanto, você deve fazer um número igual de chamadas para [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) para garantir o lançamento de todos os recursos alocados.

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>Garantindo que apenas uma instância do seu aplicativo esteja em execução

Muitos aplicativos devem garantir que eles tenham apenas uma instância em execução. Há várias maneiras de fazer isso no Windows XP. Entre elas, estão as seguintes:

-   Use [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) ou [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) para procurar uma janela conhecida que seu aplicativo abra. Se essa janela já estiver aberta, você poderá usá-la como uma indicação de que o aplicativo já está em execução.
-   Crie um objeto mutex ou Semaphore quando seu aplicativo for aberto e feche esse objeto quando o aplicativo for encerrado. O namespace do objeto global é separado para cada área de trabalho, permitindo uma lista exclusiva de objetos mutex e Semaphore para cada um.

## <a name="shutting-down-your-application-across-all-sessions"></a>Desligando seu aplicativo em todas as sessões

Um aplicativo pode precisar ser desligado em todas as sessões. Por exemplo, um aplicativo em execução em duas ou mais sessões pode, simultaneamente, baixar um novo arquivo da Web. Em seguida, talvez seja necessário fechar a si mesmo e reiniciar com os bits atualizados. Isso, é claro, precisaria ser feito em todas as sessões em execução. Seu aplicativo deve ser escrito para que ele saia corretamente quando uma notificação é recebida.

## <a name="interaction-with-system-services"></a>Interação com serviços do sistema

Do ponto de vista programático, os casos a seguir precisam ser resolvidos.

-   O processo do servidor recebe uma solicitação direta de um processo de cliente.

    Nesse caso, a mensagem é provavelmente transmitida usando uma LPC (chamada de procedimento local) ou uma RPC (chamada de procedimento remoto). Há APIs para LPC ou RPC que habilitam a recuperação do token do cliente. Depois que o token do cliente é obtido, o servidor pode usá-lo em uma chamada para [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera). Isso abre o processo na estação de janela correta, supondo que o token de usuário do cliente tenha uma marca de sessão, o que deveria.

    > [!Note]  
    > O [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) não dá suporte à herança de identificador entre sessões no momento.

     

-   O processo do servidor recebe uma notificação e precisa exibir a interface de usuário, mas a exibição não precisa estar no contexto do usuário atual.

    Nesse caso, o processo do servidor pode duplicar seu token de processo primário e alterar o identificador da sessão em questão para corresponder ao identificador da sessão atual. O identificador de sessão atual pode ser obtido usando a função [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) .

    > [!Note]  
    > Para definir a ID de sessão do token, você precisa do **\_ \_ privilégio do se TCB**. Você só terá isso como um serviço em execução no sistema de Autoridade NT \\ .

     

## <a name="remote-desktop-and-bandwidth"></a>Área de Trabalho Remota e largura de banda

Com a adição do recurso de Área de Trabalho Remota ao Windows XP, os aplicativos devem fazer um esforço para não usar mais largura de banda do que o necessário, evitando desenhos de tela e efeitos de animação extensivos se a área de trabalho estiver conectada remotamente. Para determinar se a sessão atual é remota, você pode chamar [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com **SM \_ REMOTESESSION**. No entanto, lembre-se de que essa chamada não faz distinção entre o remoto e o desconectado.

 

 
