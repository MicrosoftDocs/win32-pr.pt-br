---
title: Cancelando a operação atual do Gerenciador de reinicialização
description: Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de reinicialização.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637288"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Cancelando a operação atual do Gerenciador de reinicialização

Quando uma ação do usuário direciona o instalador para executar uma ação diferente, o método a seguir pode ser usado para cancelar a operação atual do Gerenciador de reinicialização.

**Para cancelar a operação atual do Gerenciador de reinicialização**

-   O instalador pode chamar a função [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) de outro thread para cancelar a operação atual de [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) . O Gerenciador de reinicialização pode cancelar a operação dependendo da extensão até a qual a operação foi concluída quando a função **RMCancelCurrentTask** é chamada.

 

 




