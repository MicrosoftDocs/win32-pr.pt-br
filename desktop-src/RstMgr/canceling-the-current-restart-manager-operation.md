---
title: Cancelando a operação atual do Gerenciador de Reinicialização
description: Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de Reinicialização.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010244"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Cancelando a operação atual do Gerenciador de Reinicialização

Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de Reinicialização.

**Para cancelar a operação atual do Gerenciador de Reinicialização**

-   O instalador pode chamar a [**função RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) de outro thread para cancelar a operação [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) atual. O Gerenciador de Reinicialização pode cancelar a operação dependendo da extensão em que a operação foi concluída quando a **função RMCancelCurrentTask** é chamada.

 

 




