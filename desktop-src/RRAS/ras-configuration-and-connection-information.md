---
title: Informações de conexão e configuração de RAS
description: Os aplicativos executados no Windows NT 4,0 e versões posteriores e no Windows 95 podem usar a função RasEnumConnections para obter informações sobre as conexões existentes no computador local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuração e conexão, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105778527"
---
# <a name="ras-configuration-and-connection-information"></a>Informações de conexão e configuração de RAS

Os aplicativos executados no Windows NT 4,0 e versões posteriores e no Windows 95 podem usar a função [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obter informações sobre as conexões existentes no computador local. As informações de cada conexão incluem um identificador de conexão e o nome da entrada do catálogo telefônico usado para estabelecer a conexão. Você pode usar o identificador de conexão em uma chamada para a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) obter o status atual da conexão.

O Windows NT Server 4,0 e versões posteriores fornecem duas novas funções para recuperar informações de RAS. O Windows 95does não oferece suporte a essas funções.

A função [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retorna o nome e o tipo dos dispositivos compatíveis com RAS configurados no computador local.

A função [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica um objeto de evento que o sistema sinaliza quando uma conexão RAS é criada ou encerrada.

 

 




