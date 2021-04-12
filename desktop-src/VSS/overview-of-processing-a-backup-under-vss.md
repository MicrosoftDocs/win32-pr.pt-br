---
description: Ao processar uma coordenada de backup, solicitante e gravadores para fornecer uma imagem de sistema estável da qual fazer backup de dados (o volume de sombra copiado), agrupar arquivos com base no uso e armazenar informações sobre os dados salvos.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Visão geral do processamento de um backup no VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296653"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Visão geral do processamento de um backup no VSS

Ao processar uma coordenada de backup, solicitante e gravadores para fornecer uma imagem de sistema estável da qual fazer backup de dados (o volume de sombra copiado), agrupar arquivos com base no uso e armazenar informações sobre os dados salvos. Isso deve ser feito ao criar apenas a interrupção mínima para o fluxo de trabalho normal do gravador.

Um solicitante consulta os gravadores para seus metadados, processa esses dados, notifica os gravadores antes do início da cópia de sombra e das operações de backup e, em seguida, notifica os gravadores novamente após a finalização da cópia de sombra e das operações de backup.

Em resposta a essas notificações, o gravador fornece informações sobre os arquivos para backup, incluindo a especificação de grupos de arquivos a serem coordenados ([*componentes*](vssgloss-c.md)) — pausa em suas operações de e/s antes de uma cópia de sombra e, em seguida, retorna à operação normal após a conclusão de uma cópia de sombra ou no final do backup.

No decorrer do processamento do backup, um gravador especifica os arquivos pelos quais ele é responsável por meio de seus metadados somente leitura – o documento de metadados do gravador (consulte [metadados do VSS: trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md)). Em seguida, o solicitante interpreta esses metadados, escolhe o que fazer backup e armazena essas decisões em seu próprio objeto de metadados, o documento de componentes de backup (consulte [metadados do VSS: trabalhando com o documento de componentes de backup](working-with-the-backup-components-document.md)). Este documento de componentes de backup está disponível para inspeção e modificação do gravador durante as operações de backup e restauração.

Este diagrama mostra as interações entre o solicitante, o serviço VSS, o suporte ao kernel do VSS, quaisquer gravadores VSS envolvidos e quaisquer provedores de hardware VSS.

![interações entre o solicitante, os componentes de backup, os gravadores e os provedores](images/vssimpl.png)

Para entender com mais detalhes as tarefas básicas envolvidas na execução de um backup, é útil dividir essa visão geral nos seguintes tópicos:

-   [Visão geral da inicialização do backup](overview-of-backup-initialization.md)
-   [Visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md)
-   [Visão geral das tarefas de pré-backup](overview-of-pre-backup-tasks.md)
-   [Visão geral do backup real de arquivos](overview-of-actual-backup-of-files.md)
-   [Visão geral do encerramento do backup](overview-of-backup-termination.md)

 

 



