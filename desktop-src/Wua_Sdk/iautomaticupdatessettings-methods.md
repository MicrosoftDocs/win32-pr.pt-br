---
description: A interface IAutomaticUpdatesSettings define os métodos a seguir.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Métodos IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827703"
---
# <a name="iautomaticupdatessettings-methods"></a>Métodos IAutomaticUpdatesSettings

A interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define os métodos a seguir.



| Método                                               | Descrição                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Atualizar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera as configurações de Atualizações Automáticas mais recentes. |
| [**Salvar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Aplica as configurações de Atualizações Automáticas atuais.  |



 

> [!Note]  
> No Windows RT, você não pode mais usar o método [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para definir configurações de Windows Update de forma programática. A operação de configuração falhará se você usar **salvar** para definir qualquer valor diferente de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



