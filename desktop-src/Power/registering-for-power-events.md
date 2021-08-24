---
description: Os aplicativos podem adaptar melhor seu comportamento ao estado de energia atual do computador Registrando-se para eventos de energia.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrando para eventos de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143319"
---
# <a name="registering-for-power-events"></a>Registrando para eventos de energia

Os aplicativos podem adaptar melhor seu comportamento ao estado de energia atual do computador Registrando-se para eventos de energia. Um aplicativo deve se registrar para cada evento de alteração de energia que possa afetar seu comportamento.

Um aplicativo ou serviço usa a função [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) para se registrar para notificações. Quando a configuração de energia correspondente é alterada, o sistema envia notificações da seguinte maneira:

-   Um aplicativo recebe uma mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) com um *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) e um *lParam* que aponta para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .
-   Um serviço recebe uma chamada para a função de retorno de chamada [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) que ele registrou chamando a função [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . O parâmetro *lpEventData* enviado para a função de retorno de chamada *HandlerEx* aponta para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

Na estrutura [**de \_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , o membro **PowerSetting** contém o GUID que identifica a notificação e o membro de **dados** contém o novo valor da configuração de energia.

Para obter uma lista de GUIDs de configuração de energia para notificações que são mais úteis para aplicativos, consulte [**GUIDs de configuração de energia**](power-setting-guids.md).

 

 
