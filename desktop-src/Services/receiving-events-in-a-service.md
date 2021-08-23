---
description: Um serviço que é um aplicativo de console pode registrar um manipulador de controle de console para receber notificações quando um usuário fizer logoff.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Recebendo eventos em um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe2312989208d5b6587067e64f10401c32229c2b19a7b4846163444576e63ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003704"
---
# <a name="receiving-events-in-a-service"></a>Recebendo eventos em um serviço

Um serviço que é um aplicativo de console pode registrar um [manipulador de controle de console](/windows/console/console-control-handlers) para receber notificações quando um usuário fizer logoff. No entanto, não há nenhum evento de console enviado quando um usuário interativo faz logon. Para obter informações sobre como receber notificações quando um usuário faz logon, consulte [criando um pacote de notificação do Winlogon](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package).

O sistema transmite eventos de alteração do dispositivo para todos os serviços. Esses eventos podem ser recebidos por um serviço em um procedimento de janela ou em seu manipulador de controle de serviço. Para especificar quais eventos seu serviço deve receber, use a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

Certifique-se de manipular Plug and Play eventos de dispositivo o mais rápido possível. Caso contrário, o sistema pode deixar de responder. Se o manipulador de eventos for executar uma operação que possa bloquear a execução (como e/s), é melhor iniciar outro thread para executar a operação de forma assíncrona.

Quando um serviço chama [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa), o serviço também especifica um identificador de janela ou um identificador de status de serviço. Se um serviço especificar um identificador de janela, o procedimento de janela receberá os eventos de notificação. Se um serviço especificar seu identificador de status de serviço, seu manipulador de controle de serviço receberá os eventos de notificação. Para obter mais informações, consulte [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Os identificadores de notificação de dispositivo retornados por [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) devem ser fechados chamando a função [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) quando não forem mais necessários.

 

 
