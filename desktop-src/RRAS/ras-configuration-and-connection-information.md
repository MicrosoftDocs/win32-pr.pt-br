---
title: Informações de conexão e configuração de RAS
description: os aplicativos executados no Windows NT 4,0 e versões posteriores e Windows 95 podem usar a função RasEnumConnections para obter informações sobre as conexões existentes no computador local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuração e conexão, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673426"
---
# <a name="ras-configuration-and-connection-information"></a>Informações de conexão e configuração de RAS

os aplicativos executados no Windows NT 4,0 e versões posteriores e Windows 95 podem usar a função [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obter informações sobre as conexões existentes no computador local. As informações de cada conexão incluem um identificador de conexão e o nome da entrada do catálogo telefônico usado para estabelecer a conexão. Você pode usar o identificador de conexão em uma chamada para a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) obter o status atual da conexão.

Windows NT O Server 4,0 e versões posteriores fornecem duas novas funções para recuperar informações de RAS. Windows 95does não oferece suporte a essas funções.

A função [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retorna o nome e o tipo dos dispositivos compatíveis com RAS configurados no computador local.

A função [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica um objeto de evento que o sistema sinaliza quando uma conexão RAS é criada ou encerrada.

 

 




