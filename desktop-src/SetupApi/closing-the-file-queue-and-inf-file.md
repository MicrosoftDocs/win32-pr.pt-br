---
description: Depois que a fila terminar de confirmar suas operações, ela deverá ser fechada usando a função SetupCloseFileQueue com o identificador que foi criado pelo SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Fechando a fila de arquivos e o arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769183"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="d084a-103">Fechando a fila de arquivos e o arquivo INF</span><span class="sxs-lookup"><span data-stu-id="d084a-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="d084a-104">Depois que a fila terminar de confirmar suas operações, ela deverá ser fechada usando a função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) com o identificador que foi criado pelo [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="d084a-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="d084a-105">O retorno de chamada da fila padrão deve ser destruído e recriado para que outra fila possa ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="d084a-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="d084a-106">Se um contexto padrão foi iniciado para uso pela rotina de retorno de chamada padrão, ele também deve ser encerrado chamando a função [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="d084a-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="d084a-107">O *contexto* é um ponteiro para a estrutura retornada pela função [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="d084a-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="d084a-108">Quando o acesso às informações de INF não for mais necessário, chame a função [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) com o identificador que foi criado pelo [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) para liberar recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="d084a-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



