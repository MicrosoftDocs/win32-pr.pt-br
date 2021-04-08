---
description: As funções de instalação incluem a funcionalidade de fila de arquivos.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Filas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922092"
---
# <a name="file-queues"></a><span data-ttu-id="b0aae-103">Filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0aae-103">File Queues</span></span>

<span data-ttu-id="b0aae-104">As funções de instalação incluem a funcionalidade de fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0aae-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="b0aae-105">Uma fila de arquivos é uma lista de operações de cópia, renomeação e exclusão de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0aae-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="b0aae-106">Essas operações podem ser enviadas para a fila em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="b0aae-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="b0aae-107">Quando a fila é confirmada, essas operações são processadas como um lote, na ordem do tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="b0aae-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="b0aae-108">As seções a seguir explicam o que é uma fila e como usá-la ao criar um aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="b0aae-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="b0aae-109">Também é discutido a ordem na qual as operações de arquivo enfileiradas são processadas à medida que a fila é confirmada e quais notificações a fila envia para uma rotina de retorno de chamada em cada estágio.</span><span class="sxs-lookup"><span data-stu-id="b0aae-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="b0aae-110">Sobre filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0aae-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="b0aae-111">Usando filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0aae-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="b0aae-112">Referência da fila de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0aae-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



