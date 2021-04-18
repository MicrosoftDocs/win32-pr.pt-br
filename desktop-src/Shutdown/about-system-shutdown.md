---
description: O desligamento do sistema leva o sistema a uma condição em que é seguro desligar o computador.
ms.assetid: eeede4b3-8f68-4fe0-b16a-b5449aa27d59
title: Sobre o desligamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590a062c5fcb252709ffd92bc2d6d7c8105571da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753083"
---
# <a name="about-system-shutdown"></a>Sobre o desligamento do sistema

O desligamento do sistema leva o sistema a uma condição em que é seguro desligar o computador. Todos os buffers do sistema de arquivos são liberados para o disco. em seguida, uma caixa de mensagem é exibida informando ao usuário que o computador pode ser desligado. Também há uma opção de reinicialização que reiniciará o computador, em vez de exibir essa caixa de mensagem de desligamento do sistema. Para obter mais informações, consulte [desligando](shutting-down.md). Para obter um exemplo, consulte [como desligar o sistema](how-to-shut-down-the-system.md).

O logoff interrompe todos os processos associados ao contexto de segurança do processo que chamou a função Exit, registra o usuário atual fora do sistema e exibe a caixa de diálogo de logon. Para obter mais informações, consulte [fazendo logoff](logging-off.md). Para obter um exemplo, consulte [como fazer logoff do usuário atual](how-to-log-off-the-current-user.md).

O bloqueio da estação de trabalho protege a exibição de uso não autorizado sempre que você sai do computador. Para desbloquear a estação de trabalho, você deve fazer logon. Para obter um exemplo, consulte [como bloquear a estação de trabalho](how-to-lock-the-workstation.md).

O [controlador de eventos de desligamento](shutdown-event-tracker.md) permite que o usuário ou aplicativo documente o motivo para desligar ou reiniciar o sistema.

 

 



