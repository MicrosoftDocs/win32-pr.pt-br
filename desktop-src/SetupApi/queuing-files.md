---
description: Depois de obter um identificador para uma fila de arquivos chamando a função SetupOpenFileQueue, você pode adicionar operações de arquivo à fila, arquivo por arquivo ou enfileirando todos os arquivos em uma seção INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Enfileirando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828540"
---
# <a name="queuing-files"></a><span data-ttu-id="8d007-103">Enfileirando arquivos</span><span class="sxs-lookup"><span data-stu-id="8d007-103">Queuing Files</span></span>

<span data-ttu-id="8d007-104">Depois de obter um identificador para uma fila de arquivos chamando a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , você pode adicionar operações de arquivo à fila, arquivo por arquivo ou enfileirando todos os arquivos em uma seção inf.</span><span class="sxs-lookup"><span data-stu-id="8d007-104">After you have obtained a handle to a file queue by calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function, you can add file operations to the queue, either file-by-file, or by queuing all the files in an INF section.</span></span>

<span data-ttu-id="8d007-105">Para adicionar uma operação de cópia para um arquivo individual à fila de arquivos, chame a função [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) .</span><span class="sxs-lookup"><span data-stu-id="8d007-105">To add a copy operation for an individual file to the file queue, call the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) function.</span></span> <span data-ttu-id="8d007-106">Se você quiser enfileirar uma operação de cópia de arquivo usando a mídia de origem padrão e os destinos de destino especificados em um arquivo INF, você pode chamar a função [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .</span><span class="sxs-lookup"><span data-stu-id="8d007-106">If you want to queue a file copy operation using the default source media and target destinations specified in an INF file, you can call the [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) function.</span></span>

<span data-ttu-id="8d007-107">Você pode adicionar uma operação individual de exclusão ou renomeação de arquivo à fila de arquivos aberta, chamando a função [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) ou [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .</span><span class="sxs-lookup"><span data-stu-id="8d007-107">You can add an individual file delete or rename operation to the open file queue, by calling the [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) or [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) function.</span></span>

 

 



