---
title: Notificações de conclusão
description: O Gerenciador de conexões de acesso remoto continua as notificações de progresso até que a operação de conexão seja concluída.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005559"
---
# <a name="completion-notifications"></a>Notificações de conclusão

O Gerenciador de conexões de acesso remoto continua as notificações de progresso até que a operação de conexão seja concluída. Isso ocorre nas seguintes situações:

-   O manipulador recebe uma \_ notificação RASCS conectada ou RASCS \_ desconectada. O aplicativo cliente RAS pode sair sem interromper nenhuma conexão estabelecida.
-   Ocorre um erro. O manipulador recebe uma notificação indicando o erro e o estado da conexão quando o erro ocorreu. O aplicativo cliente RAS pode sair.

O aplicativo cliente RAS não deve assumir que a operação de conexão foi concluída após chamar [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa). Ele deve aguardar uma das condições anteriores antes de sair.

 

 




