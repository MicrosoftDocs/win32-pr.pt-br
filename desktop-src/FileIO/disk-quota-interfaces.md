---
description: Interfaces usadas com cotas de disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de cota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461285"
---
# <a name="disk-quota-interfaces"></a>Interfaces de cota de disco

As interfaces a seguir são usadas com cotas de disco.



| Interface                                          | Descrição                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Controla os recursos de cota de disco de um único volume do sistema de arquivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Recebe notificações de eventos relacionadas à cota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Representa uma entrada de cota de usuário único no arquivo de informações de cota de volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Adiciona vários objetos de usuário de cota a um contêiner que é enviado para atualização em uma única chamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Enumera as entradas de cota do usuário no volume.<br/>                                                        |



 

 

