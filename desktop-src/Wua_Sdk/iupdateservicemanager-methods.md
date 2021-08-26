---
description: A interface IUpdateServiceManager define os métodos a seguir.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Métodos IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1486727db4ed4e9b561c19a1a2f3994bca0085e836ae774fda1c7db76df38144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994346"
---
# <a name="iupdateservicemanager-methods"></a>Métodos IUpdateServiceManager

A interface [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) define os métodos a seguir.



| Método                                                                           | Descrição                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | registra um pacote de verificação como um serviço com o Windows Update Agent (WUA) e, em seguida, retorna uma interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Registra um serviço com WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Registra um serviço com Atualizações Automáticas.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Remove um registro de serviço do WUA.                                                                                                         |
| [**SetOption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Define opções para o objeto que especifica a ID de serviço e se é para exibir um aviso ao alterar o registro de Atualizações Automáticas. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Cancela o registro de um serviço com Atualizações Automáticas.                                                                                                    |



 

 

 



