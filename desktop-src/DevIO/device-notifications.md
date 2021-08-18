---
description: O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificações de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12186ab6349057258d723f7e690e889b7e79af4abe47f714055599cb6f648333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636616"
---
# <a name="device-notifications"></a>Notificações de dispositivo

O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços. Você não precisa se registrar para receber esses eventos padrão. Consulte a seção Comentários em [**RegisterDeviceNotification para**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) obter detalhes. Para especificar outros eventos que seu aplicativo ou serviço deve receber, use **a função RegisterDeviceNotification.**

Quando um aplicativo ou serviço chama [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), ele também especifica a janela que receberá os eventos de notificação. Os serviços podem especificar um alça de status do serviço em vez de um alça de janela. Se um serviço especificar seu manipulador de status de serviço, seu manipulador de controle de serviço receberá os eventos de notificação. Para obter mais informações, consulte [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Certifique-se de manipular Plug and Play eventos de dispositivo o mais rápido possível. Caso contrário, o sistema poderá ficar sem resposta. Se o manipulador de eventos for executar uma operação que pode bloquear a execução (como E/S), é melhor iniciar outro thread para executar a operação de forma assíncrona.

Os alças de notificação do dispositivo retornados por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devem ser fechados chamando a [**função UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando não são mais necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro para notificação de dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
