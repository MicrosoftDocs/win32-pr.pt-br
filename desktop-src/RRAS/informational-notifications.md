---
title: Notificações informativas
description: Para os Estados de conexão conhecidos como Estados em execução, nenhuma ação é necessária para o manipulador de notificação, a menos que ocorra um erro.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "104453885"
---
# <a name="informational-notifications"></a>Notificações informativas

Para os [Estados de conexão](connection-states.md) conhecidos como Estados em execução, nenhuma ação é necessária para o manipulador de notificação, a menos que ocorra um erro. Os Estados em execução ocorrem durante as partes da operação de conexão que o RAS manipula automaticamente, como conectar-se aos dispositivos necessários, autenticar o usuário e aguardar um retorno de chamada do servidor remoto. A notificação é simplesmente um relatório de progresso para o cliente.

O cliente pode optar por passar essas notificações informativas para o usuário. Em alguns Estados em execução, o cliente talvez queira exibir informações adicionais. Por exemplo, um manipulador de notificação que recebe uma \_ notificação RASCS ConnectDevice pode chamar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obter o nome e o tipo do dispositivo que está sendo conectado. Outro exemplo é quando o cliente recebe uma \_ notificação projetada de RASCS. Isso ocorre quando a fase de projeção de RAS da operação de conexão foi concluída. O cliente pode chamar a função [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obter informações adicionais sobre a projeção. O cliente pode usar essas informações para notificar o usuário sobre quais protocolos de rede podem ser usados por essa conexão.

Você deve evitar escrever código que dependa da ordem ou ocorrência de determinados Estados informativos, pois isso pode variar entre plataformas.

 

 




