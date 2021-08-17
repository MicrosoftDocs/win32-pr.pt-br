---
title: Notificações informativas
description: Para os estados de conexão conhecidos como estados em execução, nenhuma ação é necessária do manipulador de notificação, a menos que ocorra um erro.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f526dcd0cd52eaa15929f970debe3ba78788fdb7525e734ee2e26e348b32552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790990"
---
# <a name="informational-notifications"></a>Notificações informativas

Para os [estados de conexão](connection-states.md) conhecidos como estados em execução, nenhuma ação é necessária do manipulador de notificação, a menos que ocorra um erro. Os estados em execução ocorrem durante as partes da operação de conexão que o RAS trata automaticamente, como conectar-se aos dispositivos necessários, autenticar o usuário e aguardar um retorno de chamada do servidor remoto. A notificação é simplesmente um relatório de progresso para o cliente.

O cliente pode optar por passar essas notificações informativas para o usuário. Em alguns estados em execução, o cliente pode querer exibir informações adicionais. Por exemplo, um manipulador de notificação que recebe uma notificação RASCS ConnectDevice pode chamar a \_ [**função RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obter o nome e o tipo do dispositivo que está sendo conectado. Outro exemplo é quando o cliente recebe uma notificação rascs \_ projetada. Isso ocorre quando a fase de projeção RAS da operação de conexão foi concluída. O cliente pode chamar a [**função RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obter informações adicionais sobre a projeção. O cliente pode usar essas informações para notificar o usuário sobre quais protocolos de rede podem ser usados por essa conexão.

Evite escrever código que dependa da ordem ou da ocorrência de estados informacionais específicos, pois isso pode variar entre plataformas.

 

 




