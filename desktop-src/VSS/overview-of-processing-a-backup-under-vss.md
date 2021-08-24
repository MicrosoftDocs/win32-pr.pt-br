---
description: No processamento de um backup, o solicitante e os autores coordenam para fornecer uma imagem estável do sistema da qual fazer backup de dados (o volume copiado de sombra), agrupar arquivos com base em seu uso e armazenar informações sobre os dados salvos.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Visão geral do processamento de um backup no VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60874b1c66bcc75788912f54e5b3ffc8314f1bc0d0ad6d92b815725af727936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510006"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Visão geral do processamento de um backup no VSS

No processamento de um backup, o solicitante e os autores coordenam para fornecer uma imagem estável do sistema da qual fazer backup de dados (o volume copiado de sombra), agrupar arquivos com base em seu uso e armazenar informações sobre os dados salvos. Tudo isso deve ser feito ao criar apenas uma interrupção mínima para o fluxo de trabalho normal do autor.

Um solicitante consulta os autores de seus metadados, processa esses dados, notifica os autores antes do início da cópia de sombra e das operações de backup e, em seguida, notifica os autores novamente após o término das operações de backup e cópia de sombra.

Em resposta a essas notificações, o autor fornece informações sobre os arquivos a serem copiados em backup , incluindo a especificação de grupos de arquivos para coordenar [*(*](vssgloss-c.md)componentes ) – pausa em suas operações de E/S antes de uma cópia de sombra e retorna à operação normal após a conclusão de uma cópia de sombra ou no final do backup.

No decorrer do processamento do backup, um autor especifica os arquivos pelos que ele é responsável por meio de seus metadados somente leitura— o Documento de Metadados do Writer (consulte Metadados do [VSS:](working-with-the-writer-metadata-document.md)trabalhando com o documento de metadados do autor). Em seguida, o solicitante interpreta esses metadados, escolhe o que fazer backup e armazena essas decisões em seu próprio objeto de metadados, o Documento de Componentes de Backup (consulte Metadados do [VSS:](working-with-the-backup-components-document.md)trabalhando com o documento componentes de backup ). Este Documento de Componentes de Backup está disponível para inspeção e modificação do autor durante as operações de backup e restauração.

Este diagrama mostra as interações entre o solicitante, o serviço VSS, o suporte ao kernel do VSS, quaisquer autores VSS envolvidos e quaisquer provedores de hardware VSS.

![interações entre solicitante, componentes de backup, autores e provedores](images/vssimpl.png)

Para entender melhor as tarefas básicas envolvidas na execução de um backup, é útil desmá-la nos seguintes tópicos:

-   [Visão geral da inicialização de backup](overview-of-backup-initialization.md)
-   [Visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md)
-   [Visão geral das tarefas de pré-backup](overview-of-pre-backup-tasks.md)
-   [Visão geral do backup real de arquivos](overview-of-actual-backup-of-files.md)
-   [Visão geral da terminação de backup](overview-of-backup-termination.md)

 

 



