---
description: 'Há três maneiras de um aplicativo desligar computadores locais ou remotos: Desligue o systemshut do sistema e reinicie o itshut do aplicativo, desligue e reinicie o sistema e reinicie todos os aplicativos que foram registrados para reinicialização'
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: Desligando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c91309172bc1c057cf2226331f0a4d34a10ec39e57c4b32390e024ecf9b127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963543"
---
# <a name="shutting-down"></a>Desligando

Há três maneiras de um aplicativo desligar computadores locais ou remotos:

-   desligar o sistema
-   desligar o sistema e reiniciá-lo
-   Desligue o aplicativo, desligue e reinicie o sistema e reinicie todos os aplicativos que foram registrados para reinicialização

Para desligar o sistema, use a função [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) com o sinalizador de \_ desligamento EWX. Para obter um exemplo, consulte [como desligar o sistema](how-to-shut-down-the-system.md). Para desligar e reiniciar o sistema, use o sinalizador de \_ reinicialização EWX. Para reiniciar os aplicativos que foram registrados para reinicialização usando a função [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) , use o \_ sinalizador EXW RESTARTAPPS.

As funções [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) iniciam um temporizador e exibem uma caixa de diálogo que solicita que o usuário faça logoff. Enquanto essa caixa de diálogo é exibida, a função [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) pode parar o temporizador e impedir que o computador seja desligado. No entanto, se o temporizador expirar, o computador será desligado. Essas funções também podem reiniciar o computador após uma operação de desligamento. Para obter mais informações, consulte [exibindo a caixa de diálogo de desligamento](displaying-the-shutdown-dialog-box.md).

## <a name="shutdown-notifications"></a>Notificações de desligamento

Os aplicativos com uma janela e fila de mensagens recebem notificações de desligamento por meio das mensagens de [**\_ EndSession**](wm-endsession.md) do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) e do WM. Esses aplicativos devem retornar **true** para indicar que eles podem ser encerrados. Os aplicativos não devem bloquear o desligamento do sistema, a menos que seja absolutamente necessário. Os aplicativos devem executar qualquer limpeza necessária durante o processamento do **WM \_ EndSession**. Os aplicativos que têm dados não salvos podem salvar os dados em um local temporário e restaurá-los na próxima vez que o aplicativo for iniciado. É recomendável que os aplicativos salvem seus dados e Estados com frequência; por exemplo, salve automaticamente os dados entre as operações de salvamento iniciadas pelo usuário para reduzir a quantidade de dados a serem salvos no desligamento.

Os aplicativos de console recebem notificações de desligamento em suas rotinas de manipulador. Para registrar um manipulador de console, use a função [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) .

Os aplicativos de serviço recebem notificações de desligamento em suas rotinas de manipulador. Para registrar um manipulador de controle de serviço, use a função [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .

## <a name="blocking-shutdown"></a>Desligando o bloqueio

Se um aplicativo precisar bloquear um possível desligamento do sistema, ele poderá chamar a função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . O chamador fornece uma cadeia de caracteres de motivo que será exibida para o usuário. A cadeia de caracteres de motivo deve ser curta e clara, fornecendo ao usuário as informações necessárias para decidir se deseja continuar desligando o sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como desligar o sistema](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
