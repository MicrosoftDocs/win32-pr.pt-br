---
title: Diretrizes para aplicativos
description: Os aplicativos em execução no Windows Vista e no Windows Server 2008 devem seguir essas diretrizes para garantir que o Gerenciador de Reinicialização possa desligar e reiniciar aplicativos, se necessário, para instalar atualizações.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9624f578a04267b94bde41bbdf8e3312e7b8ae0f4fb84280212ea51c2db7e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010124"
---
# <a name="guidelines-for-applications"></a>Diretrizes para aplicativos

Os aplicativos em execução no Windows Vista e no Windows Server 2008 devem seguir essas diretrizes para garantir que o Gerenciador de Reinicialização possa desligar e reiniciar aplicativos, se necessário, para instalar atualizações. Os serviços podem usar as diretrizes descritas em [Diretrizes para Serviços](guidelines-for-services.md).

-   O Gerenciador de Reinicialização consulta aplicativos gui para desligamento enviando uma notificação [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) que tem o parâmetro *lParam* definido como **ENDSESSION \_ CLOSEAPP** (0x1). Os aplicativos não devem ser desligados quando recebem uma **mensagem WM \_ QUERYENDSESSION** porque outro aplicativo pode não estar pronto para ser desligado. Os aplicativos de GUI devem escutar a mensagem **WM \_ QUERYENDSESSION** e retornar um valor **true** se o aplicativo estiver preparado para desligar e reiniciar. Se nenhum aplicativo retornar um valor **false**, o Gerenciador de Reinicialização enviará uma mensagem [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) com o parâmetro *lParam* definido como **ENDSESSION \_ CLOSEAPP** (0x1) e o parâmetro *wparam* definido como **TRUE.** Os aplicativos devem ser desligados somente quando recebem a **mensagem WM \_ ENDSESSION.** O Gerenciador de Reinicialização também envia [**uma mensagem WM \_ CLOSE**](../winmsg/wm-close.md) para aplicativos de GUI que não são desligados ao receber **WM \_ ENDSESSION**. Se qualquer aplicativo gui responder a uma mensagem **WM \_ QUERYENDSESSION** retornando um valor **false**, o desligamento será cancelado. No entanto, se o desligamento for forçado, o aplicativo será encerrado independentemente.
-   Quando um aplicativo de GUI recebe uma mensagem [**WM \_ ENDSESSION,**](/windows/desktop/Shutdown/wm-endsession) o aplicativo deve se preparar para desligar dentro do período de tempo máximo especificado. No mínimo, os aplicativos devem se preparar salvando todos os dados de usuário e informações de estado necessários após uma reinicialização. É recomendável que os aplicativos salvem periodicamente os dados e o estado do usuário.
-   O Gerenciador de Reinicialização envia uma **notificação CTRL \_ C \_ EVENT** para aplicativos de console que devem ser desligados e reiniciados. Quando um aplicativo de console recebe uma notificação **CTRL \_ C \_ EVENT,** o aplicativo deve tomar as ações necessárias para se preparar para um desligamento dentro do período de tempo máximo especificado. No mínimo, os aplicativos de console devem definir uma função [*HandlerRoutine*](/windows/console/handlerroutine) para lidar com a notificação **CTRL \_ C \_ EVENT** e devem salvar todos os dados de usuário e informações de estado que serão necessárias após uma reinicialização. É recomendável que os aplicativos salvem periodicamente os dados e o estado do usuário.
-   Se algum aplicativo não for desligado em resposta às mensagens de desligamento, os instaladores poderão usar a opção **RmForceShutdown** da [**função RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) para forçar o desligamento dos aplicativos. Quando o instalador especifica um desligamento forçado, o Gerenciador de Reinicialização tenta desligar os aplicativos corretamente enviando as mensagens de desligamento, mas os força a desligar se isso falhar. Aplicativos de GUI e aplicativos de console podem ser forçados a desligar para habilitar a instalação de uma atualização de segurança crítica. Como isso pode resultar em perda de dados, os aplicativos devem manipular as mensagens de desligamento e desligar corretamente quando necessário.
-   Os aplicativos devem se registrar para uma reinicialização usando [**a função RegisterApplicationRestart.**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) O Gerenciador de Reinicialização só pode reiniciar aplicativos que foram registrados para reinicialização. Essa é a única maneira que o Gerenciador de Reinicialização pode determinar o comando de linha de comando a ser usado ao reiniciar o aplicativo. Se o aplicativo tiver que reabrir com algum estado ou dados salvos, essas informações deverão ser incluídas no comando de linha de comando registrado para o aplicativo.
    > [!Note]  
    > Se o aplicativo reiniciado deve ser executado no mesmo diretório em que ele foi executado antes de ser desligado, o aplicativo deve salvar as informações do diretório e, em seguida, alterar para o diretório depois de reiniciar.

     

    > [!Note]  
    > A [**função RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) não reinicia aplicativos que não são executados como o usuário conectado no momento. Por exemplo, a **função RmRestart** não reinicia aplicativos iniciados com o comando **Executar** como que não são executados como o usuário conectado no momento. Esses aplicativos devem ser reiniciados manualmente.

     

-   Quando o Restart Manager determina que uma reinicialização do sistema é necessária para instalar uma atualização, ele não desliga nenhum aplicativo e serviços. Em vez disso, ele deixa isso para o instalador decidir quando agendar uma reinicialização do sistema e instalar a atualização. Os instaladores podem reduzir a interrupção para os usuários causadas por atualizações que exigem uma reinicialização do sistema usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) com o sinalizador **EWX \_ RESTARTAPPS** ou a função [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) com o sinalizador **SHUTDOWN \_ RESTARTAPPS.** O uso desses sinalizadores garante que os aplicativos registrados para reinicialização sejam reiniciados após uma reinicialização do sistema, o que minimiza o impacto sobre o usuário.

 

 