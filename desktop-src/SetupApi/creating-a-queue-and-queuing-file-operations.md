---
description: Enfileirar as operações de arquivo é útil porque permite processar a instalação como um todo, em vez de por meio da seção INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Criando uma fila e enfileirando operações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755943"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="f743a-103">Criando uma fila e enfileirando operações de arquivo</span><span class="sxs-lookup"><span data-stu-id="f743a-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="f743a-104">Enfileirar as operações de arquivo é útil porque permite processar a instalação como um todo, em vez de por meio da seção INF.</span><span class="sxs-lookup"><span data-stu-id="f743a-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="f743a-105">Para criar uma fila de arquivos, declare uma variável para armazenar o identificador de fila e, em seguida, chame a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) .</span><span class="sxs-lookup"><span data-stu-id="f743a-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="f743a-106">Depois que a fila é criada, você pode enfileirar as operações de copiar, renomear e excluir, bem como examinar a fila de arquivos para verificar as operações enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="f743a-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="f743a-107">Para adicionar operações de arquivo único à fila, use as funções [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)e [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .</span><span class="sxs-lookup"><span data-stu-id="f743a-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="f743a-108">Todas as operações de arquivo listadas em uma seção **copiar** arquivos, **Excluir arquivos** ou **renomear arquivos** podem ser adicionadas à fila usando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)ou [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f743a-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="f743a-109">Outra maneira de enfileirar todos os arquivos nas seções **copiar arquivos** listadas em uma seção de **instalação** de um inf é usar a função [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="f743a-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="f743a-110">O exemplo a seguir usa a função [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) para enfileirar operações de cópia para todos os arquivos listados em uma seção **copiar arquivos** de um arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="f743a-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="f743a-111">No exemplo, MyQueue é a fila para a qual adicionar operações de cópia, "A: \\ " especifica o caminho para a origem e MyInf é o identificador para o arquivo inf aberto.</span><span class="sxs-lookup"><span data-stu-id="f743a-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="f743a-112">O parâmetro *ListInfHandle* é definido como **NULL**, indicando que a seção para cópia está em MyInf.</span><span class="sxs-lookup"><span data-stu-id="f743a-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="f743a-113">MySection é a seção em MyInf que contém os arquivos a serem colocados em fila para cópia.</span><span class="sxs-lookup"><span data-stu-id="f743a-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="f743a-114">A cópia do SP de sinalizadores \_ \_ noSkip e a cópia do SP \_ \_ não navegar foram combinadas usando um operador OR para indicar que o usuário não deve receber opções para ignorar ou procurar arquivos se ocorrerem erros.</span><span class="sxs-lookup"><span data-stu-id="f743a-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



