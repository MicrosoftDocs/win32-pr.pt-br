---
description: O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificações do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089443"
---
# <a name="device-notifications"></a>Notificações do dispositivo

O sistema transmite um conjunto de eventos de alteração de dispositivo padrão para todos os aplicativos e serviços. Você não precisa se registrar para receber esses eventos padrão. Consulte a seção comentários em [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obter detalhes. Para especificar outros eventos que seu aplicativo ou serviço deve receber, use a função **RegisterDeviceNotification** .

Quando um aplicativo ou serviço chama [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), ele também especifica a janela que receberá os eventos de notificação. Os serviços podem especificar um identificador de status de serviço em vez de um identificador de janela. Se um serviço especificar seu identificador de status de serviço, seu manipulador de controle de serviço receberá os eventos de notificação. Para obter mais informações, consulte [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Certifique-se de manipular Plug and Play eventos de dispositivo o mais rápido possível. Caso contrário, o sistema pode deixar de responder. Se o manipulador de eventos for executar uma operação que possa bloquear a execução (como e/s), é melhor iniciar outro thread para executar a operação de forma assíncrona.

Os identificadores de notificação de dispositivo retornados por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) devem ser fechados chamando a função [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) quando não forem mais necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro para notificação de dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
