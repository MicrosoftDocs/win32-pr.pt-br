---
description: As notificações a seguir são usadas com as funções SetupInstallFile, SetupInstallFileEx e SetupInstallFromInfSection. Para obter mais informações sobre o formato e o uso de notificações, consulte notificações.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notificações de arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921840"
---
# <a name="inf-file-notifications"></a>Notificações de arquivo INF

As notificações a seguir são usadas com as funções [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) . Para obter mais informações sobre o formato e o uso de notificações, consulte [notificações](notifications.md).



| Notificação                                                      | Descrição                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | O arquivo está em uso e a operação atual é atrasada até que o sistema seja reinicializado. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | O idioma do arquivo atual não corresponde ao idioma do sistema.                   |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Já existe uma cópia do arquivo especificado no destino.                             |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Existe uma versão mais recente do arquivo especificado no destino.                            |



 

> [!Note]  
> Como o [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) cria e confirma uma fila de arquivos interna, ele também usa as [notificações de fila de arquivos](file-queue-notifications.md).

 

 

 



