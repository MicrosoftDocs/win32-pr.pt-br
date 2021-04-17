---
description: A interface IUpdateServiceRegistration define as propriedades a seguir.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propriedades de IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811438"
---
# <a name="iupdateserviceregistration-properties"></a>Propriedades de IUpdateServiceRegistration

A interface **IUpdateServiceRegistration** define as propriedades a seguir.



| Propriedade                                                                                      | Descrição                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Obtém um valor booliano que indica se o serviço também será registrado com Atualizações Automáticas, quando adicionado.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Obtém um valor de [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) que indica o estado atual do registro de serviço. |
| [**Serviço**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Obtém um ponteiro para uma interface [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) . Essa propriedade é a propriedade padrão.                                    |



 

 

 



