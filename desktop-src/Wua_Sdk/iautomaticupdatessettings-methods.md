---
description: A interface IAutomaticUpdatesSettings define os métodos a seguir.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Métodos IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049464"
---
# <a name="iautomaticupdatessettings-methods"></a>Métodos IAutomaticUpdatesSettings

A interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define os métodos a seguir.



| Método                                               | Descrição                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Atualizar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera as configurações de Atualizações Automáticas mais recentes. |
| [**Salvar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Aplica as configurações de Atualizações Automáticas atuais.  |



 

> [!Note]  
> no Windows RT, você não pode mais usar o método [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para definir as configurações de Windows Update de forma programática. A operação de configuração falhará se você usar **salvar** para definir qualquer valor diferente de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



