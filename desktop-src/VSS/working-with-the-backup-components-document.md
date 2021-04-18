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
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="79b54-103">Trabalhando com o documento de componentes de backup</span><span class="sxs-lookup"><span data-stu-id="79b54-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="79b54-104">Um solicitante cria um documento de componentes de backup no início da execução de um backup.</span><span class="sxs-lookup"><span data-stu-id="79b54-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="79b54-105">Inicialmente, o documento contém apenas uma descrição do estado da operação de backup.</span><span class="sxs-lookup"><span data-stu-id="79b54-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="79b54-106">Durante a restauração, o documento deve fornecer instruções sobre como um solicitante deve continuar copiando os arquivos de volta para o disco.</span><span class="sxs-lookup"><span data-stu-id="79b54-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="79b54-107">No decorrer da operação de restauração, o documento de componentes de backup é modificado e contém o estado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="79b54-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="79b54-108">Ao contrário do documento de metadados do gravador, que é somente leitura, há uma janela na qual o documento de componentes de backup pode ser modificado por solicitantes e gravadores.</span><span class="sxs-lookup"><span data-stu-id="79b54-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="79b54-109">O documento pode ser atualizado até a geração de um evento [*BackupComplete*](vssgloss-b.md) ou [*BackupShutdown*](vssgloss-b.md) durante as operações de backup e até um evento de [*restauração*](vssgloss-p.md) durante as restaurações.</span><span class="sxs-lookup"><span data-stu-id="79b54-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="79b54-110">Para usar o documento de componentes de backup de um solicitante, é necessário compreender os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="79b54-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="79b54-111">Ciclo de vida do documento de componentes de backup</span><span class="sxs-lookup"><span data-stu-id="79b54-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="79b54-112">Conteúdo do documento de componentes de backup</span><span class="sxs-lookup"><span data-stu-id="79b54-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



