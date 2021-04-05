---
description: A interface IUpdateSession3 define os métodos a seguir.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Métodos IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089934"
---
# <a name="iupdatesession3-methods"></a>Métodos IUpdateSession3

A interface [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) define os métodos a seguir.



| Método                                                                           | Descrição                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Retorna um ponteiro para uma interface [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) para a sessão.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Retorna um ponteiro para uma interface [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) . A interface contém registros de eventos correspondentes no computador. Isso faz com que o método [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) consulte de forma síncrona o computador para o histórico de eventos de atualização. |



 

Para obter informações sobre os membros herdados por essa interface, consulte as seguintes interfaces:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



