---
description: A interface IAutomaticUpdatesSettings define as propriedades a seguir.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propriedades de IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920973"
---
# <a name="iautomaticupdatessettings-properties"></a>Propriedades de IAutomaticUpdatesSettings

A interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define as propriedades a seguir.



| Propriedade                                                                                 | Descrição                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Obtém e define como os usuários são notificados sobre eventos de atualização automática.                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Obtém um valor booliano que indica se as configurações de atualização automática são somente leitura.         |
| [**Necessário**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Obtém um valor booliano que indica se Política de Grupo requer o serviço Atualizações Automáticas. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Obtém e define os dias da semana em que Atualizações Automáticas instala ou desinstala atualizações.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Obtém e define a hora em que o Atualizações Automáticas instala ou desinstala atualizações.                |



 

> [!Note]  
> O Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 fornecem apenas suporte limitado para [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) e [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Se o computador tiver sido configurado por meio de Política de Grupo para usar um dia e hora de instalação agendada, as propriedades **ScheduledInstallationDay** e **ScheduledInstallationTime** retornarão esse dia e hora agendados. Se o computador não tiver sido configurado por meio de Política de Grupo dessa forma, as propriedades **ScheduledInstallationDay** e **ScheduledInstallationTime** retornarão valores padrão e não confiáveis. Se você tentar modificar o dia e a hora da instalação agendada nesses sistemas operacionais, **ScheduledInstallationDay** e **ScheduledInstallationTime** parecem ter sucesso, mas não têm efeito.

 

 

 



