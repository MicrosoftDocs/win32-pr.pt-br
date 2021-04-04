---
title: Obtendo o status de uma operação do Gerenciador de reinicialização
description: Quando muitos aplicativos e serviços devem ser desligados ou reiniciados, a operação do Gerenciador de reinicialização pode levar um longo período de tempo. O método a seguir pode ser usado para obter o status da operação atual.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084811"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Obtendo o status de uma operação do Gerenciador de reinicialização

Quando muitos aplicativos e serviços devem ser desligados ou reiniciados, a operação do Gerenciador de reinicialização pode levar um longo período de tempo. O método a seguir pode ser usado para obter o status da operação atual.

**Para obter o status da operação atual do Gerenciador de reinicialização**

1.  O instalador deve implementar uma função de retorno de chamada de status de gravação do RM que determina o status dos aplicativos que foram desligados ou reiniciados. [**\_ \_ \_**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) A função pode fornecer as informações para a interface do usuário ou o log.
2.  O instalador passa o ponteiro para a função de [**retorno de chamada de status de \_ gravação \_ \_ do RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) ao chamar a função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .

 

 