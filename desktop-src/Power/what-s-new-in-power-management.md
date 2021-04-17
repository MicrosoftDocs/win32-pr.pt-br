---
description: O Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando ele está em execução em um dispositivo móvel.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novidades no gerenciamento de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775666"
---
# <a name="whats-new-in-power-management"></a>Novidades do gerenciamento de energia

O Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando ele está em execução em um dispositivo móvel.

## <a name="battery-saver"></a>Economia de bateria

Nesta versão, seu aplicativo poderá ser notificado quando a economia de bateria estiver ativada ou desativada. Ao responder às condições de energia em constante mudança, seu aplicativo pode trabalhar em conjunto com a economia de bateria para economizar energia e ajudar a estender a vida útil da bateria. Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ do \_ \_ Status de economia de energia**](power-setting-guids.md) : Use esse novo GUID com a função [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para ser notificado quando a economia de bateria estiver ativada ou desativada.

-   [**Sistema \_ \_Status de energia**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : essa estrutura foi atualizada para dar suporte à economia de bateria. O quarto membro, **SystemStatusFlag** (anteriormente chamado de **Reserved1**), agora indica se a economia de bateria está encarregado ou não. Use a função [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar um ponteiro para essa estrutura.

 

 
