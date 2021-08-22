---
description: Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando estiver em execução em um dispositivo móvel.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novidades no gerenciamento de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143189"
---
# <a name="whats-new-in-power-management"></a>Novidades do gerenciamento de energia

Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando ele está em execução em um dispositivo móvel.

## <a name="battery-saver"></a>Economia de bateria

Nesta versão, seu aplicativo poderá ser notificado quando a economia de bateria estiver ativada ou desativada. Ao responder às condições de energia em constante mudança, seu aplicativo pode trabalhar em conjunto com a economia de bateria para economizar energia e ajudar a estender a vida útil da bateria. Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ do \_ \_ Status de economia de energia**](power-setting-guids.md) : Use esse novo GUID com a função [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para ser notificado quando a economia de bateria estiver ativada ou desativada.

-   [**Sistema \_ \_Status de energia**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : essa estrutura foi atualizada para dar suporte à economia de bateria. O quarto membro, **SystemStatusFlag** (anteriormente chamado de **Reserved1**), agora indica se a economia de bateria está encarregado ou não. Use a função [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar um ponteiro para essa estrutura.

 

 
