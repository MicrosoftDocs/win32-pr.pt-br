---
description: A tabela a seguir resume as diferenças entre o desligamento no Windows Vista e no Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Alterações de desligamento do Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011073"
---
# <a name="shutdown-changes-for-windows-vista"></a>Alterações de desligamento do Windows Vista

A tabela a seguir resume as diferenças entre o desligamento no Windows Vista e no Windows XP.



| Recurso                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desligando o bloqueio       | Os aplicativos podem atrasar a resposta ao [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) por 5 segundos e, em seguida, o sistema permite que o usuário encerre o aplicativo. Os aplicativos que retornam **true** em resposta ao **WM \_ QUERYENDSESSION** podem atrasar a resposta ao [**WM \_ EndSession**](wm-endsession.md) por 5 segundos, então o sistema permite que o usuário encerre o aplicativo. | Os aplicativos podem atrasar a resposta ao [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) por 5 segundos e, em seguida, o sistema permite que o usuário continue ou cancele o desligamento. Os aplicativos que retornam **true** em resposta ao **WM \_ QUERYENDSESSION** podem atrasar a resposta ao [**WM \_ EndSession**](wm-endsession.md) por 5 segundos, então o sistema permite que o usuário continue ou cancele o desligamento.                                                                                                      |
| Cancelando o desligamento      | Se um aplicativo retornar **false** em resposta ao [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), o desligamento será cancelado na maioria dos casos. No entanto, nenhuma interface do usuário é exibida e, portanto, talvez ele não esteja ciente de que o desligamento foi cancelado.                                                                                                                                                      | Se um aplicativo retornar **false** em resposta ao [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), ele ainda aparecerá na interface do usuário de desligamento. Observe que o sistema não permite aplicativos de console ou aplicativos sem uma janela visível para cancelar o desligamento. Esses aplicativos serão encerrados automaticamente se não responderem ao **WM \_ QUERYENDSESSION** ou ao [**WM \_ EndSession**](wm-endsession.md) dentro de 5 segundos ou se eles retornarem **falsos** em resposta ao **WM \_ QUERYENDSESSION**. |
| Desligar interface do usuário | O sistema exibe uma caixa de diálogo para cada aplicativo que bloqueia o desligamento. Se o usuário clicar no botão **terminar agora** , o aplicativo será encerrado. Se o usuário clicar no botão **Cancelar** , o desligamento será cancelado e o aplicativo continuará a ser executado.                                                                                                                                    | O sistema exibe uma interface do usuário de tela inteira que identifica todos os aplicativos que bloqueiam o desligamento e seus motivos para fazer isso (se eles tiverem registrado um motivo usando [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Práticas Recomendadas

-   Os aplicativos não devem bloquear o desligamento. Responda ao [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) o mais rápido possível e adie as atividades de limpeza até processar a mensagem de [**\_ EndSession do WM**](wm-endsession.md) .
-   Os aplicativos que devem bloquear o desligamento devem usar a nova função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) para registrar uma cadeia de caracteres que explica o motivo do usuário. O usuário pode decidir se deseja continuar ou cancelar o desligamento.
-   Os aplicativos não podem contar com a capacidade de bloquear o desligamento.

 

 



