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
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="34a35-103">Visão geral do processamento de um backup no VSS</span><span class="sxs-lookup"><span data-stu-id="34a35-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="34a35-104">Ao processar uma coordenada de backup, solicitante e gravadores para fornecer uma imagem de sistema estável da qual fazer backup de dados (o volume de sombra copiado), agrupar arquivos com base no uso e armazenar informações sobre os dados salvos.</span><span class="sxs-lookup"><span data-stu-id="34a35-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="34a35-105">Isso deve ser feito ao criar apenas a interrupção mínima para o fluxo de trabalho normal do gravador.</span><span class="sxs-lookup"><span data-stu-id="34a35-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="34a35-106">Um solicitante consulta os gravadores para seus metadados, processa esses dados, notifica os gravadores antes do início da cópia de sombra e das operações de backup e, em seguida, notifica os gravadores novamente após a finalização da cópia de sombra e das operações de backup.</span><span class="sxs-lookup"><span data-stu-id="34a35-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="34a35-107">Em resposta a essas notificações, o gravador fornece informações sobre os arquivos para backup, incluindo a especificação de grupos de arquivos a serem coordenados ([*componentes*](vssgloss-c.md)) — pausa em suas operações de e/s antes de uma cópia de sombra e, em seguida, retorna à operação normal após a conclusão de uma cópia de sombra ou no final do backup.</span><span class="sxs-lookup"><span data-stu-id="34a35-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="34a35-108">No decorrer do processamento do backup, um gravador especifica os arquivos pelos quais ele é responsável por meio de seus metadados somente leitura – o documento de metadados do gravador (consulte [metadados do VSS: trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="34a35-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="34a35-109">Em seguida, o solicitante interpreta esses metadados, escolhe o que fazer backup e armazena essas decisões em seu próprio objeto de metadados, o documento de componentes de backup (consulte [metadados do VSS: trabalhando com o documento de componentes de backup](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="34a35-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="34a35-110">Este documento de componentes de backup está disponível para inspeção e modificação do gravador durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="34a35-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="34a35-111">Este diagrama mostra as interações entre o solicitante, o serviço VSS, o suporte ao kernel do VSS, quaisquer gravadores VSS envolvidos e quaisquer provedores de hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="34a35-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![interações entre o solicitante, os componentes de backup, os gravadores e os provedores](images/vssimpl.png)

<span data-ttu-id="34a35-113">Para entender com mais detalhes as tarefas básicas envolvidas na execução de um backup, é útil dividir essa visão geral nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="34a35-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="34a35-114">Visão geral da inicialização do backup</span><span class="sxs-lookup"><span data-stu-id="34a35-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="34a35-115">Visão geral da fase de descoberta de backup</span><span class="sxs-lookup"><span data-stu-id="34a35-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="34a35-116">Visão geral das tarefas de pré-backup</span><span class="sxs-lookup"><span data-stu-id="34a35-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="34a35-117">Visão geral do backup real de arquivos</span><span class="sxs-lookup"><span data-stu-id="34a35-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="34a35-118">Visão geral do encerramento do backup</span><span class="sxs-lookup"><span data-stu-id="34a35-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



