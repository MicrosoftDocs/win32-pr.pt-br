---
title: Fornecendo atualizações de status
description: Fornecendo atualizações de status
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Macro MCIWndSetActiveTimer
- Macro MCIWndSetInactiveTimer
- Macro MCIWndGetActiveTimer
- Macro MCIWndGetInactiveTimer
- Macro MCIWndSetTimers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363921"
---
# <a name="providing-status-updates"></a>Fornecendo atualizações de status

O MCIWnd usa temporizadores para atualizar periodicamente as informações na barra de título da janela e na barra de rolagem e para enviar mensagens de notificação para a janela pai. Um temporizador controla o período de atualização da janela ativa do MCIWnd e um segundo temporizador controla o período de atualização para janelas do MCIWnd que estão inativas. Seu aplicativo pode usar as macros do temporizador MCIWnd para recuperar as configurações do temporizador atual e ajustar os períodos de atualização.

Você pode definir o período de atualização usado pelo temporizador da janela ativa usando a macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) . Essa macro define o período usado pelo MCIWnd para atualizar o TrackBar, para atualizar a posição de reprodução relatada na barra de título da janela e para notificar a janela pai de que a mídia foi alterada. Você pode recuperar o período de atualização atual usado pelo temporizador da janela ativa usando a macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) . O período de atualização padrão para o temporizador de janela ativa é de 500 milissegundos.

Você pode definir o período de atualização usado pelo temporizador da janela inativa usando a macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) . Essa macro define o período usado pelo MCIWnd para atualizar o TrackBar, para atualizar a posição de reprodução relatada na legenda da janela e para notificar a janela pai de que a mídia foi alterada. Você pode recuperar o período de atualização atual usado pelo temporizador da janela inativa usando a macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) . O período de atualização padrão para o temporizador de janela inativa é de 2000 milissegundos.

Seu aplicativo pode definir simultaneamente o período de atualização para ambos os temporizadores usando a macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) . O armazenamento para o valor do período de atualização é limitado a 16 bits. Se uma quantidade maior para o período de atualização for necessária, defina os temporizadores individualmente.

 

 




