---
description: A interface IUpdateServiceRegistration define as propriedades a seguir.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propriedades de IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824f76c01b428d156d12752d07bb9547517df26a0e621f44a701e94f33340221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814801"
---
# <a name="iupdateserviceregistration-properties"></a>Propriedades de IUpdateServiceRegistration

A interface **IUpdateServiceRegistration** define as propriedades a seguir.



| Propriedade                                                                                      | Descrição                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Obtém um valor booliano que indica se o serviço também será registrado com Atualizações Automáticas, quando adicionado.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Obtém um valor de [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) que indica o estado atual do registro de serviço. |
| [**Serviço**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Obtém um ponteiro para uma interface [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) . Essa propriedade é a propriedade padrão.                                    |



 

 

 



