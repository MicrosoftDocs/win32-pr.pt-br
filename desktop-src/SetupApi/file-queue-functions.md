---
description: As funções a seguir são usadas com filas de arquivos.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funções de fila de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753088"
---
# <a name="file-queue-functions"></a>Funções de fila de arquivos

As funções a seguir são usadas com filas de arquivos.



| Função                                                             | Descrição                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Encerra a fila. As transações restantes não são confirmadas.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Confirma todas as transações em fila.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Inicializa e retorna um identificador para a fila de arquivos.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Solicita que o usuário reinicialize seu computador, se necessário.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Enfileira uma cópia de arquivo.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Enfileira os arquivos em uma seção arquivos de cópia INF.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Enfileira os arquivos em uma seção arquivos de cópia INF usando as informações padrão especificadas em um arquivo INF. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Enfileira uma exclusão de arquivo.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Enfileira os arquivos em uma seção INF delete files.                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Enfileira uma renomeação de arquivo.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Enfileira os arquivos em uma seção arquivos INF Rename.                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Verifica a fila de arquivos.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Define a substituição do caminho da plataforma.                                                                      |



 

 

 



