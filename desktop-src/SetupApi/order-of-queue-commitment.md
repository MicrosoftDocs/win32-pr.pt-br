---
description: 'Quando a função SetupCommitFileQueue confirma a fila de arquivos, ela processa as operações de arquivo na seguinte ordem: operações de exclusão de arquivo, operações de renomeação de arquivo e, por fim, operações de cópia de arquivo.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordem de compromisso de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828688"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="b3b20-103">Ordem de compromisso de fila</span><span class="sxs-lookup"><span data-stu-id="b3b20-103">Order of Queue Commitment</span></span>

<span data-ttu-id="b3b20-104">Quando a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirma a fila de arquivos, ela processa as operações de arquivo na seguinte ordem: operações de exclusão de arquivo, operações de renomeação de arquivo e, por fim, operações de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b3b20-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="b3b20-105">A estrutura de tópicos a seguir ilustra o ciclo de vida do processo de compromisso de uma fila.</span><span class="sxs-lookup"><span data-stu-id="b3b20-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="b3b20-106">iniciar a exclusão da subfila</span><span class="sxs-lookup"><span data-stu-id="b3b20-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="b3b20-107">iniciar uma operação de exclusão de arquivo <--repetir para cada</span><span class="sxs-lookup"><span data-stu-id="b3b20-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="b3b20-108">concluir uma operação de exclusão de arquivo <--exclusão de arquivo na fila</span><span class="sxs-lookup"><span data-stu-id="b3b20-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="b3b20-109">concluir a exclusão da subfila</span><span class="sxs-lookup"><span data-stu-id="b3b20-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="b3b20-110">iniciar a subfila de renomeação</span><span class="sxs-lookup"><span data-stu-id="b3b20-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="b3b20-111">iniciar uma operação de renomeação de arquivo <--repetir para cada</span><span class="sxs-lookup"><span data-stu-id="b3b20-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="b3b20-112">concluir uma operação de exclusão de arquivo <--renomeação de arquivo na fila</span><span class="sxs-lookup"><span data-stu-id="b3b20-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="b3b20-113">concluir a subfila de renomeação</span><span class="sxs-lookup"><span data-stu-id="b3b20-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="b3b20-114">Inicie a cópia subque</span><span class="sxs-lookup"><span data-stu-id="b3b20-114">start the copy subque</span></span>
    -   <span data-ttu-id="b3b20-115">iniciar uma operação de cópia de arquivo <--repetir para cada</span><span class="sxs-lookup"><span data-stu-id="b3b20-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="b3b20-116">concluir uma operação de cópia de arquivo <--cópia de arquivo na fila</span><span class="sxs-lookup"><span data-stu-id="b3b20-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="b3b20-117">concluir a cópia da subfila</span><span class="sxs-lookup"><span data-stu-id="b3b20-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="b3b20-118">concluir a fila</span><span class="sxs-lookup"><span data-stu-id="b3b20-118">finish the queue</span></span>

 

<span data-ttu-id="b3b20-119">Em cada etapa, ou se ocorrer um erro, a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviará uma notificação para a rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b3b20-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="b3b20-120">A rotina de retorno de chamada pode usar as informações enviadas pela fila para acompanhar o progresso da instalação e, se necessário, interagir com o usuário.</span><span class="sxs-lookup"><span data-stu-id="b3b20-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="b3b20-121">Por exemplo, se uma operação de cópia de arquivo precisar de um arquivo de origem que não estava disponível no caminho atual, o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviará uma notificação de SPFILENOTIFY \_ NEEDMEDIA para a rotina de retorno de chamada, juntamente com informações sobre o arquivo e a mídia necessária.</span><span class="sxs-lookup"><span data-stu-id="b3b20-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="b3b20-122">A rotina de retorno de chamada pode usar essas informações para gerar uma caixa de diálogo que solicita ao usuário para inserir o próximo disco chamando [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="b3b20-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="b3b20-123">Uma rotina de retorno de chamada de fila padrão, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), está incluída na API de instalação.</span><span class="sxs-lookup"><span data-stu-id="b3b20-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="b3b20-124">Essa rotina manipula notificações de fila e gera caixas de diálogo de erro e barras de progresso para a instalação.</span><span class="sxs-lookup"><span data-stu-id="b3b20-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="b3b20-125">Você pode usar a rotina de retorno de chamada de fila padrão como está, ou escrever uma rotina de retorno de chamada de filtro para manipular um subconjunto das notificações e passar os outros para a rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="b3b20-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="b3b20-126">Se nenhuma das funcionalidades da rotina de retorno de chamada atender às suas necessidades, você poderá escrever uma rotina de retorno de chamada personalizada independente que não chame a rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="b3b20-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="b3b20-127">Para obter mais informações sobre rotinas de retorno de chamada de fila, consulte [rotina de retorno de chamada de fila padrão](default-queue-callback-routine.md)e [criando uma rotina de retorno de chamada de fila personalizada](creating-a-custom-queue-callback-routine.md)</span><span class="sxs-lookup"><span data-stu-id="b3b20-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



