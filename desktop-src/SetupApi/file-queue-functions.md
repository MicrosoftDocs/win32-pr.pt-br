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
# <a name="file-queue-functions"></a><span data-ttu-id="43471-103">Funções de fila de arquivos</span><span class="sxs-lookup"><span data-stu-id="43471-103">File Queue Functions</span></span>

<span data-ttu-id="43471-104">As funções a seguir são usadas com filas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="43471-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="43471-105">Função</span><span class="sxs-lookup"><span data-stu-id="43471-105">Function</span></span>                                                             | <span data-ttu-id="43471-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="43471-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43471-107">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="43471-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="43471-108">Encerra a fila.</span><span class="sxs-lookup"><span data-stu-id="43471-108">Terminates the queue.</span></span> <span data-ttu-id="43471-109">As transações restantes não são confirmadas.</span><span class="sxs-lookup"><span data-stu-id="43471-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="43471-110">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="43471-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="43471-111">Confirma todas as transações em fila.</span><span class="sxs-lookup"><span data-stu-id="43471-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="43471-112">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="43471-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="43471-113">Inicializa e retorna um identificador para a fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="43471-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="43471-114">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="43471-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="43471-115">Solicita que o usuário reinicialize seu computador, se necessário.</span><span class="sxs-lookup"><span data-stu-id="43471-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="43471-116">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="43471-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="43471-117">Enfileira uma cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="43471-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="43471-118">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="43471-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="43471-119">Enfileira os arquivos em uma seção arquivos de cópia INF.</span><span class="sxs-lookup"><span data-stu-id="43471-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="43471-120">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="43471-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="43471-121">Enfileira os arquivos em uma seção arquivos de cópia INF usando as informações padrão especificadas em um arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="43471-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="43471-122">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="43471-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="43471-123">Enfileira uma exclusão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="43471-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="43471-124">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="43471-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="43471-125">Enfileira os arquivos em uma seção INF delete files.</span><span class="sxs-lookup"><span data-stu-id="43471-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="43471-126">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="43471-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="43471-127">Enfileira uma renomeação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="43471-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="43471-128">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="43471-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="43471-129">Enfileira os arquivos em uma seção arquivos INF Rename.</span><span class="sxs-lookup"><span data-stu-id="43471-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="43471-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="43471-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="43471-131">Verifica a fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="43471-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="43471-132">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="43471-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="43471-133">Define a substituição do caminho da plataforma.</span><span class="sxs-lookup"><span data-stu-id="43471-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



