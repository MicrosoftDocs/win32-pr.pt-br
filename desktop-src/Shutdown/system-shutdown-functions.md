---
description: As funções a seguir são usadas com o desligamento do sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funções de desligamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664336"
---
# <a name="system-shutdown-functions"></a>Funções de desligamento do sistema

As funções a seguir são usadas com o desligamento do sistema.



| Função                                                         | Descrição                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Interrompe um desligamento do sistema que foi iniciado.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Faz logoff do usuário interativo.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Faz logoff do usuário interativo, desliga o sistema ou desliga e reinicia o sistema.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Inicia um desligamento e reinicialização do computador especificado e reinicia todos os aplicativos que foram registrados para reinicialização.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Inicia um desligamento e uma reinicialização opcional do computador especificado.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Inicia um desligamento e uma reinicialização opcional do computador especificado e, opcionalmente, registra o motivo do desligamento.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Bloqueia a exibição da estação de trabalho.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indica que o sistema não pode ser desligado e define uma cadeia de caracteres de motivo a ser exibida para o usuário se o desligamento do sistema for iniciado. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indica que o sistema pode ser desligado e libera a cadeia de caracteres de motivo.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Recupera a cadeia de caracteres de motivo definida pela função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .                     |



 

 

 



