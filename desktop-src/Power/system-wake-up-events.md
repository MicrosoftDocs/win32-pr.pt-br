---
description: Seu aplicativo pode restaurar um computador que está em estado de suspensão para o estado de funcionamento usando um temporizador agendado ou um evento de dispositivo.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Eventos de ativação do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779592"
---
# <a name="system-wake-up-events"></a>Eventos de ativação do sistema

As informações a seguir se aplicam a ativação de [suspensão (S3) e hibernar (S4)](/windows-hardware/drivers/kernel/system-sleeping-states). Para ativações do modo de espera moderno (S0 ocioso de baixa energia), consulte [transições de ocioso para ativo](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

Seu aplicativo pode restaurar um computador que está em estado de suspensão para o estado de funcionamento usando um temporizador agendado ou um evento de dispositivo. Isso é conhecido como um *evento de ativação*. Use um [objeto de temporizador](/windows/desktop/Sync/waitable-timer-objects) que pode ser aguardado para especificar a hora em que o sistema deve ser ativado. Para criar o objeto, use a função [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Para definir o temporizador, use a função [**SetWaitableTimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) . O parâmetro *pDueTime* especifica quando o temporizador será sinalizado. Para especificar que o sistema deve ser ativado quando o temporizador for sinalizado, defina o parâmetro *fResume* como **true**.

Quando o sistema é ativado automaticamente por causa de um evento (diferente do comutador de energia ou atividade do usuário), o sistema define automaticamente um temporizador ocioso autônomo para pelo menos 2 minutos. Esse temporizador fornece aos aplicativos tempo suficiente para chamar a função [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que estão ocupados. Esse tempo permite que o sistema retorne ao estado de suspensão rapidamente depois que o computador não for mais necessário. Os critérios a seguir determinam se o sistema retorna ao estado de suspensão:

-   Se o sistema for ativado automaticamente (ou seja, nenhuma atividade do usuário estiver presente), ele será desligado assim que o temporizador ocioso autônomo expirar, supondo que nenhum aplicativo tenha chamado [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que o sistema é necessário.
-   As ativações baseadas em dispositivo disparam o temporizador ocioso autônomo por padrão, a menos que o driver de dispositivo indique a presença do usuário. Se o driver indicar a presença do usuário, o timer de ociosidade do sistema será usado.
-   Se o sistema for ativado automaticamente, mas o usuário fornecer nova entrada enquanto o evento for manipulado, o sistema não retornará automaticamente ao modo de suspensão com base no timer de ociosidade autônomo. Em vez disso, o sistema retorna ao estado de suspensão com base no timer de ociosidade do sistema.
-   Se o sistema for ativado devido à atividade do usuário, o sistema não retornará automaticamente ao modo de suspensão com base no timer de ociosidade autônomo. Em vez disso, o sistema retorna ao estado de suspensão com base no timer de ociosidade do sistema.

Quando o sistema é ativado automaticamente, ele difunde o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) para todos os aplicativos. Como o usuário não está presente, a maioria dos aplicativos não deve fazer nada. Aplicativos de manipulação de eventos, como servidores de fax, devem lidar com seus eventos. Para determinar se o sistema está nesse estado, chame a função [**IsSystemResumeAutomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) . Quando o sistema é ativado automaticamente, a exibição não é ativada automaticamente.

Se o sistema for ativado devido à atividade do usuário, o sistema primeiro transmitirá o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) seguido por um evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) . Além disso, o sistema ativará a exibição. Seu aplicativo deve reabrir os arquivos que ele fechou quando o sistema entrou em suspensão e se preparar para a entrada do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> <dt>

[Critérios de suspensão do sistema](system-sleep-criteria.md)
</dt> </dl>

 

 
