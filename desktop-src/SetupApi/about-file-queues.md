---
description: Uma fila de arquivos é uma lista de operações de arquivo que são processadas de uma vez. As operações de arquivo na fila podem ser operações de cópia, renomeação ou exclusão. A fila de arquivos organiza as operações de arquivo por tipo, criando cópias, renomear e excluir subfilas.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Sobre filas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751067"
---
# <a name="about-file-queues"></a><span data-ttu-id="638d0-105">Sobre filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="638d0-105">About File Queues</span></span>

<span data-ttu-id="638d0-106">Uma fila de arquivos é uma lista de operações de arquivo que são processadas de uma vez.</span><span class="sxs-lookup"><span data-stu-id="638d0-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="638d0-107">As operações de arquivo na fila podem ser operações de cópia, renomeação ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="638d0-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="638d0-108">A fila de arquivos organiza as operações de arquivo por tipo, criando cópias, renomear e excluir subfilas.</span><span class="sxs-lookup"><span data-stu-id="638d0-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="638d0-109">Essas operações podem ser enviadas para a fila em qualquer ordem, e o processo de enfileiramento não precisa ser contíguo.</span><span class="sxs-lookup"><span data-stu-id="638d0-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="638d0-110">Quando a fila é confirmada, a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) executa operações de arquivo na ordem do tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="638d0-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="638d0-111">Normalmente, todas as operações de arquivo necessárias para uma instalação inteira são enfileiradas na fila de arquivos e, em seguida, processadas em um único lote quando a fila é confirmada.</span><span class="sxs-lookup"><span data-stu-id="638d0-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="638d0-112">Uma vantagem de enfileirar operações de arquivo na seção Instalando arquivos por seção de um arquivo INF é que você pode simplificar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="638d0-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="638d0-113">Em vez de ter que obter informações do usuário para que cada seção seja instalada, você pode obter informações de instalação do usuário para todos os arquivos a serem instalados durante a criação da fila.</span><span class="sxs-lookup"><span data-stu-id="638d0-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="638d0-114">Isso libera o usuário para buscar outras atividades enquanto as operações de cópia com uso intensivo de tempo são processadas pela função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .</span><span class="sxs-lookup"><span data-stu-id="638d0-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="638d0-115">Outra vantagem das filas de arquivos é que você pode acompanhar o progresso da instalação como um todo.</span><span class="sxs-lookup"><span data-stu-id="638d0-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="638d0-116">Ao instalar seções por seção de um arquivo INF, indicadores de progresso como barras de progresso podem rastrear apenas a seção INF atual.</span><span class="sxs-lookup"><span data-stu-id="638d0-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="638d0-117">Quando a próxima seção for instalada, a barra de progresso será iniciada.</span><span class="sxs-lookup"><span data-stu-id="638d0-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="638d0-118">Com uma fila, o número total de arquivos a serem processados durante toda a instalação é conhecido antes da fila ser confirmada e, portanto, uma barra de progresso pode ser gerada para rastrear toda a instalação.</span><span class="sxs-lookup"><span data-stu-id="638d0-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="638d0-119">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="638d0-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="638d0-120">Ordem de compromisso de fila</span><span class="sxs-lookup"><span data-stu-id="638d0-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="638d0-121">Notificações de fila</span><span class="sxs-lookup"><span data-stu-id="638d0-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



