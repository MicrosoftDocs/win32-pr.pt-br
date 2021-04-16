---
description: O sistema transmite uma mensagem para todos os aplicativos e drivers instaláveis sempre que ocorre um evento de gerenciamento de energia.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757747"
---
# <a name="wm_powerbroadcast-messages"></a>\_Mensagens POWERBROADCAST do WM

O sistema transmite uma mensagem para todos os aplicativos e drivers instaláveis sempre que ocorre um evento de gerenciamento de energia. O sistema transmite esses eventos por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , definindo o parâmetro *wParam* como o evento de gerenciamento de energia apropriado. Por exemplo, o evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica uma alteração no status de energia do sistema. Você deve garantir que seu aplicativo responda corretamente à mensagem do **WM \_ POWERBROADCAST** .

O sistema transmite um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) imediatamente antes de suspender a operação. Isso oferece aos aplicativos e drivers uma última chance de se preparar para o evento. Em muitos casos, o sistema transmite essas mensagens sem solicitar permissão para fazer isso. Isso acontece, por exemplo, se um aplicativo força a suspensão com a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

O sistema transmite o evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) ou [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) quando a operação do sistema é restaurada. Se um aplicativo recebeu um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de o computador ser suspenso, ele receberá o \_ evento PBT APMRESUMESUSPEND. Caso contrário, ele receberá o \_ evento PBT APMRESUMECRITICAL.

O sistema envia um evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) para aplicativos que se registraram para o evento específico usando [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Para obter mais informações, consulte [registrando para eventos de energia](registering-for-power-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> </dl>

 

 



