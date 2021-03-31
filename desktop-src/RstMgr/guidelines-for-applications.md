---
title: Diretrizes para aplicativos
description: Os aplicativos executados no Windows Vista e no Windows Server 2008 devem aderir a essas diretrizes para garantir que o Gerenciador de reinicialização possa desligar e reiniciar os aplicativos, se necessário, para instalar atualizações.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641681"
---
# <a name="guidelines-for-applications"></a>Diretrizes para aplicativos

Os aplicativos executados no Windows Vista e no Windows Server 2008 devem aderir a essas diretrizes para garantir que o Gerenciador de reinicialização possa desligar e reiniciar os aplicativos, se necessário, para instalar atualizações. Os serviços podem usar as diretrizes descritas em [diretrizes para serviços](guidelines-for-services.md).

-   O Gerenciador de reinicialização consulta aplicativos de GUI para desligamento enviando uma notificação do [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) que tem o parâmetro *lParam* definido como **EndSession \_ CLOSEAPP** (0x1). Os aplicativos não devem ser desligados quando recebem uma mensagem do **WM \_ QUERYENDSESSION** porque outro aplicativo pode não estar pronto para ser desligado. Os aplicativos de GUI devem escutar a mensagem do **WM \_ QUERYENDSESSION** e retornar um valor **true** se o aplicativo estiver preparado para ser desligado e reiniciado. Se nenhum aplicativo retornar um valor **false**, o Gerenciador de reinicialização enviará uma mensagem de [**\_ EndSession do WM**](/windows/desktop/Shutdown/wm-endsession) com o parâmetro *lParam* definido como **EndSession \_ CLOSEAPP** (0x1) e o parâmetro *wParam* definido como **true**. Os aplicativos devem ser desligados somente quando recebem a mensagem de **\_ EndSession do WM** . O Gerenciador de reinicialização também envia uma mensagem de [**\_ fechamento do WM**](../winmsg/wm-close.md) para aplicativos de GUI que não são desligados ao receber o **WM \_ EndSession**. Se qualquer aplicativo de GUI responder a uma mensagem do **WM \_ QUERYENDSESSION** retornando um valor **false**, o desligamento será cancelado. No entanto, se o desligamento for forçado, o aplicativo será encerrado independentemente.
-   Quando um aplicativo de GUI recebe uma mensagem de [**\_ EndSession do WM**](/windows/desktop/Shutdown/wm-endsession) , o aplicativo deve se preparar para ser desligado dentro do período de tempo limite especificado. No mínimo, os aplicativos devem se preparar salvando quaisquer dados de usuário e informações de estado necessárias após uma reinicialização. É recomendável que os aplicativos salvem periodicamente os dados e o estado do usuário.
-   O Gerenciador de reinicialização envia uma notificação de **\_ \_ evento CTRL C** para os aplicativos de console que devem ser desligados e reiniciados. Quando um aplicativo de console recebe uma notificação de **\_ \_ evento CTRL C** , o aplicativo deve executar ações necessárias para se preparar para um desligamento dentro do período de tempo limite especificado. No mínimo, os aplicativos de console devem definir uma função [*HandlerRoutine*](/windows/console/handlerroutine) para manipular a notificação de **\_ \_ eventos CTRL C** e devem salvar quaisquer dados de usuário e informações de estado que serão necessárias após uma reinicialização. É recomendável que os aplicativos salvem periodicamente os dados e o estado do usuário.
-   Se algum aplicativo não for desligado em resposta às mensagens de desligamento, os instaladores poderão usar a opção **RmForceShutdown** da função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) para forçar a desligamento dos aplicativos. Quando o instalador especifica um desligamento forçado, o Gerenciador de reinicialização tenta desligar os aplicativos de forma limpa, enviando as mensagens de desligamento, mas as forçará a fechar se isso falhar. Aplicativos de GUI e aplicativos de console podem ser forçados a desligar para habilitar a instalação de uma atualização de segurança crítica. Como isso pode resultar em perda de dados, os aplicativos devem lidar com as mensagens de desligamento e desligar corretamente quando necessário.
-   Os aplicativos devem se registrar para uma reinicialização usando a função [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) . O Gerenciador de reinicialização só pode reiniciar os aplicativos que foram registrados para reinicialização. Essa é a única maneira que o Gerenciador de reinicialização pode determinar o comando de linha de comando a ser usado ao reiniciar o aplicativo. Se o aplicativo precisar ser reaberto com algum estado ou dados salvos, essas informações deverão ser incluídas no comando de linha de comando que está registrado para o aplicativo.
    > [!Note]  
    > Se o aplicativo reiniciado deve ser executado no mesmo diretório em que foi executado antes de ser desligado, o aplicativo deve salvar as informações do diretório e, em seguida, alterar para o diretório após a reinicialização.

     

    > [!Note]  
    > A função [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) não reinicia os aplicativos que não são executados como o usuário conectado no momento. Por exemplo, a função **RmRestart** não reinicia aplicativos iniciados com o comando **Executar como** que não são executados como o usuário conectado no momento. Esses aplicativos devem ser reiniciados manualmente.

     

-   Quando o Gerenciador de reinicialização determinar que uma reinicialização do sistema é necessária para instalar uma atualização, ele não desligará nenhum aplicativo e serviço. Em vez disso, ele deixa isso no instalador para decidir quando agendar uma reinicialização do sistema e instalar a atualização. Os instaladores podem reduzir a interrupção para os usuários causados por atualizações que exigem uma reinicialização do sistema usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) com o sinalizador **EWX \_ RESTARTAPPS** ou a função [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) com o sinalizador **Shutdown \_ RESTARTAPPS** . O uso desses sinalizadores garante que os aplicativos registrados para reinicialização sejam reiniciados após uma reinicialização do sistema, o que minimiza o impacto sobre o usuário.

 

 