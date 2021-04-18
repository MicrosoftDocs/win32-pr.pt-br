---
description: Um solicitante cria um documento de componentes de backup no início da execução de um backup.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Trabalhando com o documento de componentes de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796464"
---
# <a name="working-with-the-backup-components-document"></a>Trabalhando com o documento de componentes de backup

Um solicitante cria um documento de componentes de backup no início da execução de um backup. Inicialmente, o documento contém apenas uma descrição do estado da operação de backup. Durante a restauração, o documento deve fornecer instruções sobre como um solicitante deve continuar copiando os arquivos de volta para o disco. No decorrer da operação de restauração, o documento de componentes de backup é modificado e contém o estado dessa operação.

Ao contrário do documento de metadados do gravador, que é somente leitura, há uma janela na qual o documento de componentes de backup pode ser modificado por solicitantes e gravadores. O documento pode ser atualizado até a geração de um evento [*BackupComplete*](vssgloss-b.md) ou [*BackupShutdown*](vssgloss-b.md) durante as operações de backup e até um evento de [*restauração*](vssgloss-p.md) durante as restaurações.

Para usar o documento de componentes de backup de um solicitante, é necessário compreender os seguintes tópicos:

-   [Ciclo de vida do documento de componentes de backup](backup-components-document-life-cycle.md)
-   [Conteúdo do documento de componentes de backup](backup-components-document-contents.md)

 

 



