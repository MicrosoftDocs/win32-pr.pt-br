---
description: Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos. Chamar a função SetupOpenFileQueue retorna um identificador para um arquivo de fila. Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrindo e fechando uma fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753918"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="9b09a-105">Abrindo e fechando uma fila</span><span class="sxs-lookup"><span data-stu-id="9b09a-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="9b09a-106">Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b09a-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="9b09a-107">Chamar a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) retorna um identificador para um arquivo de fila.</span><span class="sxs-lookup"><span data-stu-id="9b09a-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="9b09a-108">Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.</span><span class="sxs-lookup"><span data-stu-id="9b09a-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="9b09a-109">Depois que todas as operações de arquivo especificadas tiverem sido enfileiradas e confirmadas, você deverá chamar a função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar recursos alocados durante a chamada para [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="9b09a-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="9b09a-110">A função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) não confirma a fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b09a-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="9b09a-111">Todas as operações que não forem confirmadas quando **SetupCloseFileQueue** for chamado não serão executadas.</span><span class="sxs-lookup"><span data-stu-id="9b09a-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



